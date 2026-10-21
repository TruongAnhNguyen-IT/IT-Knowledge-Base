
# Driver Update – Cập nhật Driver

## 1. Purpose – Mục đích

**Tiếng Việt**

Cập nhật driver nhằm khắc phục lỗi, cải thiện tính tương thích, bổ sung chức năng hoặc giải quyết vấn đề hiệu năng và bảo mật khi nhà sản xuất có cung cấp bản cập nhật phù hợp.

**English**

Driver updates may fix bugs, improve compatibility, add functionality, or address performance and security issues when a suitable update is available from the manufacturer.

## 2. When Should Drivers Be Updated? – Khi nào nên cập nhật?

Consider updating when:

- A device is not functioning correctly.
- The manufacturer documents a fix for the reported problem.
- A new operating system version requires a compatible driver.
- A security advisory recommends an update.
- A supported feature requires a newer driver.

Tiếng Việt:

Nên cân nhắc cập nhật khi thiết bị gặp lỗi, nhà sản xuất đã sửa lỗi tương ứng, Windows cần driver tương thích, có khuyến nghị bảo mật hoặc cần sử dụng tính năng mới.

Không nhất thiết cập nhật mọi driver chỉ vì có phiên bản mới.

## 3. Identify the Current Driver – Xác định Driver hiện tại

1. Open Device Manager.
2. Expand the device category.
3. Right-click the device.
4. Select Properties.
5. Open the Driver tab.
6. Record Driver Provider, Driver Date, and Driver Version.

PowerShell example:

```powershell
Get-CimInstance Win32_PnPSignedDriver |
    Select-Object DeviceName, DriverProviderName, DriverVersion, DriverDate
```

Tiếng Việt: Ghi lại phiên bản driver hiện tại để so sánh sau khi cập nhật hoặc dùng làm thông tin xử lý sự cố.

## 4. Update Method 1: Windows Update

1. Open Settings.
2. Select Windows Update.
3. Check for updates.
4. Review optional updates if available.
5. Select appropriate driver updates.
6. Install and restart if required.
7. Verify device operation.

Tiếng Việt: Mở Settings > Windows Update, kiểm tra bản cập nhật, xem các driver tùy chọn nếu có, chọn bản phù hợp, cài đặt và kiểm tra thiết bị.

## 5. Update Method 2: Manufacturer Website

1. Identify the exact device model.
2. Visit the official support website.
3. Compare the available driver with the installed version.
4. Read the release notes.
5. Confirm operating system compatibility.
6. Download the official package.
7. Install according to the vendor's instructions.
8. Restart if required.
9. Test the device.

Tiếng Việt:

1. Xác định chính xác model thiết bị.
2. Truy cập website hỗ trợ chính thức.
3. So sánh driver có sẵn với phiên bản đang dùng.
4. Đọc thông tin phát hành.
5. Xác nhận tính tương thích với Windows.
6. Tải gói cài đặt chính thức.
7. Cài đặt theo hướng dẫn của nhà sản xuất.
8. Khởi động lại nếu cần.
9. Kiểm tra thiết bị.

## 6. Update Method 3: Device Manager

1. Open Device Manager.
2. Right-click the target device.
3. Select Update driver.
4. Choose Search automatically for drivers.
5. Follow the instructions.
6. Verify the result.

Tiếng Việt: Trong Device Manager, nhấp phải thiết bị, chọn Update driver > Search automatically for drivers và làm theo hướng dẫn.

Note: Automatic search may not find the latest driver available from the device manufacturer.

Lưu ý: Tìm kiếm tự động có thể không tìm được phiên bản mới nhất trên website của nhà sản xuất.

## 7. Before and After Checklist – Checklist trước và sau cập nhật

### Before – Trước khi cập nhật

- [ ] Confirm the reported problem.
- [ ] Record the current driver version.
- [ ] Check the release notes.
- [ ] Verify compatibility.
- [ ] Prepare a rollback or recovery plan.
- [ ] Back up important data when appropriate.

### After – Sau khi cập nhật

- [ ] Confirm the new driver version.
- [ ] Check Device Manager for warnings.
- [ ] Test the affected device.
- [ ] Check related applications and functions.
- [ ] Record the result.
- [ ] Roll back or troubleshoot if the issue becomes worse.

## 8. Common Risks – Rủi ro thường gặp

| Risk | Mitigation |
|---|---|
| Device becomes unstable | Use a compatible driver and prepare rollback. |
| Network disconnects | Have an alternative connection or offline installer. |
| Display problems | Keep the correct OEM graphics driver available. |
| New driver is incompatible | Verify model and OS support. |
| Performance becomes worse | Compare results and review release notes. |

Tiếng Việt: Trước khi cập nhật driver mạng hoặc đồ họa trên máy đang sử dụng để làm việc, hãy chuẩn bị phương án khôi phục phù hợp để tránh mất kết nối hoặc gián đoạn công việc.

## 9. Change Log Template – Mẫu ghi nhận thay đổi

| Field | Example |
|---|---|
| Date | 2026-10-21 |
| Device | Ethernet adapter |
| Previous version | Record actual version |
| New version | Record actual version |
| Reason | Intermittent disconnection |
| Result | Record test results |
| Technician | Record technician name |

The example is illustrative. Enter the actual device information and test results.

## 10. References – Tài liệu tham khảo

- Microsoft Support: https://support.microsoft.com/
- Microsoft Learn: https://learn.microsoft.com/
- Microsoft Update Catalog: https://www.catalog.update.microsoft.com/

