
# Windows Installation Overview – Tổng quan cài đặt Windows

## 1. Introduction – Giới thiệu

### Tiếng Việt

Cài đặt Windows là quá trình triển khai hệ điều hành lên máy tính để người dùng có thể sử dụng phần mềm, thiết bị ngoại vi và các chức năng của hệ thống.

Kỹ thuật viên IT Support cần hiểu quy trình chuẩn bị, lựa chọn phương pháp cài đặt, cấu hình phân vùng, cài driver, cập nhật hệ thống, kích hoạt Windows và kiểm tra sau cài đặt.

### English

Windows installation is the process of deploying the operating system onto a computer so users can access applications, peripherals, and system functionality.

An IT Support technician should understand preparation, installation methods, partitioning, driver installation, system updates, activation, and post-installation verification.

## 2. Windows Installation Methods – Các phương pháp cài đặt

| Method | Description |
|---|---|
| USB installation | Install Windows using bootable USB media. |
| In-place upgrade | Upgrade a supported existing Windows installation while retaining selected data and applications. |
| Reset this PC | Reinstall Windows using available recovery options. |
| Network deployment | Deploy Windows through an organization's network infrastructure. |
| Virtual machine installation | Install Windows in a virtualized environment for testing and learning. |

Tiếng Việt:

- Cài đặt bằng USB: Khởi động từ USB chứa bộ cài Windows.
- Nâng cấp tại chỗ: Nâng cấp hệ điều hành hiện có trong điều kiện được hỗ trợ.
- Reset this PC: Cài đặt lại Windows bằng tính năng khôi phục.
- Triển khai qua mạng: Cài đặt Windows theo hạ tầng của tổ chức.
- Máy ảo: Cài Windows để học tập, kiểm thử và thực hành.

## 3. Pre-Installation Checklist – Checklist trước khi cài

- [ ] Confirm the computer model and hardware specifications.
- [ ] Confirm the Windows edition and system requirements.
- [ ] Back up important files.
- [ ] Verify that the backup can be accessed.
- [ ] Record the existing Windows edition and activation status.
- [ ] Identify the storage device that will receive Windows.
- [ ] Check UEFI/BIOS settings.
- [ ] Confirm the installation media source.
- [ ] Prepare network, storage, and other required drivers.
- [ ] Check BitLocker or device encryption status.
- [ ] Ensure access to the recovery key if encryption is enabled.

### Tiếng Việt

- [ ] Kiểm tra model và cấu hình máy tính.
- [ ] Xác nhận phiên bản Windows và yêu cầu hệ thống.
- [ ] Sao lưu dữ liệu quan trọng.
- [ ] Kiểm tra khả năng truy cập bản sao lưu.
- [ ] Ghi lại edition và trạng thái kích hoạt Windows hiện tại.
- [ ] Xác định đúng ổ đĩa sẽ cài Windows.
- [ ] Kiểm tra cấu hình UEFI/BIOS.
- [ ] Xác minh nguồn bộ cài.
- [ ] Chuẩn bị driver mạng, lưu trữ và các driver cần thiết.
- [ ] Kiểm tra BitLocker hoặc mã hóa thiết bị.
- [ ] Chuẩn bị khóa khôi phục nếu đang bật mã hóa.

**Warning / Cảnh báo:** Installing Windows, deleting partitions, or formatting a disk may permanently destroy data. Verify the target disk and backup before proceeding.

Cài Windows, xóa phân vùng hoặc format ổ đĩa có thể làm mất dữ liệu vĩnh viễn. Luôn xác nhận đúng ổ đĩa và bản sao lưu trước khi thực hiện.

## 4. Hardware and Compatibility – Phần cứng và tương thích

Check the following:

- Processor compatibility.
- RAM capacity.
- Available storage space.
- UEFI firmware support.
- TPM and Secure Boot requirements when applicable.
- Network adapter support.
- Graphics and chipset drivers.

Tiếng Việt:

Kiểm tra CPU, RAM, dung lượng lưu trữ, hỗ trợ UEFI, yêu cầu TPM/Secure Boot khi áp dụng, card mạng và driver đồ họa/chipset.

For Windows 11, verify the current official system requirements. Do not assume every computer capable of running Windows 10 is eligible for Windows 11.

Đối với Windows 11, cần kiểm tra yêu cầu hệ thống chính thức hiện hành. Không mặc định máy chạy được Windows 10 sẽ đủ điều kiện cài Windows 11.

## 5. Installation Workflow – Quy trình cài đặt

1. Back up important data.
2. Prepare official installation media.
3. Configure the boot method.
4. Start Windows Setup.
5. Select language and keyboard settings.
6. Choose the appropriate installation option.
7. Select the target disk and partition.
8. Complete the installation.
9. Configure the initial Windows setup.
10. Install drivers and updates.
11. Verify activation.
12. Test system functionality.
13. Document the completed work.

### Tiếng Việt

1. Sao lưu dữ liệu.
2. Chuẩn bị bộ cài chính thức.
3. Cấu hình phương thức khởi động.
4. Khởi chạy Windows Setup.
5. Chọn ngôn ngữ và bàn phím.
6. Chọn phương án cài đặt phù hợp.
7. Chọn đúng ổ đĩa và phân vùng.
8. Hoàn thành cài đặt.
9. Thiết lập Windows lần đầu.
10. Cài driver và bản cập nhật.
11. Kiểm tra kích hoạt.
12. Kiểm tra chức năng hệ thống.
13. Ghi nhận công việc đã thực hiện.

## 6. Installation Types – Kiểu cài đặt

### Clean Installation

A clean installation installs Windows onto a selected target, usually after preparing or replacing the existing OS installation.

Cài mới là triển khai Windows lên ổ đĩa hoặc phân vùng được chọn. Nếu xóa hoặc format phân vùng, dữ liệu trên đó có thể bị mất.

### Upgrade Installation

An upgrade installation updates an existing Windows installation while preserving supported applications, settings, and files according to the selected upgrade path.

Nâng cấp giữ lại các thành phần được hỗ trợ theo đường dẫn nâng cấp. Cần kiểm tra tính tương thích và sao lưu trước khi thực hiện.

## 7. UEFI/GPT vs. Legacy BIOS/MBR

| Feature | UEFI/GPT | Legacy BIOS/MBR |
|---|---|---|
| Boot firmware | UEFI | Legacy BIOS or Compatibility Support Module |
| Typical system disk | GPT | MBR |
| Windows boot partition | EFI System Partition | Active system partition |
| Secure Boot | Supported when configured appropriately | Not supported in the traditional legacy boot path |
| Typical use | Modern systems | Older systems or specific legacy requirements |

Tiếng Việt:

- UEFI/GPT: Phù hợp với phần lớn máy tính hiện đại.
- Legacy BIOS/MBR: Thường dùng với máy cũ hoặc hệ thống cần tương thích legacy.
- Chế độ khởi động và kiểu phân vùng cần tương thích với nhau.

## 8. Common Installation Problems – Lỗi thường gặp

| Problem | Initial troubleshooting |
|---|---|
| USB does not boot | Check boot menu, USB media, and firmware mode. |
| Disk is not detected | Check storage controller, BIOS/UEFI, and required drivers. |
| GPT/MBR error | Verify boot mode and partition style. |
| Installation fails | Record the error code and inspect the relevant stage. |
| No network after installation | Check the network adapter and driver. |
| Activation fails | Verify edition, license, and activation status. |
| Repeated setup loop | Check boot order and installation media. |

## 9. Documentation Template – Mẫu ghi nhận

```text
Computer Model:
Serial Number:
Windows Edition:
Windows Version:
Installation Date:
Installation Method:
Boot Mode:
Partition Style:
Target Disk:
Driver Status:
Activation Status:
Windows Update Status:
Testing Result:
Technician:
Notes:
```

## 10. References – Tài liệu tham khảo

- Windows installation support:
  https://support.microsoft.com/windows
- Windows 11 specifications and requirements:
  https://www.microsoft.com/windows/windows-11-specifications
- Windows installation media:
  https://www.microsoft.com/software-download/

## 11. Disclaimer – Lưu ý

Always use legitimate installation media and a valid license. Procedures may differ depending on Windows edition, device model, firmware, and organizational policy.

Luôn sử dụng bộ cài hợp pháp và giấy phép phù hợp. Quy trình có thể khác nhau tùy phiên bản Windows, thiết bị, firmware và chính sách tổ chức.

