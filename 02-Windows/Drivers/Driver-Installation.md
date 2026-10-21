
# Driver Installation – Cài đặt Driver

## 1. Purpose – Mục đích

**Tiếng Việt**

Tài liệu hướng dẫn quy trình cài đặt driver trên Windows, từ bước xác định thiết bị, tìm đúng gói cài đặt đến kiểm tra hoạt động sau khi cài.

**English**

This document describes the Windows driver installation process, from device identification and package selection to post-installation verification.

## 2. Before Installation – Trước khi cài đặt

Checklist:

- [ ] Identify the computer or device model.
- [ ] Check the Windows edition and version.
- [ ] Check the system architecture.
- [ ] Identify the device that needs a driver.
- [ ] Download the driver from a trusted source.
- [ ] Check compatibility and installation instructions.
- [ ] Back up important data or create a restore point when appropriate.
- [ ] Ensure administrator access is available.

Tiếng Việt:

- [ ] Xác định model máy tính hoặc thiết bị.
- [ ] Kiểm tra phiên bản và edition Windows.
- [ ] Kiểm tra kiến trúc hệ điều hành.
- [ ] Xác định thiết bị cần cài driver.
- [ ] Tải driver từ nguồn đáng tin cậy.
- [ ] Kiểm tra tính tương thích và hướng dẫn cài đặt.
- [ ] Sao lưu dữ liệu hoặc tạo điểm khôi phục khi phù hợp.
- [ ] Đảm bảo có quyền quản trị viên.

## 3. Method 1: Windows Update

### Steps – Các bước thực hiện

1. Open Settings.
2. Select Windows Update.
3. Check for updates.
4. Review available optional driver updates, if present.
5. Install appropriate updates.
6. Restart if requested.
7. Verify the device.

Tiếng Việt:

1. Mở Settings.
2. Chọn Windows Update.
3. Nhấn Check for updates.
4. Kiểm tra các bản cập nhật driver tùy chọn nếu có.
5. Cài đặt các bản phù hợp.
6. Khởi động lại nếu được yêu cầu.
7. Kiểm tra thiết bị.

Note: Optional driver updates may not be available on every system. Windows Update may not provide the newest or most suitable driver for every device.

Lưu ý: Không phải máy nào cũng có driver tùy chọn. Windows Update có thể không cung cấp phiên bản mới nhất hoặc phù hợp nhất cho mọi thiết bị.

## 4. Method 2: Manufacturer Installer

### Steps – Các bước thực hiện

1. Identify the exact device model.
2. Open the manufacturer's official support website.
3. Select the correct operating system.
4. Download the required driver package.
5. Verify the downloaded file and its source.
6. Run the installer with administrator privileges if required.
7. Follow the installation wizard.
8. Restart the computer if requested.
9. Verify the installed driver.

Tiếng Việt:

1. Xác định chính xác model thiết bị.
2. Truy cập trang hỗ trợ chính thức của nhà sản xuất.
3. Chọn đúng hệ điều hành.
4. Tải gói driver cần thiết.
5. Kiểm tra file và nguồn tải.
6. Chạy trình cài đặt bằng quyền quản trị viên nếu cần.
7. Làm theo hướng dẫn cài đặt.
8. Khởi động lại máy nếu được yêu cầu.
9. Kiểm tra driver sau khi cài.

## 5. Method 3: Device Manager

Use this method when a suitable driver package is already available locally.

### Steps – Các bước thực hiện

1. Open Device Manager.
2. Right-click the target device.
3. Select **Update driver**.
4. Select **Browse my computer for drivers**.
5. Choose the folder containing the extracted driver files.
6. Follow the instructions.
7. Verify the device status.

Tiếng Việt:

1. Mở Device Manager.
2. Nhấp phải thiết bị cần cài driver.
3. Chọn **Update driver**.
4. Chọn **Browse my computer for drivers**.
5. Chọn thư mục chứa driver đã giải nén.
6. Làm theo hướng dẫn.
7. Kiểm tra trạng thái thiết bị.

Important: The folder must contain a compatible driver package, commonly including an `.inf` file. Do not point Windows to an arbitrary folder.

Lưu ý: Thư mục phải chứa gói driver tương thích, thường có file `.inf`. Không chọn một thư mục bất kỳ.

## 6. Method 4: Install an INF Package

For a trusted, compatible driver package containing INF files, an administrator can use PnPUtil.

Example:

```cmd
pnputil /add-driver "C:\Drivers\Network\driver.inf" /install
```

Tiếng Việt:

- Mở Command Prompt bằng quyền Administrator.
- Thay đường dẫn ví dụ bằng đường dẫn thực tế.
- Đảm bảo INF thuộc đúng thiết bị và tương thích với Windows.
- Kiểm tra kết quả lệnh và trạng thái thiết bị.

English:

- Open Command Prompt as Administrator.
- Replace the example path with the actual path.
- Ensure the INF matches the device and Windows version.
- Review the command output and verify the device.

Note: PnPUtil does not guarantee that an arbitrary driver will be installed or become the active driver. Package compatibility and Windows driver ranking still apply.

## 7. Installation Verification – Kiểm tra sau cài đặt

- Open Device Manager.
- Confirm that the device is detected.
- Check for warning icons.
- Open Properties > Driver.
- Record the provider, version, and date.
- Test the device's actual function.

Examples:

| Device | Test |
|---|---|
| Network adapter | Check network connectivity. |
| Audio | Play sound and test the microphone. |
| Graphics | Check display resolution and graphics functions. |
| Printer | Print a test page. |
| Bluetooth | Test pairing with a known compatible device. |

Tiếng Việt:

- Mở Device Manager.
- Xác nhận thiết bị được nhận diện.
- Kiểm tra biểu tượng cảnh báo.
- Mở Properties > Driver.
- Ghi nhận nhà cung cấp, phiên bản và ngày driver.
- Kiểm tra chức năng thực tế của thiết bị.

## 8. Common Installation Problems – Lỗi thường gặp

| Problem | Suggested action |
|---|---|
| Incompatible driver | Verify model and OS compatibility. |
| Installer fails | Review the error message and installation logs. |
| Device remains unknown | Check hardware ID and vendor documentation. |
| Device still has a warning icon | Review Device Manager error code. |
| No network after installation | Check adapter status and consider rollback. |
| Restart required | Save work and restart as instructed. |

## 9. Best Practices – Thực hành tốt

- Do not install multiple driver packages blindly.
- Avoid unknown driver-updater tools.
- Keep a copy of the original installer when appropriate.
- Change one driver at a time when troubleshooting.
- Test the device before closing the support ticket.
- Document the resolution.

Không cài nhiều gói driver một cách tùy tiện. Khi xử lý sự cố, nên thay đổi từng driver một, kiểm tra kết quả và ghi lại phương án khắc phục.

## 10. References – Tài liệu tham khảo

- Microsoft Support: https://support.microsoft.com/
- Microsoft Learn: https://learn.microsoft.com/
- Microsoft Update Catalog: https://www.catalog.update.microsoft.com/

