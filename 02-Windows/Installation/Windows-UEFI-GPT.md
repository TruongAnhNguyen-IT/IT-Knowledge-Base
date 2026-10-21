
# Windows UEFI/GPT – Cài đặt Windows theo chuẩn UEFI/GPT

## 1. Introduction – Giới thiệu

### Tiếng Việt

UEFI là giao diện firmware hiện đại giúp máy tính khởi động hệ điều hành. GPT (GUID Partition Table) là chuẩn phân vùng ổ đĩa hiện đại, hỗ trợ nhiều phân vùng và ổ đĩa có dung lượng lớn.

Đối với phần lớn máy tính hiện đại, cài Windows theo UEFI/GPT là lựa chọn phù hợp.

### English

UEFI is a modern firmware interface used to start an operating system. GPT (GUID Partition Table) is a modern disk partitioning scheme that supports many partitions and large storage devices.

UEFI/GPT is the preferred configuration for most modern Windows computers.

## 2. UEFI vs. Legacy BIOS – So sánh

| Feature | UEFI | Legacy BIOS |
|---|---|---|
| Boot method | Modern firmware boot | Traditional firmware boot |
| Typical disk style | GPT | MBR |
| Secure Boot | Supported when configured | Not supported by the traditional legacy boot path |
| EFI System Partition | Required for standard UEFI Windows boot | Not used for legacy Windows boot |
| Typical use | Modern computers | Legacy compatibility |

Tiếng Việt: Với cài đặt Windows thông thường, chế độ boot UEFI cần đi cùng bố cục hệ thống phù hợp với GPT. Không nên chuyển chế độ boot tùy tiện trên máy đang có hệ điều hành.

## 3. Requirements – Yêu cầu

- A computer that supports UEFI.
- Compatible Windows installation media.
- A supported Windows version and edition.
- A target disk suitable for GPT.
- A backup of important data.
- Appropriate storage drivers if required.

### Tiếng Việt

- Máy tính hỗ trợ UEFI.
- USB cài Windows tương thích.
- Phiên bản Windows được hỗ trợ.
- Ổ đĩa đích phù hợp với GPT.
- Bản sao lưu dữ liệu quan trọng.
- Driver lưu trữ phù hợp nếu cần.

## 4. Verify Firmware Mode – Kiểm tra chế độ firmware

In an existing Windows installation:

1. Press `Win + R`.
2. Enter `msinfo32`.
3. Find BIOS Mode.
4. Review whether the current system uses UEFI or Legacy.

### Tiếng Việt

1. Nhấn `Win + R`.
2. Nhập `msinfo32`.
3. Tìm mục BIOS Mode.
4. Kiểm tra Windows đang chạy theo UEFI hay Legacy.

To inspect a disk's partition style, open PowerShell as Administrator:

```powershell
Get-Disk |
    Select-Object Number, FriendlyName, PartitionStyle, Size
```

The `PartitionStyle` field may report GPT, MBR, or RAW.

Lưu ý: BIOS Mode describes the current boot mode. PartitionStyle describes the selected disk's partition scheme. They are related but are not the same setting.

## 5. Configure UEFI – Cấu hình UEFI

1. Restart the computer.
2. Enter the firmware setup.
3. Locate boot configuration.
4. Select UEFI boot mode when appropriate.
5. Configure Secure Boot according to the device and operating system requirements.
6. Save changes and restart.

### Tiếng Việt

1. Khởi động lại máy.
2. Vào BIOS/UEFI Setup.
3. Tìm cấu hình khởi động.
4. Chọn chế độ UEFI khi phù hợp.
5. Cấu hình Secure Boot theo yêu cầu thiết bị và hệ điều hành.
6. Lưu cấu hình và khởi động lại.

Firmware menus differ by manufacturer. Do not disable security features without a clear reason.

Giao diện firmware khác nhau theo nhà sản xuất. Không vô hiệu hóa tính năng bảo mật khi chưa có lý do rõ ràng.

## 6. Clean Installation on a GPT Disk – Cài mới trên ổ GPT

For a new or intentionally erased target disk:

1. Boot the installation USB using its UEFI boot entry.
2. Start Windows Setup.
3. Select the appropriate Windows edition and installation option.
4. Review the listed disks and partitions.
5. If performing a clean installation, delete existing target-disk partitions only after verifying the disk and backup.
6. Select the resulting unallocated space.
7. Allow Windows Setup to create the required system partitions.
8. Complete the installation.

### Tiếng Việt

1. Khởi động USB bằng mục boot UEFI.
2. Khởi chạy Windows Setup.
3. Chọn đúng edition và phương án cài đặt.
4. Kiểm tra danh sách ổ đĩa và phân vùng.
5. Chỉ xóa phân vùng ổ đĩa đích khi đã xác nhận đúng ổ và sao lưu.
6. Chọn vùng Unallocated.
7. Để Windows Setup tự tạo các phân vùng hệ thống cần thiết.
8. Hoàn thành cài đặt.

**Critical warning:** Deleting partitions erases the data stored on them. Do not use this procedure on a disk that contains data you need to keep.

## 7. Convert MBR to GPT – Chuyển đổi MBR sang GPT

For supported existing Windows installations, Microsoft provides `MBR2GPT.exe` to convert a system disk from MBR to GPT under specific conditions.

This is different from erasing the disk during a clean installation.

### Tiếng Việt

Microsoft cung cấp công cụ `MBR2GPT.exe` để chuyển đổi ổ đĩa hệ thống từ MBR sang GPT trong những điều kiện nhất định. Công cụ này khác với thao tác xóa sạch ổ đĩa khi cài mới.

Before conversion:

- Verify the disk and operating system.
- Check the official prerequisites.
- Back up important data.
- Suspend BitLocker protection when required by the documented procedure.
- Prepare recovery media and a recovery key when applicable.
- Confirm that the firmware supports UEFI.
- Plan to switch the firmware boot configuration after a successful conversion.

### English

Before conversion, verify the target disk, supported configuration, recovery options, encryption status, and UEFI compatibility. Follow Microsoft's documented procedure and configure the firmware to boot in UEFI mode after conversion.

Official reference:
https://learn.microsoft.com/en-us/windows/deployment/mbr-to-gpt

## 8. Verify the Installation – Kiểm tra sau cài đặt

- [ ] `msinfo32` reports UEFI for BIOS Mode.
- [ ] The system disk uses GPT.
- [ ] Windows boots normally.
- [ ] Device Manager shows no unresolved critical device issues.
- [ ] Network and audio work.
- [ ] Windows activation is checked.
- [ ] Windows Update is checked.

## 9. Common Problems – Lỗi thường gặp

| Problem | Possible solution |
|---|---|
| Windows cannot install to an MBR disk when booted in UEFI mode | Verify the target disk and choose a supported GPT installation path. |
| USB does not boot in UEFI mode | Check the USB media and firmware boot menu. |
| Disk is not detected | Check storage configuration and required drivers. |
| System fails to boot after changing firmware mode | Restore the previous compatible setting and investigate the boot configuration. |
| Secure Boot warning | Verify firmware configuration and Windows requirements. |

## 10. References – Tài liệu tham khảo

- Microsoft MBR2GPT:
  https://learn.microsoft.com/en-us/windows/deployment/mbr-to-gpt
- Windows hardware requirements:
  https://www.microsoft.com/windows/windows-11-specifications

