# Windows Legacy BIOS/MBR – Legacy Boot and MBR Installation Guide

## 1. Introduction – Giới thiệu

### English

Legacy BIOS is a traditional firmware boot interface used by older computers and operating systems. It initializes hardware and transfers control to the operating system's boot code.

MBR (Master Boot Record) is an older disk partitioning scheme commonly used with Legacy BIOS boot. It stores partition table information and boot code in the first logical sector of a disk.

Legacy BIOS/MBR remains relevant for older computers, legacy operating systems, and specific environments that require backward compatibility.

However, for supported modern Windows deployments, UEFI/GPT is generally preferred because it supports modern firmware security features and larger, more flexible disk layouts.

### Tiếng Việt

Legacy BIOS là phương thức khởi động truyền thống được sử dụng trên máy tính và hệ điều hành đời cũ. Nó khởi tạo phần cứng và chuyển quyền điều khiển cho mã khởi động của hệ điều hành.

MBR (Master Boot Record) là chuẩn phân vùng ổ đĩa cũ thường được sử dụng cùng Legacy BIOS. MBR lưu thông tin bảng phân vùng và mã khởi động tại sector logic đầu tiên của ổ đĩa.

Legacy BIOS/MBR vẫn có ý nghĩa đối với máy tính cũ, hệ điều hành legacy và các môi trường cần duy trì khả năng tương thích ngược.

Tuy nhiên, với các hệ thống Windows hiện đại được hỗ trợ, UEFI/GPT thường là lựa chọn ưu tiên vì hỗ trợ các tính năng bảo mật firmware hiện đại và bố cục ổ đĩa linh hoạt hơn.

**Scope / Phạm vi:** This guide focuses on Legacy BIOS/MBR concepts, supported legacy Windows installation scenarios, disk verification, troubleshooting, and safe disk management.

Tài liệu tập trung vào khái niệm Legacy BIOS/MBR, các trường hợp cài Windows legacy được hỗ trợ, kiểm tra ổ đĩa, xử lý sự cố và quản lý ổ đĩa an toàn.

---

## 2. Legacy BIOS vs. MBR – Phân biệt Legacy BIOS và MBR

Legacy BIOS and MBR are related but different concepts.

Legacy BIOS và MBR có liên quan nhưng không phải cùng một khái niệm.

| Feature / Đặc điểm | Legacy BIOS | MBR |
|---|---|---|
| Type / Loại | Firmware boot interface | Disk partitioning scheme |
| Purpose / Chức năng | Initializes hardware and starts the boot process | Stores partition table entries and boot code |
| Main role / Vai trò chính | Firmware boot compatibility | Disk layout and partition identification |
| Common association / Liên hệ phổ biến | Commonly boots from MBR disks | Commonly used for Legacy BIOS boot |
| Main limitation / Hạn chế chính | Limited modern firmware security capabilities compared with UEFI | Limited partition entries and addressable disk capacity |

### English

A computer may contain UEFI firmware that supports Compatibility Support Module (CSM), allowing legacy boot on supported systems. The actual boot mode depends on firmware configuration and the selected boot entry.

Therefore, the presence of UEFI firmware does not automatically mean that Windows is currently booting in UEFI mode.

### Tiếng Việt

Một máy tính có thể sử dụng firmware UEFI hỗ trợ Compatibility Support Module (CSM), cho phép khởi động legacy trên các hệ thống tương thích. Chế độ boot thực tế phụ thuộc vào cấu hình firmware và mục boot được chọn.

Vì vậy, máy có firmware UEFI không có nghĩa Windows hiện đang khởi động theo UEFI.

---

## 3. MBR Characteristics – Đặc điểm của MBR

### 3.1 Partition limitations – Giới hạn phân vùng

**English**

The traditional MBR partition table supports up to four primary partition entries.

If more than four logical partitions are needed, one primary partition entry can be used for an extended partition containing logical drives.

MBR does not provide the same flexible partitioning capabilities as GPT.

**Tiếng Việt**

Bảng phân vùng MBR truyền thống hỗ trợ tối đa bốn mục phân vùng chính (primary partition entries).

Nếu cần nhiều hơn bốn phân vùng logic, một mục phân vùng chính có thể được dùng cho phân vùng mở rộng (extended partition), bên trong chứa các ổ logic (logical drives).

MBR không cung cấp khả năng phân vùng linh hoạt tương đương GPT.

### 3.2 Disk capacity limitation – Giới hạn dung lượng ổ đĩa

With conventional 512-byte logical sectors, MBR has an addressable disk-size limit of approximately 2 TiB.

Với sector logic 512 byte theo cách sử dụng truyền thống, MBR có giới hạn dung lượng địa chỉ hóa khoảng 2 TiB.

A disk larger than this limit may not be fully addressable through the traditional MBR layout. Actual behavior also depends on the storage device, controller, sector format, operating system, and driver support.

Ổ đĩa lớn hơn giới hạn này có thể không được địa chỉ hóa đầy đủ theo bố cục MBR truyền thống. Khả năng sử dụng thực tế còn phụ thuộc vào thiết bị lưu trữ, bộ điều khiển, định dạng sector, hệ điều hành và driver.

### 3.3 Boot process – Quy trình khởi động

**English**

In a typical Legacy BIOS/MBR Windows installation:

1. The firmware initializes the hardware.
2. The firmware executes the boot code from the selected boot device.
3. The boot code locates the active system partition and continues the boot process.
4. Windows Boot Manager and subsequent Windows boot components load the operating system.

The exact boot chain varies by operating system version and system configuration.

**Tiếng Việt**

Trong cấu hình Windows Legacy BIOS/MBR thông thường:

1. Firmware khởi tạo phần cứng.
2. Firmware thực thi mã khởi động từ thiết bị được chọn.
3. Mã khởi động xác định phân vùng hệ thống active và tiếp tục quá trình boot.
4. Windows Boot Manager cùng các thành phần khởi động tiếp theo tải hệ điều hành.

Chuỗi khởi động chính xác có thể thay đổi theo phiên bản hệ điều hành và cấu hình máy.

### 3.4 Secure Boot – Khởi động an toàn

**English**

Secure Boot is a UEFI firmware security feature. The traditional Legacy BIOS boot path does not provide UEFI Secure Boot functionality.

**Tiếng Việt**

Secure Boot là tính năng bảo mật của firmware UEFI. Đường khởi động Legacy BIOS truyền thống không cung cấp chức năng UEFI Secure Boot.

For Windows 11, Microsoft specifies UEFI firmware with Secure Boot capability and TPM 2.0 among the minimum system requirements. Legacy BIOS/MBR should not be treated as a standard Windows 11 deployment configuration.

Đối với Windows 11, Microsoft quy định firmware UEFI có khả năng hỗ trợ Secure Boot và TPM 2.0 trong các yêu cầu hệ thống tối thiểu. Không nên xem Legacy BIOS/MBR là cấu hình triển khai Windows 11 tiêu chuẩn.

Official reference:

https://learn.microsoft.com/en-us/windows/whats-new/windows-11-requirements

---

## 4. When to Use Legacy/MBR – Khi nào nên sử dụng Legacy/MBR?

### Appropriate scenarios – Trường hợp phù hợp

Consider Legacy BIOS/MBR when:

- The target computer only supports Legacy BIOS boot.
- A supported legacy operating system requires Legacy boot.
- An existing legacy application or hardware configuration depends on the current boot architecture.
- An organization must maintain a documented legacy environment for compatibility.

Tiếng Việt:

Cân nhắc Legacy BIOS/MBR khi:

- Máy tính đích chỉ hỗ trợ khởi động Legacy BIOS.
- Hệ điều hành legacy được hỗ trợ yêu cầu Legacy boot.
- Ứng dụng hoặc cấu hình phần cứng cũ phụ thuộc vào kiến trúc boot hiện tại.
- Tổ chức cần duy trì môi trường legacy có tài liệu và quy trình kiểm soát.

### When not to use it – Trường hợp không nên sử dụng

Avoid choosing Legacy/MBR merely out of habit when the computer supports UEFI/GPT and the target operating system supports the modern configuration.

Do not assume that every old Windows version, new computer, or Windows 11 installation supports Legacy/MBR.

Không nên chọn Legacy/MBR chỉ vì thói quen khi máy hỗ trợ UEFI/GPT và hệ điều hành đích hỗ trợ cấu hình hiện đại.

Không được mặc định mọi phiên bản Windows cũ, máy tính mới hoặc bản cài Windows 11 đều hỗ trợ Legacy/MBR.

---

## 5. Verify the Current Configuration – Kiểm tra cấu hình hiện tại

### 5.1 Check firmware boot mode – Kiểm tra chế độ boot

**English**

1. Press `Win + R`.
2. Enter `msinfo32`.
3. Press Enter.
4. Find **BIOS Mode**.
5. Record the displayed value.

**Tiếng Việt**

1. Nhấn `Win + R`.
2. Nhập `msinfo32`.
3. Nhấn Enter.
4. Tìm mục **BIOS Mode**.
5. Ghi nhận giá trị hiển thị.

| BIOS Mode | Meaning / Ý nghĩa |
|---|---|
| Legacy | Windows is currently booted using the legacy BIOS-compatible path. / Windows hiện đang khởi động theo đường Legacy. |
| UEFI | Windows is currently booted in UEFI mode. / Windows hiện đang khởi động theo UEFI. |

The BIOS Mode field describes the current Windows boot environment. It does not identify the partition style of every connected disk.

Mục BIOS Mode mô tả môi trường khởi động Windows hiện tại. Nó không xác định kiểu phân vùng của tất cả ổ đĩa được kết nối.

### 5.2 Check disk partition style – Kiểm tra kiểu phân vùng

Open PowerShell as Administrator:

```powershell
Get-Disk |
    Select-Object Number, FriendlyName, PartitionStyle, OperationalStatus, Size |
    Format-Table -AutoSize
```

Example output:

```text
Number FriendlyName    PartitionStyle OperationalStatus Size
------ ------------    -------------- ----------------- ----
0      SATA SSD        MBR            Online            ...
1      External HDD    GPT            Online            ...
```

The output is an example only. Actual disk names, numbers, styles, and sizes depend on the computer.

Đây chỉ là ví dụ. Tên, số thứ tự, kiểu phân vùng và dung lượng thực tế phụ thuộc vào máy tính.

Common `PartitionStyle` values:

- `MBR`: Master Boot Record.
- `GPT`: GUID Partition Table.
- `RAW`: Windows does not recognize a valid partition style for the disk; investigate before initializing or formatting it.

Các giá trị `PartitionStyle` thường gặp:

- `MBR`: ổ đĩa dùng chuẩn Master Boot Record.
- `GPT`: ổ đĩa dùng chuẩn GUID Partition Table.
- `RAW`: Windows chưa nhận diện được kiểu phân vùng hợp lệ; cần kiểm tra trước khi khởi tạo hoặc định dạng.

### 5.3 Inspect partitions – Kiểm tra các phân vùng

```powershell
Get-Partition |
    Select-Object DiskNumber, PartitionNumber, DriveLetter, Type, Size |
    Format-Table -AutoSize
```

To inspect one specific disk:

```powershell
Get-Partition -DiskNumber 0 |
    Format-Table PartitionNumber, DriveLetter, Type, Size -AutoSize
```

Replace `0` with the verified disk number.

Thay `0` bằng số ổ đĩa đã xác minh.

**Important:** Disk 0 is not necessarily the Windows system disk. Check the disk model, capacity, partition layout, and current Windows installation before making changes.

**Quan trọng:** Disk 0 không nhất thiết là ổ chứa Windows. Phải kiểm tra model, dung lượng, bố cục phân vùng và vị trí cài đặt Windows trước khi thay đổi.

---

## 6. Prepare Installation Media – Chuẩn bị USB cài Windows

### Requirements – Yêu cầu

- A compatible Windows installation image.
- A USB drive with sufficient capacity.
- A trusted media creation method.
- A target computer that supports the intended boot mode.
- A backup of important data.

Tiếng Việt:

- Bộ cài Windows tương thích.
- USB có dung lượng phù hợp.
- Phương pháp tạo bộ cài đáng tin cậy.
- Máy tính đích hỗ trợ chế độ boot cần sử dụng.
- Bản sao lưu dữ liệu quan trọng.

### Procedure – Quy trình

1. Download installation media from Microsoft or another authorized source.
2. Back up the USB's existing contents.
3. Create the installation media using a supported or trusted tool.
4. Confirm that the media and target firmware support the intended Legacy boot method.
5. Safely eject the USB.

Tiếng Việt:

1. Tải bộ cài từ Microsoft hoặc nguồn được ủy quyền.
2. Sao lưu dữ liệu hiện có trên USB.
3. Tạo bộ cài bằng công cụ được hỗ trợ hoặc đáng tin cậy.
4. Xác nhận bộ cài và firmware máy đích hỗ trợ phương thức Legacy boot cần dùng.
5. Tháo USB an toàn.

Creating installation media may erase the USB drive.

Quá trình tạo bộ cài có thể xóa dữ liệu trên USB.

Official Windows download resources:

- Windows 10: https://www.microsoft.com/software-download/windows10
- Windows 11: https://www.microsoft.com/software-download/windows11

Verify the support lifecycle and hardware requirements of the selected Windows version before installation.

Kiểm tra vòng đời hỗ trợ và yêu cầu phần cứng của phiên bản Windows được chọn trước khi cài đặt.

---

## 7. Configure Legacy Boot – Cấu hình Legacy Boot

### Procedure – Quy trình

1. Restart the computer.
2. Enter BIOS/UEFI Setup.
3. Locate the boot configuration menu.
4. Enable Legacy or CSM only if the firmware supports it and the use case requires it.
5. Open the one-time Boot Menu.
6. Select the USB entry that corresponds to Legacy boot, if separate entries are provided.
7. Save the configuration if required and restart.

Tiếng Việt:

1. Khởi động lại máy tính.
2. Vào BIOS/UEFI Setup.
3. Tìm menu cấu hình khởi động.
4. Chỉ bật Legacy hoặc CSM nếu firmware hỗ trợ và trường hợp sử dụng yêu cầu.
5. Mở Boot Menu một lần.
6. Chọn mục USB tương ứng với Legacy boot nếu có các mục riêng biệt.
7. Lưu cấu hình nếu cần và khởi động lại.

### Important considerations – Lưu ý quan trọng

- Firmware menus vary by manufacturer and model.
- Some modern computers do not provide Legacy/CSM support.
- Changing boot mode on an existing system can prevent Windows from starting.
- Changing firmware or TPM settings may trigger BitLocker recovery.

Tiếng Việt:

- Menu firmware khác nhau theo nhà sản xuất và model.
- Một số máy hiện đại không hỗ trợ Legacy/CSM.
- Thay đổi boot mode trên hệ thống hiện có có thể khiến Windows không khởi động.
- Thay đổi firmware hoặc thiết lập TPM có thể kích hoạt BitLocker Recovery.

Do not change the boot mode on a production system without documenting the current configuration and preparing a recovery plan.

Không thay đổi chế độ boot trên máy đang sử dụng thực tế nếu chưa ghi nhận cấu hình hiện tại và chuẩn bị phương án khôi phục.

---

## 8. Install Windows on an MBR Disk – Cài Windows trên ổ MBR

### 8.1 Standard installation – Cài đặt thông thường

This procedure is intended for a supported Windows version and a target computer that can boot the installer in Legacy mode.

Quy trình này dành cho phiên bản Windows được hỗ trợ và máy tính có thể khởi động bộ cài theo Legacy.

**English**

1. Boot the Windows installation USB in Legacy mode.
2. Start Windows Setup.
3. Select the language, time, and keyboard options.
4. Continue to the installation screen.
5. Select the appropriate Windows edition if prompted.
6. Choose the Custom installation option.
7. Identify the correct target disk and existing partitions.
8. Select the intended installation partition or prepare the disk for a clean installation.
9. Format or delete partitions only when a clean installation is intended and all required data has been backed up.
10. Complete Windows Setup.
11. Remove the installation USB when instructed or when the system restarts, and verify that the computer boots from its internal disk.

**Tiếng Việt**

1. Khởi động USB cài Windows theo Legacy.
2. Mở Windows Setup.
3. Chọn ngôn ngữ, thời gian và bàn phím.
4. Tiếp tục đến màn hình cài đặt.
5. Chọn đúng edition Windows nếu được yêu cầu.
6. Chọn phương án cài đặt Custom.
7. Xác định đúng ổ đĩa đích và các phân vùng hiện có.
8. Chọn phân vùng cài đặt hoặc chuẩn bị ổ đĩa cho cài mới hoàn toàn.
9. Chỉ format hoặc xóa phân vùng khi thực sự muốn cài mới và đã sao lưu toàn bộ dữ liệu cần giữ.
10. Hoàn tất Windows Setup.
11. Tháo USB khi được hướng dẫn hoặc khi máy khởi động lại, sau đó xác nhận máy boot từ ổ đĩa trong.

### 8.2 Partition layout – Bố cục phân vùng

A typical Legacy BIOS/MBR Windows installation may use:

| Partition | Purpose / Chức năng |
|---|---|
| System Reserved or system partition | Stores boot files and boot configuration. / Chứa tệp khởi động và cấu hình boot. |
| Windows partition | Stores Windows and installed applications. / Chứa Windows và ứng dụng đã cài. |
| Recovery partition, if present | Provides recovery functionality. / Hỗ trợ chức năng khôi phục nếu có. |
| Data partition, if configured | Stores user or business data. / Lưu dữ liệu cá nhân hoặc doanh nghiệp. |

Exact layouts vary by Windows version, installation method, and recovery requirements.

Bố cục chính xác phụ thuộc vào phiên bản Windows, phương pháp cài đặt và yêu cầu khôi phục.

### 8.3 Data protection – Bảo vệ dữ liệu

**Warning:** Deleting or formatting partitions can destroy data. Always verify the target disk and backup before making changes.

**Cảnh báo:** Xóa hoặc định dạng phân vùng có thể làm mất dữ liệu. Luôn xác minh ổ đĩa đích và sao lưu trước khi thay đổi.

Do not delete the System Reserved partition or other system partitions on an existing installation unless you understand their purpose and are intentionally rebuilding the boot configuration.

Không xóa phân vùng System Reserved hoặc các phân vùng hệ thống trên bản cài đặt hiện có nếu chưa hiểu chức năng và không có kế hoạch xây dựng lại cấu hình khởi động.

---

## 9. Convert GPT to MBR – Chuyển GPT sang MBR

### 9.1 Overview – Tổng quan

The DiskPart `convert mbr` command converts an empty basic disk from GPT to MBR. The disk must have no partitions or volumes before conversion.

Tiếng Việt:

Lệnh DiskPart `convert mbr` chuyển một ổ đĩa basic đang trống từ GPT sang MBR. Ổ đĩa phải không còn phân vùng hoặc volume trước khi chuyển đổi.

This is not a non-destructive conversion method for a disk containing data. Back up the required information and use a documented migration plan.

Đây không phải phương pháp chuyển đổi bảo toàn dữ liệu cho ổ đĩa đang chứa dữ liệu. Hãy sao lưu thông tin cần thiết và lập kế hoạch chuyển đổi rõ ràng.

Official reference:

https://learn.microsoft.com/en-us/windows-server/storage/disk-management/change-disk-partition-scheme

### 9.2 Destructive conversion procedure – Quy trình chuyển đổi có xóa dữ liệu

**Use this procedure only on a test disk or a disk that is authorized for complete erasure.**

**Chỉ sử dụng quy trình này trên ổ đĩa thử nghiệm hoặc ổ đĩa đã được cho phép xóa hoàn toàn.**

From an elevated Command Prompt or Windows Setup Command Prompt:

```text
diskpart
list disk
```

Review the disk list. Confirm the target by its capacity, model, and other available details.

Kiểm tra danh sách ổ đĩa. Xác nhận ổ đích dựa trên dung lượng, model và các thông tin khác.

Select and inspect the intended disk:

```text
select disk N
detail disk
```

Replace `N` with the verified disk number. Do not proceed unless the displayed disk is correct.

Thay `N` bằng số ổ đĩa đã xác minh. Không tiếp tục nếu thông tin hiển thị không đúng ổ cần xử lý.

Only after confirming that complete erasure is intended:

```text
clean
convert mbr
exit
```

Tiếng Việt:

- `clean`: xóa thông tin phân vùng trên ổ đĩa được chọn.
- `convert mbr`: chuyển ổ đĩa đã trống sang MBR.
- `exit`: thoát DiskPart.

**Critical warning:** These commands can make all existing volumes on the selected disk inaccessible. Do not execute them on the Windows system disk or a production data disk unless complete erasure is explicitly intended and authorized.

**Cảnh báo nghiêm trọng:** Các lệnh này có thể khiến tất cả volume hiện có trên ổ đĩa được chọn không còn truy cập được. Không chạy trên ổ hệ thống Windows hoặc ổ dữ liệu đang sử dụng nếu chưa có chủ đích và sự cho phép xóa sạch.

### 9.3 Convert using Disk Management – Chuyển đổi bằng Disk Management

Windows Disk Management can also convert a disk between GPT and MBR when the disk is eligible. Existing volumes must be removed before the conversion, so this approach is also destructive to the data on those volumes.

Tiếng Việt:

Windows Disk Management cũng có thể chuyển đổi giữa GPT và MBR khi ổ đĩa đáp ứng điều kiện. Các volume hiện có phải được xóa trước khi chuyển đổi, do đó phương pháp này cũng làm mất dữ liệu trong những volume đó.

For disks containing data that must be preserved, do not assume that a built-in conversion path exists for every scenario. Evaluate a supported migration or backup-and-restore approach.

Đối với ổ đĩa cần giữ nguyên dữ liệu, không nên mặc định mọi trường hợp đều có phương pháp chuyển đổi tích hợp bảo toàn dữ liệu. Hãy đánh giá phương án migration được hỗ trợ hoặc sao lưu và khôi phục.

---

## 10. Troubleshooting – Xử lý sự cố

| Problem / Lỗi | Possible cause / Nguyên nhân | Recommended action / Hướng xử lý |
|---|---|---|
| Legacy/CSM option is missing | Firmware does not support Legacy boot, or the option is hidden by configuration. | Check the manufacturer's documentation. Do not assume the feature can be enabled. |
| Windows Setup reports that the disk is not GPT | Installer booted in UEFI mode while the target disk uses MBR. | Verify the installer boot mode and target disk. Choose a supported installation path. |
| Windows Setup reports that the disk is not MBR | Installer booted in Legacy mode while the target disk uses GPT. | Verify firmware boot mode and disk style. Avoid deleting partitions until the intended configuration is confirmed. |
| USB is not detected | Unsupported boot mode, incorrectly created media, or firmware configuration. | Recreate the media if necessary and inspect firmware boot options. |
| Disk is missing from Windows Setup | Storage controller, driver, cable, or hardware issue. | Check firmware detection, connections, controller settings, and required drivers. |
| Disk capacity appears limited | MBR addressing limitations or storage/controller configuration. | Check disk style, sector format, controller, and operating system support. Consider GPT when supported. |
| System fails to boot after firmware changes | Boot mode mismatch or incorrect boot order. | Restore the documented previous configuration if safe, then diagnose the boot setup. |
| Windows starts from the wrong drive | Multiple bootable disks or incorrect boot priority. | Verify the boot order and identify the intended system disk. |

### Troubleshooting workflow – Quy trình xử lý sự cố

1. Record the exact error message.
2. Check the current `BIOS Mode` in `msinfo32`.
3. Inspect the disk style using `Get-Disk`.
4. Identify the correct system disk and installation target.
5. Verify the intended installer boot mode.
6. Check firmware, storage-controller settings, and drivers where relevant.
7. Back up data before destructive operations.
8. Apply one change at a time and test the result.
9. Document the root cause and final resolution.

Tiếng Việt:

1. Ghi nhận chính xác thông báo lỗi.
2. Kiểm tra `BIOS Mode` bằng `msinfo32`.
3. Kiểm tra kiểu phân vùng bằng `Get-Disk`.
4. Xác định đúng ổ hệ thống và ổ đĩa cài đặt.
5. Xác minh chế độ boot của bộ cài.
6. Kiểm tra firmware, bộ điều khiển lưu trữ và driver nếu liên quan.
7. Sao lưu dữ liệu trước thao tác phá hủy.
8. Mỗi lần chỉ thay đổi một yếu tố và kiểm tra kết quả.
9. Ghi lại nguyên nhân gốc và phương án xử lý cuối cùng.

**Do not format the disk immediately when an installation error appears. Diagnose the boot mode and partition style first.**

**Không định dạng ổ đĩa ngay khi xuất hiện lỗi cài đặt. Hãy kiểm tra chế độ boot và kiểu phân vùng trước.**

---

## 11. Best Practices – Thực hành tốt

### English

- Prefer UEFI/GPT for modern systems that support it.
- Use Legacy/MBR only when justified by compatibility requirements.
- Verify the current firmware mode and partition style separately.
- Confirm the disk identity before using DiskPart.
- Back up important data before changing partition schemes.
- Never run `clean` without confirming the target disk and the intention to erase it.
- Avoid changing firmware boot mode on an existing installation without a recovery plan.
- Verify that the operating system is supported on the target hardware.
- Document all changes and test the final boot process.

### Tiếng Việt

- Ưu tiên UEFI/GPT trên các hệ thống hiện đại có hỗ trợ.
- Chỉ sử dụng Legacy/MBR khi có yêu cầu tương thích rõ ràng.
- Kiểm tra riêng chế độ firmware và kiểu phân vùng.
- Xác nhận chính xác ổ đĩa trước khi dùng DiskPart.
- Sao lưu dữ liệu quan trọng trước khi thay đổi kiểu phân vùng.
- Không chạy `clean` nếu chưa xác nhận đúng ổ đĩa và chủ đích xóa dữ liệu.
- Không thay đổi chế độ boot trên hệ thống hiện có khi chưa có phương án khôi phục.
- Xác minh hệ điều hành được hỗ trợ trên phần cứng đích.
- Ghi lại mọi thay đổi và kiểm tra quá trình khởi động cuối cùng.

---

## 12. Practical Lab – Bài thực hành

### Lab objective – Mục tiêu

Practice inspecting firmware mode, identifying MBR/GPT disks, and planning a legacy installation without modifying a production system.

Thực hành kiểm tra chế độ firmware, nhận diện ổ MBR/GPT và lập kế hoạch cài đặt legacy mà không thay đổi hệ thống đang sử dụng thực tế.

### Task 1: Check the current boot mode

Open `msinfo32` and record the BIOS Mode value.

Mở `msinfo32` và ghi nhận giá trị BIOS Mode.

### Task 2: Inspect disk partition styles

Run:

```powershell
Get-Disk |
    Select-Object Number, FriendlyName, PartitionStyle, Size
```

Record the disk number, model, partition style, and capacity.

Ghi lại số ổ đĩa, model, kiểu phân vùng và dung lượng.

### Task 3: Inspect the partition layout

```powershell
Get-Partition |
    Select-Object DiskNumber, PartitionNumber, DriveLetter, Type, Size
```

Identify the Windows partition and any system or recovery partitions.

Xác định phân vùng Windows và các phân vùng hệ thống hoặc phục hồi.

### Task 4: Create an installation plan

Document:

- Target computer and Windows version.
- Whether Legacy boot is supported.
- Target disk identity and partition style.
- Required backup and recovery plan.
- Intended installation method.
- Expected partition layout.
- Post-installation checks.

Ghi lại thông tin máy đích, phiên bản Windows, khả năng hỗ trợ Legacy, ổ đĩa đích, phương án sao lưu, phương pháp cài đặt, bố cục phân vùng dự kiến và các bước kiểm tra sau cài đặt.

### Lab report template – Mẫu báo cáo

```text
Lab Name: Windows Legacy BIOS/MBR

Computer / VM:
Windows Version:
Firmware Mode:
Legacy/CSM Supported:
System Disk Number:
Disk Partition Style:
Disk Capacity:
Installation Method:
Backup Verified:
Issues Encountered:
Troubleshooting Steps:
Final Result:
Lessons Learned:
```

Do not run destructive DiskPart commands as part of this inspection lab. Use a disposable virtual disk for conversion exercises.

Không chạy các lệnh DiskPart phá hủy dữ liệu trong bài thực hành kiểm tra này. Hãy dùng ổ đĩa ảo có thể xóa bỏ để thực hành chuyển đổi.

---

## 13. References – Tài liệu tham khảo

1. **Microsoft Learn – Windows Setup: Installing using the MBR or GPT partition style**

   https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-setup-installing-using-the-mbr-or-gpt-partition-style

   Explains the relationship between installer boot mode and disk partition style.

2. **Microsoft Learn – Convert a disk to GPT or MBR**

   https://learn.microsoft.com/en-us/windows-server/storage/disk-management/change-disk-partition-scheme

   Describes disk conversion requirements and the need for an empty disk.

3. **Microsoft Learn – Windows 11 requirements**

   https://learn.microsoft.com/en-us/windows/whats-new/windows-11-requirements

   Documents Windows 11 hardware and firmware requirements.

4. **Microsoft Learn – Boot and install Windows**

   https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/boot-and-install-windows

   Provides Windows deployment and boot-mode guidance.

5. **Microsoft Learn – MBR2GPT**

   https://learn.microsoft.com/en-us/windows/deployment/mbr-to-gpt

   Documents Microsoft's supported MBR-to-GPT conversion utility for compatible Windows system disks.

---


**Disclaimer:** This document is a technical learning guide. Always verify hardware compatibility, operating system support, and disk identity before changing firmware or partition configuration.

**Lưu ý:** Đây là tài liệu học tập kỹ thuật. Luôn xác minh khả năng tương thích phần cứng, mức hỗ trợ hệ điều hành và danh tính ổ đĩa trước khi thay đổi firmware hoặc cấu hình phân vùng.

