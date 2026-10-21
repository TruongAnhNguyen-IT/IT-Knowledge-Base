
# Driver Overview – Tổng quan về Driver

## 1. Introduction – Giới thiệu

**Tiếng Việt**

Driver (trình điều khiển thiết bị) là phần mềm trung gian giúp hệ điều hành giao tiếp với phần cứng. Driver cho phép Windows nhận diện, quản lý và sử dụng các thiết bị như card mạng, card đồ họa, máy in, âm thanh và chipset.

**English**

A device driver is software that allows an operating system to communicate with hardware. It enables Windows to recognize, manage, and use devices such as network adapters, graphics cards, printers, audio devices, and chipsets.

## 2. Functions of Drivers – Chức năng

- Nhận diện thiết bị phần cứng.
- Cho phép hệ điều hành điều khiển thiết bị.
- Cung cấp các chức năng phù hợp với phần cứng.
- Cải thiện tính ổn định, hiệu năng và khả năng tương thích.
- Khắc phục lỗi thiết bị thông qua các phiên bản driver mới.

English:
- Identify hardware devices.
- Allow the operating system to control hardware.
- Provide hardware-specific functionality.
- Improve stability, performance, and compatibility.
- Fix device issues through driver updates.

## 3. Common Driver Types – Các loại Driver phổ biến

| Driver | Chức năng |
|---|---|
| Chipset | Hỗ trợ giao tiếp giữa CPU, chipset và các thiết bị trên mainboard. |
| Graphics / VGA | Điều khiển GPU và các chức năng hiển thị. |
| Network / LAN | Hỗ trợ kết nối mạng Ethernet. |
| Wireless / Wi-Fi | Hỗ trợ kết nối mạng không dây. |
| Bluetooth | Quản lý kết nối Bluetooth. |
| Audio | Điều khiển âm thanh đầu vào và đầu ra. |
| Storage | Hỗ trợ bộ điều khiển và thiết bị lưu trữ. |
| Printer | Cho phép Windows giao tiếp với máy in. |
| Touchpad | Hỗ trợ thao tác trên bàn di chuột laptop. |
| USB | Hỗ trợ bộ điều khiển và thiết bị USB. |

English: Common driver categories include chipset, graphics, network, wireless, Bluetooth, audio, storage, printer, touchpad, and USB drivers.

## 4. Driver vs. Firmware vs. Application

| Component | Explanation |
|---|---|
| Driver | Software that enables the OS to communicate with hardware. |
| Firmware | Low-level software stored in a hardware device. |
| Application | Software that performs tasks for the user. |

Tiếng Việt:
- Driver: Phần mềm giúp hệ điều hành giao tiếp với phần cứng.
- Firmware: Phần mềm cấp thấp được lưu trong thiết bị.
- Application: Phần mềm phục vụ nhu cầu sử dụng của người dùng.

## 5. How to Check Drivers – Cách kiểm tra Driver

### Method 1: Device Manager

1. Press `Win + X`.
2. Select **Device Manager**.
3. Expand the relevant device category.
4. Right-click the device and select **Properties**.
5. Open the **Driver** tab.
6. Check the provider, date, version, and available actions.

Tiếng Việt:

1. Nhấn `Win + X`.
2. Chọn **Device Manager (Trình quản lý Thiết bị)**.
3. Mở nhóm thiết bị cần kiểm tra.
4. Nhấp phải thiết bị và chọn **Properties**.
5. Chọn tab **Driver**.
6. Kiểm tra nhà cung cấp, ngày phát hành, phiên bản và các tùy chọn có sẵn.

### Method 2: System Information

1. Press `Win + R`.
2. Enter `msinfo32`.
3. Review hardware resources and system components.

Lưu ý: `msinfo32` cung cấp thông tin phần cứng và hệ thống; Device Manager thường thuận tiện hơn để kiểm tra thuộc tính của từng driver.

### Method 3: PowerShell

Run PowerShell as Administrator:

```powershell
Get-CimInstance Win32_PnPSignedDriver |
    Select-Object DeviceName, DriverVersion, DriverDate, DriverProviderName
```

Lệnh hiển thị thông tin về các driver thiết bị Plug and Play đã ký mà Windows truy vấn được.

English: This command retrieves available Plug and Play driver information, including device name, version, date, and provider.

## 6. Device Manager Status – Trạng thái thiết bị

| Indicator | Meaning |
|---|---|
| No warning icon | No obvious Device Manager warning is shown. |
| Yellow warning icon | A device or driver problem may exist. |
| Unknown device | Windows cannot identify the device correctly. |
| Down-arrow icon | The device may be disabled. |

Tiếng Việt:
- Không có biểu tượng cảnh báo: Không thấy cảnh báo rõ ràng trong Device Manager.
- Dấu chấm than vàng: Có thể thiết bị hoặc driver đang gặp sự cố.
- Unknown device: Windows chưa nhận diện được thiết bị.
- Biểu tượng mũi tên xuống: Thiết bị có thể đang bị vô hiệu hóa.

Không có biểu tượng cảnh báo không đồng nghĩa driver chắc chắn hoạt động hoàn hảo.

## 7. Driver Sources – Nguồn tải Driver

Ưu tiên theo thứ tự:

1. Windows Update.
2. Trang hỗ trợ chính thức của nhà sản xuất laptop hoặc máy tính.
3. Trang hỗ trợ chính thức của nhà sản xuất mainboard hoặc thiết bị.
4. Công cụ cập nhật chính thức của nhà sản xuất.
5. Microsoft Update Catalog khi phù hợp.

Avoid unofficial driver-download websites and unknown driver-updater utilities.

Tiếng Việt: Không tải driver từ website không rõ nguồn gốc hoặc cài các công cụ cập nhật driver không đáng tin cậy.

## 8. Best Practices – Thực hành tốt

- Xác định đúng model thiết bị và phiên bản Windows.
- Kiểm tra kiến trúc hệ điều hành, chẳng hạn x64 hoặc ARM64.
- Ưu tiên driver có chữ ký số hợp lệ.
- Tạo điểm khôi phục khi phù hợp trước khi thay đổi lớn.
- Sao lưu driver quan trọng khi cần thiết.
- Chỉ cập nhật khi có lý do rõ ràng.
- Kiểm tra thiết bị sau khi cài đặt.
- Ghi lại phiên bản cũ và phiên bản mới.

English:
- Verify the device model and Windows version.
- Check the operating system architecture.
- Prefer properly signed drivers.
- Create a restore point when appropriate.
- Back up important drivers when needed.
- Update for a clear reason.
- Test the device after installation.
- Record the old and new versions.

## 9. References – Tài liệu tham khảo

- Microsoft Learn: https://learn.microsoft.com/
- Microsoft Support: https://support.microsoft.com/
- Microsoft Update Catalog: https://www.catalog.update.microsoft.com/

## 10. Disclaimer – Lưu ý

Driver availability and installation procedures vary by hardware model and Windows version. Always verify compatibility with the device manufacturer.

Khả năng hỗ trợ và quy trình cài đặt có thể khác nhau theo model phần cứng và phiên bản Windows. Luôn kiểm tra tính tương thích trước khi cài đặt.
