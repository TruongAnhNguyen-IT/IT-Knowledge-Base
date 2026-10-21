
# Windows USB Installation – Cài đặt Windows bằng USB

## 1. Purpose – Mục đích

**Tiếng Việt**

Hướng dẫn tạo USB cài Windows và sử dụng USB để cài đặt hệ điều hành trên máy tính vật lý.

**English**

This document explains how to create Windows installation media on a USB drive and use it to install the operating system on a physical computer.

## 2. Requirements – Yêu cầu

- A USB drive meeting the current requirements of the selected creation tool; an 8 GB or larger drive is commonly sufficient for Windows installation media.
- A working computer with internet access.
- An official Windows download or media creation tool.
- A compatible target computer.
- A backup of important data.
- A valid license appropriate for the Windows edition.

### Tiếng Việt

- USB đáp ứng yêu cầu của công cụ tạo bộ cài; USB từ 8 GB trở lên thường đủ cho bộ cài Windows.
- Máy tính có kết nối Internet.
- Bộ cài hoặc công cụ tạo phương tiện cài đặt chính thức.
- Máy tính mục tiêu tương thích.
- Bản sao lưu dữ liệu quan trọng.
- Giấy phép hợp lệ phù hợp với edition Windows.

**Warning / Cảnh báo:** Creating installation media may erase the USB drive. Back up all files on it first.

Tạo USB cài đặt có thể xóa dữ liệu trên USB. Hãy sao lưu trước khi thực hiện.

## 3. Download Windows – Tải Windows

1. Open the official Microsoft software download website.
2. Select the required Windows version.
3. Download the Media Creation Tool if offered for that version, or obtain the official ISO.
4. Review the system requirements.
5. Avoid modified or unofficial ISO files.

Official source:
https://www.microsoft.com/software-download/

Tiếng Việt:

1. Truy cập trang tải Windows chính thức của Microsoft.
2. Chọn phiên bản Windows cần cài.
3. Tải Media Creation Tool nếu phiên bản đó hỗ trợ, hoặc tải file ISO chính thức.
4. Kiểm tra yêu cầu hệ thống.
5. Tránh file ISO đã chỉnh sửa hoặc không rõ nguồn gốc.

## 4. Method A: Media Creation Tool

1. Connect the USB drive.
2. Run the official Media Creation Tool.
3. Accept the applicable license terms.
4. Choose the option to create installation media.
5. Select the language, edition, and architecture as required.
6. Select USB flash drive.
7. Choose the correct USB drive.
8. Confirm and wait for the process to finish.
9. Safely eject the USB drive.

### Tiếng Việt

1. Cắm USB vào máy.
2. Chạy công cụ Media Creation Tool chính thức.
3. Chấp nhận điều khoản sử dụng.
4. Chọn tạo phương tiện cài đặt.
5. Chọn ngôn ngữ, edition và kiến trúc phù hợp.
6. Chọn USB flash drive.
7. Xác nhận đúng USB.
8. Chờ hoàn tất.
9. Tháo USB an toàn.

The available options vary by Windows release and creation tool.

Các tùy chọn có thể khác nhau tùy phiên bản Windows và công cụ tạo bộ cài.

## 5. Method B: Using an Official ISO

1. Download the official ISO.
2. Verify the download if Microsoft provides a checksum.
3. Use a trusted tool to create bootable installation media.
4. Select the correct target USB drive.
5. Select a boot configuration compatible with the target computer.
6. Complete the process.
7. Test booting the USB on the target computer.

### Tiếng Việt

1. Tải file ISO chính thức.
2. Kiểm tra checksum nếu Microsoft cung cấp.
3. Sử dụng công cụ đáng tin cậy để tạo USB boot.
4. Chọn đúng USB đích.
5. Chọn cấu hình boot tương thích với máy tính.
6. Hoàn tất tạo USB.
7. Kiểm tra khả năng khởi động USB trên máy mục tiêu.

Note: Do not copy the ISO file onto a USB drive as an ordinary file and assume it will become bootable.

Lưu ý: Chỉ chép file ISO vào USB như một file thông thường không đồng nghĩa USB đã có khả năng boot.

## 6. Boot from USB – Khởi động từ USB

1. Shut down or restart the target computer.
2. Insert the installation USB.
3. Open the one-time boot menu or firmware setup.
4. Select the USB entry compatible with the intended boot mode.
5. Wait for Windows Setup to load.

The boot-menu key varies by manufacturer. Common keys include F12, F11, F9, Esc, or Del.

### Tiếng Việt

1. Tắt hoặc khởi động lại máy.
2. Cắm USB cài đặt.
3. Mở Boot Menu hoặc BIOS/UEFI.
4. Chọn mục USB phù hợp với chế độ boot.
5. Chờ Windows Setup tải lên.

Phím Boot Menu tùy nhà sản xuất; có thể gặp F12, F11, F9, Esc hoặc Del.

## 7. Windows Setup – Các bước cài đặt

1. Select language, time, and keyboard settings.
2. Start Windows Setup.
3. Select the appropriate installation option.
4. Enter a product key if required, or choose the applicable option to proceed without entering it immediately.
5. Select the correct Windows edition when prompted.
6. Accept the license terms.
7. Select the custom installation option for a clean installation.
8. Identify the correct target disk and partition.
9. Proceed only after verifying the disk selection.
10. Wait for Windows to copy files and restart.

### Tiếng Việt

1. Chọn ngôn ngữ, thời gian và bàn phím.
2. Khởi chạy Windows Setup.
3. Chọn phương án cài đặt phù hợp.
4. Nhập khóa sản phẩm nếu được yêu cầu, hoặc chọn phương án phù hợp để nhập sau.
5. Chọn đúng edition Windows khi được hỏi.
6. Chấp nhận điều khoản sử dụng.
7. Chọn cài đặt tùy chỉnh nếu muốn cài mới.
8. Xác định đúng ổ đĩa và phân vùng.
9. Chỉ tiếp tục sau khi xác nhận đúng ổ đĩa.
10. Chờ Windows sao chép file và khởi động lại.

**Critical warning:** Deleting or formatting partitions destroys data stored on those partitions. Never select a disk based only on its position in the list; verify its capacity and identity.

**Cảnh báo quan trọng:** Xóa hoặc format phân vùng sẽ làm mất dữ liệu trên phân vùng đó. Không chọn ổ đĩa chỉ dựa vào vị trí hiển thị; hãy kiểm tra dung lượng và nhận diện chính xác.

## 8. First Boot – Khởi động lần đầu

1. Follow the initial Windows setup.
2. Configure the region and keyboard.
3. Connect to a network when required or appropriate.
4. Configure the user account and security settings.
5. Review privacy settings.
6. Allow setup to complete.
7. Remove the USB after the initial installation phase when appropriate.
8. Ensure the computer boots from its internal drive.

### Tiếng Việt

Thực hiện cấu hình ban đầu, tài khoản, bảo mật và quyền riêng tư. Khi Windows hoàn tất quá trình cài đặt, đảm bảo máy khởi động từ ổ đĩa trong thay vì tiếp tục vào bộ cài USB.

## 9. Common Problems – Lỗi thường gặp

| Problem | Suggested action |
|---|---|
| USB is not detected | Try another port and check firmware boot options. |
| USB does not boot | Recreate the media and verify boot compatibility. |
| Disk is missing | Check storage configuration and required drivers. |
| GPT/MBR warning | Verify UEFI/Legacy mode and target disk layout. |
| Setup loops back to USB | Check boot order and remove USB at the appropriate stage. |
| Installation fails | Record the exact error and investigate its cause. |

## 10. Post-Installation Checklist – Checklist sau cài đặt

- [ ] Windows starts normally.
- [ ] Correct edition is installed.
- [ ] Activation status is checked.
- [ ] Drivers are installed.
- [ ] Windows Update is checked.
- [ ] Network connectivity works.
- [ ] Audio and display work.
- [ ] Storage devices are detected.
- [ ] Required applications are installed.
- [ ] User data is restored safely.

## 11. References – Tài liệu tham khảo

- Microsoft Windows downloads:
  https://www.microsoft.com/software-download/
- Microsoft Support:
  https://support.microsoft.com/windows

