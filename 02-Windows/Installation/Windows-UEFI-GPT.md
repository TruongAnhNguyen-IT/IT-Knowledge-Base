# Windows UEFI/GPT – UEFI Boot and GPT Disk Installation Guide

## 1. Introduction – Giới thiệu

### English

UEFI (Unified Extensible Firmware Interface) is a firmware interface that initializes hardware and starts the operating system. It replaces the traditional BIOS boot process on modern computers.

GPT (GUID Partition Table) is a disk partitioning standard designed to support large storage devices, multiple partitions, and modern operating system deployment.

For a standard Windows installation that boots in UEFI mode, the disk containing the Windows operating system must use GPT.

This guide covers firmware verification, disk partition styles, Windows installation, MBR-to-GPT conversion, troubleshooting, and post-installation validation.

### Tiếng Việt

UEFI (Unified Extensible Firmware Interface) là giao diện firmware dùng để khởi tạo phần cứng và khởi động hệ điều hành. UEFI thay thế phương thức khởi động BIOS truyền thống trên các máy tính hiện đại.

GPT (GUID Partition Table) là chuẩn phân vùng ổ đĩa hỗ trợ thiết bị lưu trữ dung lượng lớn, nhiều phân vùng và triển khai hệ điều hành theo tiêu chuẩn hiện đại.

Đối với cài đặt Windows thông thường khởi động theo UEFI, ổ đĩa chứa hệ điều hành Windows phải sử dụng GPT.

Tài liệu này hướng dẫn kiểm tra firmware, kiểu phân vùng, cài đặt Windows, chuyển đổi MBR sang GPT, xử lý lỗi và xác minh sau cài đặt.

**Scope / Phạm vi:** Windows 10/11 on compatible hardware. Always verify the operating system's support status, edition requirements, and hardware compatibility before deployment.

---

## 2. UEFI vs. Legacy BIOS – So sánh chế độ khởi động

| Feature / Đặc điểm | UEFI | Legacy BIOS |
|---|---|---|
| Boot method / Phương thức boot | UEFI boot manager | Traditional BIOS boot |
| Typical system disk / Kiểu ổ hệ thống thường dùng | GPT | MBR |
| Secure Boot | Supported when configured and compatible | Not supported through the traditional Legacy boot path |
| System boot partition / Phân vùng khởi động | EFI System Partition (ESP) | Typically an active system partition |
| Partition limitations / Giới hạn phân vùng | Supports GPT's large disk and partition capabilities | MBR has legacy partition and disk-size limitations |
| Typical usage / Ứng dụng | Modern Windows deployments | Legacy compatibility |

### Important distinction – Phân biệt các khái niệm

- **UEFI/Legacy** describes the firmware boot mode.
- **GPT/MBR** describes the disk partitioning scheme.
- **Secure Boot** is a UEFI security feature that verifies trusted boot components.
- **ESP (EFI System Partition)** stores UEFI boot files.

Tiếng Việt:

- **UEFI/Legacy** là chế độ khởi động của firmware.
- **GPT/MBR** là kiểu bảng phân vùng của ổ đĩa.
- **Secure Boot** là tính năng bảo mật UEFI giúp xác minh các thành phần khởi động đáng tin cậy.
- **ESP (EFI System Partition)** là phân vùng chứa các tệp khởi động UEFI.

UEFI firmware may support a Compatibility Support Module (CSM) for legacy booting. Therefore, a computer with UEFI firmware does not necessarily mean its current Windows installation boots in UEFI mode.

Firmware UEFI có thể hỗ trợ Compatibility Support Module (CSM) để khởi động theo chế độ Legacy. Vì vậy, máy có firmware UEFI không đồng nghĩa với việc Windows hiện tại đang khởi động theo UEFI.

---

## 3. Requirements – Yêu cầu trước khi thực hiện

### Hardware requirements – Yêu cầu phần cứng

- A computer with UEFI firmware support.
- A compatible SSD or HDD.
- Sufficient disk capacity for Windows and required system partitions.
- Compatible storage controller configuration and drivers.

Tiếng Việt:

- Máy tính hỗ trợ firmware UEFI.
- Ổ SSD hoặc HDD tương thích.
- Dung lượng ổ đĩa đủ cho Windows và các phân vùng hệ thống.
- Cấu hình bộ điều khiển lưu trữ và driver tương thích.

### Software and preparation – Phần mềm và chuẩn bị

- An official or trusted Windows installation USB.
- A supported Windows version and compatible edition.
- A backup of important data.
- Device-specific drivers when required.
- BitLocker recovery key if device encryption is enabled.
- Administrator access when required.

Tiếng Việt:

- USB cài Windows từ nguồn chính thức hoặc đáng tin cậy.
- Phiên bản Windows được hỗ trợ và edition tương thích.
- Bản sao lưu dữ liệu quan trọng.
- Driver phù hợp với thiết bị nếu cần.
- Khóa khôi phục BitLocker nếu bật mã hóa thiết bị.
- Quyền quản trị khi cần thiết.

### Pre-installation checklist – Danh sách kiểm tra

- [ ] Confirm the correct target disk.
- [ ] Back up user files and important business data.
- [ ] Confirm Windows activation and license information when relevant.
- [ ] Check whether BitLocker or Device Encryption is enabled.
- [ ] Confirm that the firmware supports UEFI.
- [ ] Prepare network, storage, and other required drivers.
- [ ] Disconnect unnecessary external storage devices where practical.

**Warning:** Deleting partitions, cleaning a disk, or formatting a volume can permanently destroy data. Confirm the disk identity and backup before proceeding.

**Cảnh báo:** Xóa phân vùng, làm sạch ổ đĩa hoặc định dạng volume có thể khiến dữ liệu bị mất vĩnh viễn. Phải xác nhận đúng ổ đĩa và hoàn tất sao lưu trước khi thực hiện.

---

## 4. Verify Firmware Mode and Disk Style – Kiểm tra chế độ firmware và kiểu phân vùng

### 4.1 Check BIOS Mode using System Information

**English**

1. Press `Win + R`.
2. Enter `msinfo32`.
3. Press Enter.
4. Locate **BIOS Mode**.
5. Check the reported value.

**Tiếng Việt**

1. Nhấn `Win + R`.
2. Nhập `msinfo32`.
3. Nhấn Enter.
4. Tìm mục **BIOS Mode**.
5. Kiểm tra giá trị hiển thị.

Typical results:

| BIOS Mode | Meaning / Ý nghĩa |
|---|---|
| UEFI | Windows is currently booted in UEFI mode. / Windows hiện đang khởi động theo UEFI. |
| Legacy | Windows is currently booted in legacy BIOS compatibility mode. / Windows hiện đang khởi động theo Legacy. |

The `BIOS Mode` field does not report the partition style of every attached disk.

Mục `BIOS Mode` không cho biết kiểu phân vùng của tất cả ổ đĩa đang kết nối.

### 4.2 Check disk partition style using PowerShell

Open PowerShell as Administrator and run:

```powershell
Get-Disk |
    Select-Object Number, FriendlyName, PartitionStyle, OperationalStatus, Size |
    Format-Table -AutoSize
```

Example output:

```text
Number FriendlyName       PartitionStyle OperationalStatus Size
------ ------------       -------------- ----------------- ----
0      NVMe SSD           GPT            Online            ...
1      SATA HDD           MBR            Online            ...
```

The output above is illustrative; actual disk names, numbers, and sizes depend on the computer.

Tiếng Việt:

Lệnh trên liệt kê các ổ đĩa vật lý, tên thiết bị, kiểu phân vùng, trạng thái hoạt động và dung lượng.

- `GPT`: ổ đĩa sử dụng GPT.
- `MBR`: ổ đĩa sử dụng MBR.
- `RAW`: Windows chưa nhận diện được bảng phân vùng hợp lệ cho ổ đĩa đó; cần kiểm tra trước khi khởi tạo hoặc định dạng.
- `OperationalStatus`: trạng thái hoạt động mà Windows báo cáo.

**Important:** Disk number `0` is not guaranteed to be the Windows system disk. Identify the correct disk before making changes.

**Lưu ý:** Không được mặc định Disk 0 là ổ chứa Windows. Phải xác định chính xác ổ hệ thống trước khi thay đổi.

### 4.3 Inspect partitions using PowerShell

```powershell
Get-Partition |
    Select-Object DiskNumber, PartitionNumber, DriveLetter, Type, Size |
    Format-Table -AutoSize
```

To inspect a specific disk:

```powershell
Get-Partition -DiskNumber 0 |
    Format-Table PartitionNumber, DriveLetter, Type, Size -AutoSize
```

Replace `0` with the verified disk number.

Tiếng Việt:

Các lệnh này hiển thị danh sách phân vùng và thông tin liên quan. Chúng hữu ích khi xác định phân vùng Windows, phân vùng hệ thống EFI và các phân vùng phục hồi.

### 4.4 Check Secure Boot status

Run the following command in PowerShell:

```powershell
Confirm-SecureBootUEFI
```

Typical results:

- `True`: Secure Boot is enabled.
- `False`: Secure Boot is disabled.
- An error may indicate that the current environment does not support this query or that Windows is not running in a compatible UEFI environment.

Tiếng Việt:

- `True`: Secure Boot đang bật.
- `False`: Secure Boot đang tắt.
- Nếu xuất hiện lỗi, cần kiểm tra chế độ khởi động, firmware và quyền thực thi lệnh.

Do not assume that Secure Boot must be enabled on every device regardless of hardware, operating system, or deployment requirements. For compatible Windows 11 systems, check the applicable security and hardware requirements.

Không nên mặc định mọi thiết bị đều phải bật Secure Boot bất kể phần cứng và yêu cầu triển khai. Với máy tương thích Windows 11, cần kiểm tra các yêu cầu bảo mật và phần cứng tương ứng.

---

## 5. Configure UEFI Firmware – Cấu hình firmware UEFI

### Procedure – Quy trình

1. Restart the computer.
2. Enter UEFI Setup using the manufacturer's designated key or recovery menu.
3. Locate Boot Configuration or Boot Mode.
4. Select UEFI boot mode when appropriate.
5. Review CSM or Legacy Support settings.
6. Configure Secure Boot according to the device and operating system requirements.
7. Save changes and restart.
8. Confirm that the correct Windows Boot Manager or USB boot entry is available.

Tiếng Việt:

1. Khởi động lại máy tính.
2. Vào UEFI Setup bằng phím hoặc menu khôi phục của nhà sản xuất.
3. Tìm Boot Configuration hoặc Boot Mode.
4. Chọn UEFI khi phù hợp.
5. Kiểm tra CSM hoặc Legacy Support.
6. Cấu hình Secure Boot theo yêu cầu thiết bị và hệ điều hành.
7. Lưu cấu hình và khởi động lại.
8. Kiểm tra mục Windows Boot Manager hoặc mục boot USB phù hợp.

### Common firmware keys – Phím truy cập thường gặp

| Manufacturer / Nhà sản xuất | Common key / Phím thường gặp |
|---|---|
| Dell | F2 for Setup; F12 for Boot Menu |
| HP | Esc, then F10 for Setup; F9 for Boot Menu on many models |
| Lenovo | F1 or F2 on many models; some devices use a dedicated recovery button |
| ASUS | F2 or Del for Setup; boot-menu key varies by model |
| Acer | F2 for Setup; F12 for Boot Menu on supported models |
| MSI | Del for Setup; F11 for Boot Menu on many models |

Keys vary by model and firmware version. Consult the manufacturer's documentation.

Phím truy cập thay đổi tùy model và phiên bản firmware. Hãy kiểm tra tài liệu của nhà sản xuất.

**Caution:** Changing the boot mode on an existing Windows installation may make the operating system unbootable. Changing Secure Boot or TPM-related settings may also trigger BitLocker recovery.

**Thận trọng:** Thay đổi chế độ boot trên Windows hiện có có thể khiến hệ điều hành không khởi động được. Thay đổi Secure Boot hoặc thiết lập liên quan đến TPM cũng có thể kích hoạt yêu cầu khôi phục BitLocker.

---

## 6. Create Windows Installation Media – Tạo USB cài Windows

### Recommended method – Phương pháp khuyến nghị

Use Microsoft's official Windows installation media creation instructions or an official Windows ISO.

Reference:

- Windows 11 download: https://www.microsoft.com/software-download/windows11
- Windows 10 download and lifecycle information: https://www.microsoft.com/software-download/windows10

### Procedure – Quy trình

1. Prepare a USB drive with sufficient capacity for the selected installation media.
2. Back up the USB's existing contents.
3. Use Microsoft's supported media creation method or a trusted ISO-writing utility.
4. Complete the media creation process.
5. Safely eject the USB drive.

Tiếng Việt:

1. Chuẩn bị USB có dung lượng phù hợp.
2. Sao lưu dữ liệu đang có trên USB.
3. Sử dụng công cụ tạo bộ cài được Microsoft hỗ trợ hoặc công cụ ghi ISO đáng tin cậy.
4. Hoàn tất quá trình tạo bộ cài.
5. Tháo USB an toàn.

Creating installation media may erase the USB's existing data.

Quá trình tạo bộ cài có thể xóa dữ liệu đang lưu trên USB.

### Boot the USB in UEFI mode – Khởi động USB theo UEFI

1. Connect the installation USB.
2. Restart the computer.
3. Open the one-time Boot Menu.
4. Select the USB entry identified as UEFI when the firmware provides separate boot entries.
5. Confirm that Windows Setup starts.

Tiếng Việt:

1. Cắm USB cài Windows.
2. Khởi động lại máy.
3. Mở Boot Menu.
4. Chọn mục USB có nhãn UEFI nếu firmware cung cấp các lựa chọn riêng biệt.
5. Xác nhận Windows Setup khởi chạy.

**Important:** A USB device appearing in the Boot Menu does not, by itself, prove that Windows Setup was started in UEFI mode. If necessary, verify the current environment before changing the target disk.

**Lưu ý:** USB xuất hiện trong Boot Menu không tự động chứng minh Windows Setup đã khởi động theo UEFI. Nếu cần, hãy kiểm tra môi trường khởi động trước khi thay đổi ổ đĩa đích.

---

## 7. Clean Installation on a GPT Disk – Cài mới Windows trên ổ GPT

### 7.1 Standard installation method – Phương pháp cài đặt thông thường

This procedure is for a new disk or a disk that has been intentionally selected for a clean installation.

**English**

1. Boot the installation USB in UEFI mode.
2. Start Windows Setup.
3. Select the language, time, and keyboard options.
4. Continue to the installation screen.
5. Select the appropriate Windows edition if prompted.
6. Choose the Custom installation option.
7. Identify the correct target disk.
8. If a clean installation is intended, delete the existing partitions on that target disk only after confirming the backup and disk identity.
9. Select the resulting unallocated space.
10. Continue with installation and allow Windows Setup to create the required partitions.
11. Complete the initial Windows configuration.

**Tiếng Việt**

1. Khởi động USB cài đặt theo UEFI.
2. Khởi chạy Windows Setup.
3. Chọn ngôn ngữ, thời gian và bàn phím.
4. Tiếp tục đến màn hình cài đặt.
5. Chọn đúng edition Windows nếu được yêu cầu.
6. Chọn phương án cài đặt Custom.
7. Xác định chính xác ổ đĩa đích.
8. Nếu cài mới hoàn toàn, chỉ xóa các phân vùng trên ổ đích sau khi xác nhận đã sao lưu và chọn đúng ổ.
9. Chọn vùng Unallocated sau khi xóa phân vùng.
10. Tiếp tục và để Windows Setup tự tạo các phân vùng cần thiết.
11. Hoàn thành cấu hình Windows ban đầu.

### 7.2 Expected UEFI/GPT partition layout – Bố cục phân vùng dự kiến

A typical Windows UEFI installation includes:

| Partition | Purpose / Chức năng |
|---|---|
| EFI System Partition (ESP) | Stores UEFI boot files. / Chứa tệp khởi động UEFI. |
| Microsoft Reserved (MSR) | Reserved for Windows partition management. / Dành cho quản lý phân vùng Windows. |
| Windows partition | Stores the operating system and applications. / Chứa hệ điều hành và ứng dụng. |
| Windows Recovery partition | Supports Windows recovery tools. / Hỗ trợ công cụ khôi phục Windows. |

Exact sizes and layout may vary by Windows version, deployment method, disk sector format, and recovery requirements. Let Windows Setup manage the standard layout unless a documented deployment requirement calls for a custom layout.

Kích thước và bố cục có thể thay đổi theo phiên bản Windows, phương pháp triển khai, định dạng sector và yêu cầu phục hồi. Hãy để Windows Setup tự quản lý bố cục tiêu chuẩn, trừ khi có yêu cầu triển khai riêng đã được xác định.

### 7.3 Alternative: manually convert a blank target disk using DiskPart

**Warning:** The `clean` command removes the selected disk's partition information. All existing volumes on the selected disk can become inaccessible. Use this method only when the target disk is intentionally being erased.

**Cảnh báo:** Lệnh `clean` xóa thông tin phân vùng của ổ đĩa được chọn. Các volume hiện có có thể không còn truy cập được. Chỉ dùng phương pháp này khi chủ động xóa ổ đĩa đích.

From Windows Setup, press `Shift + F10` to open Command Prompt, then:

```text
diskpart
list disk
```

Inspect the disk list and confirm the target disk by its size and other available information.

Kiểm tra danh sách ổ đĩa, đối chiếu dung lượng và các thông tin có sẵn để xác nhận đúng ổ đích.

Only after confirming the disk:

```text
select disk N
detail disk
```

Replace `N` with the verified disk number. Review the details again before continuing.

Chỉ sau khi xác nhận chính xác ổ đĩa:

```text
clean
convert gpt
exit
```

Return to Windows Setup, refresh the disk list if necessary, select the target disk's unallocated space, and continue installation.

Quay lại Windows Setup, làm mới danh sách ổ đĩa nếu cần, chọn vùng Unallocated của ổ đích và tiếp tục cài đặt.

**Never copy and run the destructive commands blindly.** Do not select a disk based only on its number.

**Không sao chép và chạy các lệnh phá hủy dữ liệu một cách máy móc.** Không chọn ổ đĩa chỉ dựa trên số thứ tự.

---

## 8. Convert MBR to GPT Using MBR2GPT – Chuyển đổi MBR sang GPT

### 8.1 Overview – Tổng quan

`MBR2GPT.exe` is a Microsoft utility for converting a supported Windows system disk from MBR to GPT without intentionally deleting the data stored on its partitions.

It is designed for supported system-disk conversion scenarios, not for converting arbitrary non-system data disks.

Tiếng Việt:

`MBR2GPT.exe` là công cụ của Microsoft dùng để chuyển đổi ổ đĩa hệ thống Windows đủ điều kiện từ MBR sang GPT mà không chủ đích xóa dữ liệu trong các phân vùng.

Công cụ này được thiết kế cho các trường hợp chuyển đổi ổ đĩa hệ thống được hỗ trợ, không phải công cụ chuyển đổi tùy ý mọi ổ dữ liệu.

Official documentation:

https://learn.microsoft.com/en-us/windows/deployment/mbr-to-gpt

### 8.2 Important prerequisites – Điều kiện quan trọng

Before conversion, verify that:

- The target is the correct Windows system disk.
- The disk currently uses MBR.
- The disk layout meets the tool's validation requirements.
- The firmware supports UEFI boot.
- The current Windows installation is supported by the conversion procedure.
- Important data has been backed up.
- BitLocker protection has been handled according to Microsoft's instructions.
- A recovery key and recovery media are available when applicable.

Tiếng Việt:

Trước khi chuyển đổi, cần xác nhận:

- Đã chọn đúng ổ đĩa hệ thống Windows.
- Ổ đĩa hiện sử dụng MBR.
- Bố cục phân vùng đáp ứng điều kiện kiểm tra của công cụ.
- Firmware hỗ trợ khởi động UEFI.
- Windows hiện tại thuộc trường hợp được quy trình chuyển đổi hỗ trợ.
- Dữ liệu quan trọng đã được sao lưu.
- BitLocker được xử lý theo hướng dẫn của Microsoft.
- Có khóa khôi phục và phương tiện cứu hộ khi cần.

Typical layout requirements include no more than three primary MBR partitions, no extended or logical partitions, and a valid boot configuration. Other validation requirements also apply.

Điều kiện bố cục thường bao gồm không quá ba phân vùng primary MBR, không có phân vùng extended/logical và cấu hình khởi động hợp lệ. Các điều kiện kiểm tra khác cũng được áp dụng.

### 8.3 Step 1: Identify the Windows system disk

Run PowerShell as Administrator:

```powershell
Get-Disk |
    Select-Object Number, FriendlyName, PartitionStyle, Size |
    Format-Table -AutoSize
```

Confirm which disk contains the current Windows installation before using `MBR2GPT`.

Xác nhận ổ đĩa chứa Windows hiện tại trước khi sử dụng `MBR2GPT`.

### 8.4 Step 2: Validate the disk

Open Command Prompt as Administrator.

Run:

```cmd
mbr2gpt /validate /disk:N /allowFullOS
```

Replace `N` with the verified system disk number.

Example for a system disk confirmed to be Disk 0:

```cmd
mbr2gpt /validate /disk:0 /allowFullOS
```

The validation operation checks whether the disk meets the conversion requirements. Do not proceed if validation fails.

Lệnh kiểm tra xem ổ đĩa có đáp ứng các điều kiện chuyển đổi hay không. Không tiếp tục nếu bước kiểm tra thất bại.

### 8.5 Step 3: Convert the disk

Only after successful validation, a completed backup, and preparation for recovery, run:

```cmd
mbr2gpt /convert /disk:N /allowFullOS
```

Replace `N` with the verified disk number.

This command performs the conversion. Although the tool is designed to preserve existing partition data, conversion is a system-level operation and should never be treated as risk-free.

Lệnh này thực hiện chuyển đổi. Mặc dù công cụ được thiết kế để giữ dữ liệu trong các phân vùng, đây vẫn là thao tác cấp hệ thống và không được xem là hoàn toàn không có rủi ro.

### 8.6 Step 4: Configure UEFI boot after conversion

After successful conversion:

1. Restart the computer.
2. Enter firmware setup.
3. Change the boot configuration to UEFI mode.
4. Disable legacy/CSM boot where required by the device configuration.
5. Select Windows Boot Manager when available.
6. Save the configuration and restart.
7. Verify that Windows starts successfully.

Tiếng Việt:

1. Khởi động lại máy.
2. Vào firmware setup.
3. Chuyển cấu hình khởi động sang UEFI.
4. Tắt Legacy/CSM nếu cấu hình thiết bị yêu cầu.
5. Chọn Windows Boot Manager nếu có.
6. Lưu cấu hình và khởi động lại.
7. Xác nhận Windows khởi động thành công.

Do not change firmware settings prematurely. Follow the documented conversion workflow and be prepared to troubleshoot boot configuration issues.

Không thay đổi firmware quá sớm. Hãy thực hiện theo quy trình chuyển đổi đã được hướng dẫn và chuẩn bị phương án xử lý nếu gặp lỗi khởi động.

---

## 9. Verification After Installation – Kiểm tra sau cài đặt

### 9.1 Verify firmware mode

Open `msinfo32` and check:

- `BIOS Mode`: UEFI.
- `Secure Boot State`: review the reported state when supported and applicable.

Tiếng Việt:

Mở `msinfo32` và kiểm tra:

- `BIOS Mode`: UEFI.
- `Secure Boot State`: xem trạng thái được báo cáo nếu thiết bị hỗ trợ và phù hợp.

### 9.2 Verify the system disk

Run PowerShell:

```powershell
Get-Disk |
    Select-Object Number, FriendlyName, PartitionStyle, OperationalStatus |
    Format-Table -AutoSize
```

Confirm that the disk containing the Windows installation uses GPT.

Xác nhận ổ đĩa chứa Windows sử dụng GPT.

### 9.3 Verify Windows system and devices

- [ ] Windows starts normally after restart.
- [ ] BIOS Mode reports UEFI.
- [ ] The Windows system disk uses GPT.
- [ ] Windows Boot Manager is available in firmware where expected.
- [ ] Device Manager has no unresolved critical device issues.
- [ ] Network connectivity works.
- [ ] Audio and display function correctly.
- [ ] Storage devices are detected correctly.
- [ ] Windows activation status is checked.
- [ ] Windows Update is reviewed.
- [ ] BitLocker status and recovery information are checked when applicable.

Tiếng Việt:

- [ ] Windows khởi động bình thường sau khi restart.
- [ ] BIOS Mode hiển thị UEFI.
- [ ] Ổ đĩa hệ thống Windows sử dụng GPT.
- [ ] Windows Boot Manager xuất hiện trong firmware khi phù hợp.
- [ ] Device Manager không còn lỗi thiết bị nghiêm trọng chưa xử lý.
- [ ] Kết nối mạng hoạt động.
- [ ] Âm thanh và màn hình hoạt động bình thường.
- [ ] Các thiết bị lưu trữ được nhận diện đúng.
- [ ] Đã kiểm tra trạng thái kích hoạt Windows.
- [ ] Đã kiểm tra Windows Update.
- [ ] Đã kiểm tra trạng thái BitLocker và thông tin khôi phục khi cần.

---

## 10. Common Problems and Troubleshooting – Lỗi thường gặp và cách xử lý

| Problem / Lỗi | Possible cause / Nguyên nhân có thể | Recommended action / Hướng xử lý |
|---|---|---|
| Windows cannot be installed to this disk because it is not GPT | Setup booted in UEFI mode, but the target disk uses MBR. | Verify the target disk. Use a supported GPT clean-install path or validate MBR2GPT conversion eligibility. |
| USB does not boot in UEFI mode | Incorrect boot entry, incompatible media, or firmware configuration. | Recreate the installation media if needed and select the correct UEFI USB entry. |
| SSD/HDD is not detected in Setup | Missing storage driver, controller configuration, connection issue, or hardware failure. | Check firmware detection, hardware connections, storage-controller settings, and vendor drivers. |
| No Windows Boot Manager after conversion | Firmware mode or boot files may not be configured correctly. | Verify UEFI settings, inspect the EFI system partition, and follow Microsoft recovery guidance. |
| BitLocker recovery screen appears | Firmware, Secure Boot, TPM, or boot configuration changed. | Use the legitimate recovery key and investigate the triggering configuration change. |
| MBR2GPT validation fails | Unsupported disk layout, invalid BCD configuration, or another prerequisite failure. | Read the exact error and logs, inspect the partition layout, and resolve the failed prerequisite before retrying. |
| Secure Boot status cannot be queried | The environment or firmware does not support the query. | Check `msinfo32` and the manufacturer's firmware documentation. |
| Windows boots to the wrong drive | Multiple bootable disks or an unexpected boot order. | Review the boot order and identify the correct Windows Boot Manager entry. |

### Tiếng Việt – Nguyên tắc xử lý sự cố

1. Ghi nhận chính xác thông báo lỗi.
2. Xác nhận chế độ boot hiện tại.
3. Xác định đúng ổ đĩa và kiểu phân vùng.
4. Kiểm tra cáp, SSD/HDD, driver và cấu hình firmware khi có liên quan.
5. Sao lưu dữ liệu trước khi thực hiện các thay đổi có nguy cơ mất dữ liệu.
6. Thay đổi từng yếu tố và kiểm tra lại sau mỗi bước.
7. Ghi lại nguyên nhân và phương án khắc phục để phục vụ công việc IT Support.

**Do not immediately format the disk when an installation error occurs.** Diagnose the firmware mode, target disk, and partition layout first.

**Không định dạng ổ đĩa ngay khi gặp lỗi cài đặt.** Hãy kiểm tra chế độ firmware, ổ đĩa đích và bố cục phân vùng trước.

---

## 11. Best Practices – Quy trình thực hành tốt

### English

- Prefer UEFI/GPT for supported modern Windows deployments.
- Use official installation media.
- Confirm the target disk by its identity and capacity.
- Back up user data before partitioning or converting disks.
- Use Windows Setup to create the standard partition layout for a clean installation.
- Use MBR2GPT only for supported system-disk conversion scenarios.
- Preserve BitLocker recovery information before firmware changes.
- Avoid unnecessary Secure Boot or TPM changes.
- Document the original configuration, actions performed, and final results.
- Verify the system after installation before handing it back to the user.

### Tiếng Việt

- Ưu tiên UEFI/GPT cho các hệ thống Windows hiện đại được hỗ trợ.
- Sử dụng bộ cài Windows chính thức.
- Xác nhận ổ đĩa đích bằng thông tin nhận diện và dung lượng.
- Sao lưu dữ liệu trước khi phân vùng hoặc chuyển đổi ổ đĩa.
- Để Windows Setup tạo bố cục phân vùng tiêu chuẩn khi cài mới.
- Chỉ dùng MBR2GPT cho các trường hợp chuyển đổi ổ hệ thống được hỗ trợ.
- Bảo quản khóa khôi phục BitLocker trước khi thay đổi firmware.
- Tránh thay đổi Secure Boot hoặc TPM khi không cần thiết.
- Ghi lại cấu hình ban đầu, thao tác đã thực hiện và kết quả cuối cùng.
- Kiểm tra hệ thống trước khi bàn giao cho người dùng.

---

## 12. Practical Lab – Bài thực hành

### Lab objective – Mục tiêu

Practice identifying firmware mode, disk partition style, and installation readiness in a virtual machine or on a test computer with no required data.

Thực hành xác định chế độ firmware, kiểu phân vùng và mức độ sẵn sàng cài đặt trong máy ảo hoặc máy thử nghiệm không chứa dữ liệu cần giữ lại.

### Tasks – Các bước thực hành

**Task 1: Inspect the current environment**

```powershell
Get-Disk |
    Select-Object Number, FriendlyName, PartitionStyle, Size
```

Open `msinfo32` and record the BIOS Mode value.

Mở `msinfo32` và ghi nhận giá trị BIOS Mode.

**Task 2: Record the partition layout**

```powershell
Get-Partition |
    Select-Object DiskNumber, PartitionNumber, DriveLetter, Type, Size
```

Identify the Windows partition and relevant system partitions.

Xác định phân vùng Windows và các phân vùng hệ thống liên quan.

**Task 3: Inspect Secure Boot**

```powershell
Confirm-SecureBootUEFI
```

Record the output or error and explain what it means for the current environment.

Ghi lại kết quả hoặc thông báo lỗi và giải thích ý nghĩa đối với môi trường hiện tại.

**Task 4: Plan a clean UEFI/GPT installation**

Document the following without deleting any disk:

- Target disk identity.
- Current partition style.
- Required backup.
- Installation USB boot entry.
- Expected partition layout.
- Post-installation validation steps.

Ghi lại các thông tin trên mà không xóa bất kỳ ổ đĩa nào.

### Lab report template – Mẫu báo cáo

```text
Lab Name: Windows UEFI/GPT Installation

Computer / VM:
Windows Version:
Firmware Mode:
System Disk Number:
System Disk Partition Style:
Secure Boot Status:
Installation Method:
Backup Verified:
Issues Encountered:
Troubleshooting Steps:
Final Result:
Lessons Learned:
```

---

## 13. References – Tài liệu tham khảo

1. **Microsoft Learn – Windows Setup: Installing using the MBR or GPT partition style**

   https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-setup-installing-using-the-mbr-or-gpt-partition-style

   Explains the relationship between firmware boot mode and disk partition style.

2. **Microsoft Learn – MBR2GPT**

   https://learn.microsoft.com/en-us/windows/deployment/mbr-to-gpt

   Documents conversion prerequisites, command-line options, validation, and troubleshooting.

3. **Microsoft Learn – UEFI/GPT-based hard drive partitions**

   https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/configure-uefigpt-based-hard-drive-partitions

   Describes the standard system, MSR, Windows, and recovery partitions.

4. **Microsoft – Windows 11 specifications and requirements**

   https://www.microsoft.com/windows/windows-11-specifications

   Provides Windows 11 hardware and system requirements.

5. **Microsoft – Windows 11 download**

   https://www.microsoft.com/software-download/windows11

   Provides official Windows 11 download and installation resources.

---

## 14. Document Information – Thông tin tài liệu

| Field | Value |
|---|---|
| Document | Windows-UEFI-GPT.md |
| Category | Windows / Installation |
| Language | English with Vietnamese explanations |
| Audience | IT Support, Helpdesk, Junior System Administrator |
| Difficulty | Beginner to Intermediate |
| Topics | UEFI, GPT, Secure Boot, Windows Setup, MBR2GPT |
| Last reviewed | 2026-10-21 |
| Maintainer | Truong Anh Nguyen |

**Disclaimer:** This document is a technical learning guide. Always verify the actual device configuration and consult current Microsoft and manufacturer documentation before making firmware or disk-partition changes.

**Lưu ý:** Đây là tài liệu học tập kỹ thuật. Luôn xác minh cấu hình thực tế và tham khảo tài liệu Microsoft cũng như nhà sản xuất trước khi thay đổi firmware hoặc phân vùng ổ đĩa.
