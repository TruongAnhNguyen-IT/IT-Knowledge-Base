
# Driver Rollback – Quay lui phiên bản Driver

## 1. Purpose – Mục đích

**Tiếng Việt**

Driver Rollback là thao tác quay lại driver đã cài trước đó khi phiên bản mới gây lỗi, giảm hiệu năng hoặc làm thiết bị hoạt động không ổn định.

**English**

Driver rollback is the process of returning to a previously installed driver when a newer version causes errors, reduced performance, or device instability.

## 2. When to Roll Back – Khi nào cần Rollback?

Consider rolling back when:

- A problem begins immediately after a driver update.
- Network connectivity becomes unstable after updating the network driver.
- Audio stops working after an audio driver update.
- Graphics problems appear after installing a new graphics driver.
- A peripheral stops functioning after a driver change.

Tiếng Việt:

- Sự cố xuất hiện ngay sau khi cập nhật driver.
- Mạng không ổn định sau khi cập nhật driver mạng.
- Âm thanh bị mất sau khi cập nhật driver âm thanh.
- Lỗi hiển thị xuất hiện sau khi cập nhật driver đồ họa.
- Thiết bị ngoại vi không hoạt động sau khi thay đổi driver.

Important: Establish a reasonable link between the driver change and the issue before rolling back.

Lưu ý: Cần xác định mối liên hệ hợp lý giữa việc thay đổi driver và sự cố trước khi rollback.

## 3. Method 1: Roll Back Driver in Device Manager

### Steps – Các bước thực hiện

1. Press `Win + X`.
2. Select Device Manager.
3. Expand the relevant device category.
4. Right-click the affected device.
5. Select Properties.
6. Open the Driver tab.
7. Select Roll Back Driver if available.
8. Choose a reason if prompted.
9. Complete the process.
10. Restart if required.
11. Test the device.

Tiếng Việt:

1. Nhấn `Win + X`.
2. Chọn Device Manager.
3. Mở nhóm thiết bị liên quan.
4. Nhấp phải thiết bị đang gặp lỗi.
5. Chọn Properties.
6. Mở tab Driver.
7. Chọn Roll Back Driver nếu tùy chọn này khả dụng.
8. Chọn lý do nếu Windows yêu cầu.
9. Hoàn tất thao tác.
10. Khởi động lại nếu cần.
11. Kiểm tra thiết bị.

## 4. If Roll Back Driver Is Unavailable – Nếu không có nút Roll Back Driver

Possible reasons:

- Windows does not have a previous driver version available for rollback.
- The previous driver package is no longer available through the rollback mechanism.
- The current installation does not provide a usable rollback option.

Tiếng Việt:

Các nguyên nhân có thể gồm:
- Windows không còn phiên bản driver trước đó để quay lại.
- Gói driver cũ không còn khả dụng thông qua chức năng rollback.
- Hệ thống không cung cấp tùy chọn rollback có thể sử dụng.

Alternative procedure:

1. Identify the device model and Windows version.
2. Obtain a compatible previous driver from the official manufacturer.
3. Follow the manufacturer's downgrade or installation instructions.
4. If necessary, install the compatible package through Device Manager.
5. Verify the driver version and device operation.

Quy trình thay thế:

1. Xác định model thiết bị và phiên bản Windows.
2. Tìm phiên bản driver cũ tương thích từ nhà sản xuất.
3. Thực hiện theo hướng dẫn cài đặt hoặc hạ phiên bản của nhà sản xuất.
4. Nếu phù hợp, cài gói driver qua Device Manager.
5. Kiểm tra phiên bản driver và hoạt động của thiết bị.

Do not uninstall a critical driver without a recovery plan.

Không gỡ driver quan trọng nếu chưa có phương án khôi phục.

## 5. System Restore as an Alternative – Khôi phục hệ thống

If the problem affects multiple system components, System Restore may be appropriate when a suitable restore point exists.

Tiếng Việt:

Nếu sự cố ảnh hưởng đến nhiều thành phần hệ thống, có thể cân nhắc System Restore khi có điểm khôi phục phù hợp.

Steps:

1. Save your work.
2. Open the Windows recovery options.
3. Locate System Restore.
4. Select an appropriate restore point.
5. Review the affected programs and drivers.
6. Confirm the operation.
7. Test the system after restoration.

Lưu ý:
- System Restore is not the same as driver rollback.
- It may revert other system changes.
- It is not a substitute for a personal-data backup.
- Availability depends on system configuration and restore points.

## 6. Post-Rollback Verification – Kiểm tra sau Rollback

- [ ] Confirm the driver version.
- [ ] Check Device Manager for warnings.
- [ ] Reproduce the original issue and test whether it is resolved.
- [ ] Test related hardware and applications.
- [ ] Restart the computer if necessary.
- [ ] Document the outcome.

Tiếng Việt:

- [ ] Xác nhận phiên bản driver sau khi quay lui.
- [ ] Kiểm tra cảnh báo trong Device Manager.
- [ ] Kiểm tra lại lỗi ban đầu.
- [ ] Kiểm tra phần cứng và ứng dụng liên quan.
- [ ] Khởi động lại máy nếu cần.
- [ ] Ghi nhận kết quả xử lý.

## 7. Rollback Report Template – Mẫu báo cáo

```text
Issue:
Device:
Previous driver version:
New driver version:
Symptoms:
Rollback method:
Result:
Further action:
```

Bản dịch:

```text
Sự cố:
Thiết bị:
Phiên bản driver trước:
Phiên bản driver mới:
Triệu chứng:
Phương pháp rollback:
Kết quả:
Hành động tiếp theo:
```

## 8. References – Tài liệu tham khảo

- Microsoft Support: https://support.microsoft.com/
- Microsoft Learn: https://learn.microsoft.com/

