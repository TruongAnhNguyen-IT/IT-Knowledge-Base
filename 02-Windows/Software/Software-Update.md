# Software Update – Cập nhật phần mềm Windows

## 1. Mục tiêu / Purpose

### Tiếng Việt
Cập nhật phần mềm giúp vá lỗ hổng, sửa lỗi và duy trì tương thích. Tuy nhiên, cập nhật có thể làm thay đổi chức năng hoặc gây gián đoạn; cần kiểm soát phiên bản, thử nghiệm, triển khai theo giai đoạn và có phương án phục hồi.

### English
Software updates patch vulnerabilities, fix defects, and maintain compatibility. Updates can also change functionality or disrupt services; version control, testing, phased rollout, and recovery planning are essential.

## 2. Phân loại cập nhật / Update types

- Security update – bản vá bảo mật
- Bug fix / maintenance release – sửa lỗi/bảo trì
- Feature update – bổ sung hoặc thay đổi tính năng
- Major version upgrade – nâng phiên bản lớn
- Runtime/dependency update – cập nhật thành phần phụ thuộc
- Driver/firmware update – cần đánh giá riêng vì có thể ảnh hưởng phần cứng
- Definition/signature update – dữ liệu nhận diện bảo mật

## 3. Trước khi cập nhật / Before updating

1. Xác định ứng dụng, phiên bản hiện tại, phiên bản đích và lý do.
2. Đọc release notes, known issues, yêu cầu reboot và lộ trình hỗ trợ.
3. Xác nhận backup dữ liệu/cấu hình và khả năng rollback.
4. Kiểm tra dependency, tích hợp, plugin, macro và kết nối tới hệ thống nghiệp vụ.
5. Chọn nhóm pilot và thời gian thay đổi.
6. Thông báo người dùng và chuẩn bị hỗ trợ sau cập nhật.
   
1. Identify the app, current/target versions, and reason.
2. Review release notes, known issues, reboot requirements, and support lifecycle.
3. Confirm data/configuration backups and rollback capability.
4. Check dependencies, integrations, plug-ins, macros, and business-system connectivity.
5. Select a pilot group and change window.
6. Notify users and prepare post-update support.
   
## 4. Kiểm tra phiên bản / Check versions

```powershell
# WinGet inventory; availability depends on WinGet version and policy
winget list

# Query a package's current source metadata before updating
winget show --id 7zip.7zip --exact

# Find package-specific update candidates
winget upgrade
```

Không giả định tên hiển thị giống Package ID. Kiểm tra publisher, ID, source và phiên bản trước khi dùng `--id` hoặc tự động hóa.

Do not assume a display name equals a Package ID. Validate publisher, ID, source, and version before using `--id` or automation.

## 5. Cập nhật bằng WinGet / Update with WinGet

```powershell
# Review available upgrades first
winget upgrade

# Update a verified package ID
winget upgrade --id 7zip.7zip --exact
```

`winget upgrade --all` có thể cập nhật nhiều ứng dụng và gây thay đổi rộng; chỉ dùng sau khi đánh giá danh sách, kiểm tra tương thích và được phê duyệt. Tùy package, một số ứng dụng không hỗ trợ nâng cấp im lặng hoặc cần thao tác thủ công.

`winget upgrade --all` can update many applications and cause broad changes; use it only after reviewing candidates, checking compatibility, and obtaining approval. Some packages do not support silent upgrades or require manual action.

## 6. Cập nhật thủ công / Vendor-managed updates

- Dùng chức năng Update trong ứng dụng nếu đây là phương thức được nhà cung cấp hỗ trợ.
- Với ứng dụng nghiệp vụ, tham khảo release channel và lịch phát hành của vendor.
- Không tải bản cập nhật từ trang mirror không được xác minh.
- Với ứng dụng có dữ liệu cục bộ, kiểm tra backup và schema migration.
- Ghi lại installer/version, hash/chữ ký, thời gian, exit code và log.

- Use the application's built-in updater when vendor-supported.
- For business apps, follow the vendor's release channel and schedule.
- Do not download updates from unverified mirror sites.
- For apps with local data, verify backups and schema migrations.
- Record installer/version, hash/signature, time, exit code, and logs.

## 7. Cập nhật theo giai đoạn / Phased rollout

| Vòng / Ring | Phạm vi / Scope | Tiêu chí tiếp tục / Exit criteria |
|---|---|---|
| Lab | VM/test devices | Cài đặt, chức năng chính và rollback được xác minh / Install, core function, rollback validated |
| IT pilot | IT staff | Không có lỗi nghiêm trọng / No critical failures |
| Business pilot | Đại diện nhóm nghiệp vụ | Workflow và tích hợp hoạt động / Workflow and integrations work |
| Broad rollout | Nhóm còn lại | Tỷ lệ thành công đạt ngưỡng đã thống nhất / Success rate meets agreed threshold |
| Monitor | Sau triển khai | Ticket, crash và hiệu năng ổn định / Tickets, crashes, and performance stable |

Ngưỡng thành công, thời gian quan sát và tiêu chí dừng phải được xác định trong change record, không đặt tùy tiện sau khi sự cố xảy ra.

Define success thresholds, observation periods, and stop criteria in the change record before deployment—not after an incident occurs.

## 8. Ghi log và xác minh / Logging and validation

```powershell
$start = Get-Date
# Perform the approved update here.
$end = Get-Date

"Started: $start"
"Ended:   $end"

# Check application crashes/errors around the change window
Get-WinEvent -FilterHashtable @{
  LogName='Application'
  StartTime=$start.AddMinutes(-5)
  EndTime=$end.AddMinutes(30)
} -ErrorAction SilentlyContinue |
  Where-Object { $_.LevelDisplayName -in 'Error','Critical','Warning' } |
  Select-Object TimeCreated, ProviderName, Id, LevelDisplayName, Message
```

Đừng chỉ xác minh “installer chạy xong”. Kiểm tra phiên bản thực tế, chức năng chính, dịch vụ, tích hợp, log và xác nhận người dùng.

Do not stop at “the installer finished.” Verify the actual version, core functions, services, integrations, logs, and user confirmation.

## 9. Rollback / Quay lại phiên bản trước

### Tiếng Việt
Không phải mọi ứng dụng đều hỗ trợ downgrade. Trước khi cập nhật, xác định một trong các phương án: gói phiên bản cũ được vendor hỗ trợ, backup/snapshot hợp lệ, restore dữ liệu, hoặc phương án khắc phục do vendor hướng dẫn. Với cơ sở dữ liệu, downgrade binary có thể không tương thích với schema đã nâng cấp.

### English
Not every app supports downgrade. Before updating, identify a supported older package, valid backup/snapshot, data restore method, or vendor-directed remediation. For database-backed applications, older binaries may not be compatible with an upgraded schema.

**Quy trình:** dừng rollout → xác định phạm vi ảnh hưởng → bảo toàn log → xin phê duyệt rollback → thực hiện phương án đã thử nghiệm → kiểm tra dữ liệu/chức năng → thông báo người dùng → phân tích nguyên nhân gốc.

**Process:** stop rollout → scope impact → preserve logs → obtain rollback approval → execute the tested plan → validate data/functionality → notify users → perform root-cause analysis.

## 10. Windows Update và ứng dụng bên thứ ba / Windows Update vs third-party apps

Windows Update chủ yếu quản lý cập nhật hệ điều hành và một số thành phần/driver theo cấu hình. Không mặc định rằng Windows Update sẽ cập nhật mọi ứng dụng bên thứ ba. Quản lý từng ứng dụng theo cơ chế được vendor và tổ chức hỗ trợ.

Windows Update primarily manages OS updates and selected components/drivers according to configuration. Do not assume it updates every third-party app. Manage each application through vendor- and organization-supported mechanisms.

## 11. Tình huống doanh nghiệp / Enterprise scenario

**Tình huống:** bản cập nhật ứng dụng POS khiến máy in hóa đơn không còn được nhận diện.

**Xử lý:** tạm dừng rollout; ghi nhận version ứng dụng, driver và Windows; kiểm tra release notes; thử tái hiện trên máy lab; xác minh kết nối, cổng in và service; dùng rollback được vendor hỗ trợ nếu cần; kiểm tra giao dịch thử và in thử trước khi đưa máy trở lại vận hành.

**Scenario:** a POS application update causes a receipt printer to disappear.

**Response:** pause rollout; record app, driver, and Windows versions; review release notes; reproduce in a lab; validate connectivity, printer port, and services; use vendor-supported rollback if needed; test a transaction and print before returning the terminal to service.

