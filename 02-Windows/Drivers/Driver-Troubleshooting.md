
# Driver Troubleshooting – Xử lý sự cố Driver

## 1. Purpose – Mục đích

**Tiếng Việt**

Tài liệu hướng dẫn quy trình kiểm tra và xử lý các sự cố driver thường gặp trên Windows. Mục tiêu là xác định nguyên nhân có căn cứ, khắc phục an toàn và ghi lại kết quả.

**English**

This document provides a systematic process for diagnosing and resolving common Windows driver problems. The goal is to identify evidence-based causes, apply safe fixes, and document the results.

## 2. Common Symptoms – Triệu chứng thường gặp

- Unknown device in Device Manager.
- Yellow warning icon.
- Device not detected.
- Network adapter missing.
- No sound output.
- Incorrect screen resolution.
- Printer not working.
- Bluetooth device cannot connect.
- Device stops working after an update.
- Blue screen or system instability associated with a driver.

Tiếng Việt:

- Xuất hiện Unknown device.
- Có biểu tượng chấm than vàng.
- Windows không nhận diện thiết bị.
- Mất card mạng trong Device Manager.
- Không có âm thanh.
- Độ phân giải màn hình không đúng.
- Máy in không hoạt động.
- Không kết nối được thiết bị Bluetooth.
- Thiết bị lỗi sau khi cập nhật driver.
- Màn hình xanh hoặc hệ thống không ổn định có liên quan đến driver.

## 3. Troubleshooting Workflow – Quy trình xử lý

### Step 1: Collect Information – Thu thập thông tin

Record:

- Computer and device model.
- Windows version and architecture.
- Device Manager status and error code.
- Driver provider and version.
- Recent updates or hardware changes.
- Exact error message.
- When the problem started.

Tiếng Việt: Ghi lại model máy, phiên bản Windows, mã lỗi, phiên bản driver, thay đổi gần đây, thông báo lỗi và thời điểm sự cố xuất hiện.

### Step 2: Check Device Manager

1. Open Device Manager.
2. Find the affected device.
3. Open Properties.
4. Review the General tab and device status.
5. Record any error code.
6. Review the Driver tab.

Tiếng Việt: Kiểm tra trạng thái thiết bị, mã lỗi và thông tin driver trước khi thay đổi cấu hình.

### Step 3: Check Windows Updates and Recent Changes

- Check whether Windows was recently updated.
- Review recent driver installations.
- Confirm whether the issue started after a hardware change.
- Review available manufacturer guidance.

Do not assume that every device error is caused by a driver.

Không mặc định mọi lỗi thiết bị đều do driver. Nguyên nhân cũng có thể đến từ phần cứng, cáp, nguồn điện, cấu hình hoặc dịch vụ hệ thống.

### Step 4: Apply the Least Risky Fix

Try appropriate actions in this order:

1. Check physical connections and power.
2. Restart the device or computer when appropriate.
3. Check whether the device is disabled.
4. Run the appropriate built-in troubleshooter if available.
5. Install a compatible official driver.
6. Roll back a recent driver update when justified.
7. Investigate hardware faults if the problem persists.

Tiếng Việt:

1. Kiểm tra kết nối vật lý và nguồn điện.
2. Khởi động lại thiết bị hoặc máy tính khi phù hợp.
3. Kiểm tra thiết bị có bị vô hiệu hóa hay không.
4. Chạy công cụ khắc phục sự cố phù hợp nếu có.
5. Cài driver chính thức tương thích.
6. Rollback nếu sự cố liên quan đến bản cập nhật gần đây.
7. Kiểm tra lỗi phần cứng nếu vẫn chưa khắc phục được.

## 4. Common Device Manager Error Codes – Mã lỗi thường gặp

| Code | Meaning | Initial action |
|---|---|---|
| Code 10 | Device cannot start. | Check the driver, device configuration, and hardware. |
| Code 28 | Drivers are not installed. | Install a compatible driver. |
| Code 31 | Windows cannot load the required drivers. | Review the driver package and related system information. |
| Code 43 | Windows has stopped the device because it reported problems. | Investigate the driver and possible hardware issues. |
| Code 45 | The device is not currently connected. | Check physical or logical connection. |

Tiếng Việt:

- Code 10: Thiết bị không thể khởi động.
- Code 28: Chưa cài driver cho thiết bị.
- Code 31: Windows không thể tải driver cần thiết.
- Code 43: Windows dừng thiết bị do thiết bị báo lỗi.
- Code 45: Thiết bị hiện không được kết nối.

Các mã lỗi chỉ là dấu hiệu định hướng, không khẳng định duy nhất một nguyên nhân.

## 5. Problem: Unknown Device – Lỗi thiết bị không xác định

### Possible causes – Nguyên nhân có thể

- Missing driver.
- Unsupported or unidentified hardware.
- Incorrect or incomplete driver package.
- Hardware not detected correctly.

### Resolution – Cách xử lý

1. Open Device Manager.
2. Right-click Unknown device.
3. Select Properties.
4. Open the Details tab.
5. Select Hardware Ids.
6. Record the displayed values.
7. Search the device or hardware ID through trusted manufacturer resources.
8. Install the correct driver.
9. Verify the result.

PowerShell alternative for listing devices with reported problems:

```powershell
Get-CimInstance Win32_PnPEntity |
    Where-Object { $_.ConfigManagerErrorCode -ne 0 } |
    Select-Object Name, PNPDeviceID, ConfigManagerErrorCode
```

Lưu ý: Lệnh liệt kê thiết bị có mã lỗi cấu hình khác 0; không phải mọi kết quả đều có nghĩa là thiếu driver.

## 6. Problem: Network Adapter Not Working – Lỗi card mạng

### Checklist

- [ ] Check Ethernet cable or Wi-Fi availability.
- [ ] Check whether the adapter appears in Device Manager.
- [ ] Check adapter status and error codes.
- [ ] Verify that the adapter is enabled.
- [ ] Check the installed network driver.
- [ ] Test with a known-good cable or access point when appropriate.
- [ ] Check IP configuration.
- [ ] Review recent driver changes.

Useful commands:

```cmd
ipconfig /all
ping 127.0.0.1
ping <default-gateway>
```

Replace `<default-gateway>` with the actual gateway address.

Tiếng Việt:

- `ipconfig /all`: Kiểm tra cấu hình IP, địa chỉ MAC và thông tin DHCP.
- `ping 127.0.0.1`: Kiểm tra ngăn xếp TCP/IP cục bộ.
- `ping <default-gateway>`: Kiểm tra khả năng kết nối tới gateway.

Nếu card mạng không xuất hiện trong Device Manager, cần kiểm tra thêm BIOS/UEFI, kết nối vật lý, phần cứng và khả năng nhận diện thiết bị.

## 7. Problem: Audio Not Working – Lỗi âm thanh

1. Check volume and mute settings.
2. Select the correct output device.
3. Check the audio device in Device Manager.
4. Review the driver status.
5. Run the available audio troubleshooter.
6. Install or reinstall a compatible official driver if necessary.
7. Test the speakers or headphones.

Tiếng Việt: Kiểm tra âm lượng, thiết bị đầu ra, trạng thái driver, công cụ sửa lỗi âm thanh và phần cứng trước khi cài lại driver.

## 8. Problem: Graphics Driver – Lỗi Driver VGA

Symptoms may include incorrect resolution, display glitches, application crashes, or driver resets.

Tiếng Việt: Triệu chứng có thể gồm sai độ phân giải, lỗi hiển thị, ứng dụng bị đóng hoặc driver bị khởi động lại.

Recommended actions:

1. Check the display cable and monitor.
2. Review Device Manager.
3. Record the graphics driver version.
4. Check the official OEM or GPU vendor support page.
5. Roll back if the issue began after a driver update.
6. Install a compatible driver if needed.
7. Test display resolution and graphics applications.

For laptops with switchable graphics, verify compatibility with the laptop manufacturer's recommended driver.

Đối với laptop sử dụng đồ họa tích hợp và rời, cần kiểm tra tính tương thích với driver được nhà sản xuất laptop khuyến nghị.

## 9. Problem: Printer Driver – Lỗi Driver máy in

1. Check printer power and connectivity.
2. Confirm the selected printer.
3. Check the print queue.
4. Review the printer status in Windows.
5. Verify the model and driver package.
6. Check the connection type and printer port.
7. Reinstall the appropriate driver if necessary.
8. Print a test page.

Tiếng Việt: Kiểm tra nguồn, kết nối, hàng đợi in, trạng thái máy in, đúng model, cổng kết nối và driver trước khi kết luận máy in hỏng.

## 10. Escalation – Khi nào cần chuyển cấp xử lý?

Escalate when:

- The issue persists after reasonable troubleshooting.
- Hardware failure is suspected.
- A critical business device is affected.
- A driver issue causes repeated blue screens.
- The required fix may affect many devices.
- Administrator privileges or vendor support are required.

Tiếng Việt: Chuyển cấp khi lỗi kéo dài, nghi hỏng phần cứng, ảnh hưởng thiết bị nghiệp vụ quan trọng, gây màn hình xanh lặp lại hoặc cần quyền và hỗ trợ chuyên sâu.

## 11. Incident Report Template – Mẫu báo cáo sự cố

```text
Ticket ID:
Date:
User / Department:
Computer Model:
Windows Version:
Device:
Problem Description:
Device Manager Error Code:
Driver Provider / Version:
Troubleshooting Steps:
Root Cause:
Resolution:
Verification Result:
Further Action:
Technician:
```

## 12. Best Practices – Thực hành tốt

- Record evidence before making changes.
- Change one variable at a time where practical.
- Use trusted driver sources.
- Avoid disabling security protections to force installation.
- Prepare a recovery plan before changing critical drivers.
- Verify the actual device function.
- Document unresolved issues and escalation details.

## 13. References – Tài liệu tham khảo

- Microsoft Support: https://support.microsoft.com/
- Microsoft Learn: https://learn.microsoft.com/
- Microsoft Update Catalog: https://www.catalog.update.microsoft.com/

