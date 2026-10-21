# Windows Installation – Tài liệu cài đặt Windows

> A bilingual Vietnamese-English knowledge base covering Windows installation, disk partitioning, boot modes, activation, and post-installation configuration.

> Kho tài liệu song ngữ Việt – Anh về cài đặt Windows, phân vùng ổ đĩa, chế độ khởi động, kích hoạt và cấu hình sau cài đặt.

## 1. Overview – Tổng quan

### Tiếng Việt

Thư mục này tập hợp kiến thức và quy trình thực hành cài đặt Windows dành cho người học IT, kỹ thuật viên IT Support và quản trị viên hệ thống.

Nội dung bao gồm:

- Tổng quan quy trình cài đặt Windows.
- Tạo USB cài đặt Windows.
- Quản lý ổ đĩa, phân vùng và hệ thống tệp.
- Cài đặt Windows theo chuẩn UEFI/GPT.
- Cài đặt Windows theo chuẩn Legacy BIOS/MBR.
- Cấu hình và kiểm tra hệ thống sau cài đặt.
- Kích hoạt Windows và xử lý lỗi cấp phép.
- Thực hành kiểm tra và khắc phục sự cố khởi động.

### English

This directory contains Windows installation knowledge and practical procedures for IT learners, IT Support technicians, and system administrators.

Topics include:

- Windows installation fundamentals.
- Creating Windows installation media.
- Disk, partition, and file system management.
- UEFI/GPT installation.
- Legacy BIOS/MBR installation.
- Post-installation configuration and verification.
- Windows activation and licensing troubleshooting.
- Boot troubleshooting and practical labs.

## 2. Documentation Structure – Cấu trúc tài liệu

| File | Description |
|---|---|
| [Windows-Installation-Overview.md](Windows-Installation-Overview.md) | Tổng quan quy trình cài đặt Windows. / Windows installation fundamentals. |
| [Windows-USB-Installation.md](Windows-USB-Installation.md) | Tạo USB boot và chuẩn bị bộ cài. / Creating bootable installation media. |
| [Windows-Partitioning.md](Windows-Partitioning.md) | Quản lý ổ đĩa, phân vùng và file system. / Disk and partition management. |
| [Windows-UEFI-GPT.md](Windows-UEFI-GPT.md) | Cài đặt và kiểm tra UEFI/GPT. / UEFI/GPT installation and verification. |
| [Windows-Legacy-BIOS-MBR.md](Windows-Legacy-BIOS-MBR.md) | Cài đặt và kiểm tra Legacy BIOS/MBR. / Legacy BIOS/MBR installation and verification. |
| [Windows-Post-Installation.md](Windows-Post-Installation.md) | Cấu hình, cài driver và kiểm tra sau cài đặt. / Post-installation setup and testing. |
| [Windows-Activation.md](Windows-Activation.md) | Kích hoạt và xử lý lỗi cấp phép Windows. / Windows activation and licensing troubleshooting. |

**Lưu ý:** Tên file trong bảng phải khớp chính xác với tên file thực tế trên GitHub, bao gồm dấu gạch nối và phần mở rộng `.md`.

**Note:** File names in this table must exactly match the actual GitHub file names, including hyphens and the `.md` extension.

## 3. Recommended Learning Path – Lộ trình học đề xuất

### English

1. **Windows-Installation-Overview.md** — Understand the installation workflow and prerequisites.
2. **Windows-USB-Installation.md** — Create installation media and learn boot-menu selection.
3. **Windows-Partitioning.md** — Understand disks, partitions, and file systems.
4. **Windows-UEFI-GPT.md** — Practice modern firmware and partition configurations.
5. **Windows-Legacy-BIOS-MBR.md** — Understand legacy boot compatibility.
6. **Windows-Post-Installation.md** — Configure drivers, updates, security, and connectivity.
7. **Windows-Activation.md** — Verify licensing status and troubleshoot activation errors.

### Tiếng Việt

1. Học tổng quan quy trình và các điều kiện trước khi cài đặt.
2. Thực hành tạo USB boot và chọn đúng thiết bị khởi động.
3. Tìm hiểu ổ đĩa, phân vùng và hệ thống tệp.
4. Thực hành cài đặt theo chuẩn UEFI/GPT.
5. Hiểu khả năng tương thích của Legacy BIOS/MBR.
6. Hoàn thiện Windows sau cài đặt: driver, cập nhật, bảo mật và mạng.
7. Kiểm tra kích hoạt Windows và xử lý lỗi cấp phép.

## 4. Practical Labs – Bài thực hành

### Lab 01: Create a Bootable USB

**Objective:** Prepare official Windows installation media.

**Mục tiêu:** Chuẩn bị USB cài Windows từ nguồn chính thức.

**Tasks – Các bước thực hiện**

- Obtain the official Windows installation tool or ISO.
- Verify the USB capacity and back up any data on it.
- Create the bootable installation media.
- Confirm that the process completed successfully.
- Test the boot menu on a suitable computer.

- Tải công cụ hoặc file ISO Windows từ nguồn chính thức.
- Kiểm tra dung lượng USB và sao lưu dữ liệu trước khi tạo USB boot.
- Tạo USB cài đặt.
- Xác nhận quá trình tạo USB hoàn tất.
- Kiểm tra menu boot trên máy tính phù hợp.

**Expected result – Kết quả mong đợi:** Tạo được USB cài Windows và xác định đúng tùy chọn khởi động.

### Lab 02: Identify Disk Partition Styles

**Objective:** Inspect the partition style of available disks.

**Mục tiêu:** Kiểm tra kiểu phân vùng của các ổ đĩa hiện có.

Run PowerShell as Administrator:

```powershell
Get-Disk |
    Select-Object Number, FriendlyName, PartitionStyle, Size
```

To inspect volumes:

```powershell
Get-Volume |
    Select-Object DriveLetter, FileSystem, FileSystemLabel, Size
```

**Tasks – Các bước thực hiện**

- Identify the target disk by its number, model, and capacity.
- Record whether the disk uses GPT, MBR, or another reported state.
- Inspect existing partitions and volumes.
- Understand the difference between a physical disk, a partition, and a volume.
- Do not modify the disk during this inspection lab.

- Xác định ổ đĩa mục tiêu dựa trên số thứ tự, model và dung lượng.
- Ghi nhận ổ đĩa đang sử dụng GPT, MBR hay trạng thái khác.
- Kiểm tra các phân vùng và volume hiện có.
- Phân biệt ổ đĩa vật lý, phân vùng và volume.
- Không thay đổi cấu trúc ổ đĩa trong bài thực hành kiểm tra này.

**Expected result – Kết quả mong đợi:** Biết cách kiểm tra kiểu phân vùng trước khi cài đặt hoặc thay đổi ổ đĩa.

### Lab 03: Practice Windows Installation

**Objective:** Install Windows in a controlled test environment.

**Mục tiêu:** Thực hành cài đặt Windows trong môi trường thử nghiệm có kiểm soát.

**Tasks – Các bước thực hiện**

- Prepare official installation media.
- Confirm the intended firmware boot mode.
- Identify the correct test disk.
- Review the existing partition layout.
- Complete Windows Setup.
- Verify the first boot and sign-in process.

- Chuẩn bị USB cài Windows chính thức.
- Xác nhận chế độ boot dự kiến.
- Xác định chính xác ổ đĩa thử nghiệm.
- Kiểm tra cấu trúc phân vùng hiện tại.
- Hoàn tất Windows Setup.
- Kiểm tra lần khởi động đầu tiên và quá trình đăng nhập.

**Expected result – Kết quả mong đợi:** Hiểu và thực hiện được quy trình cài Windows trong môi trường thử nghiệm.

**Safety:** Use a virtual machine or a dedicated test disk whenever possible. Installing Windows can erase data if the wrong disk or partition is selected.

**An toàn:** Ưu tiên máy ảo hoặc ổ đĩa thử nghiệm riêng. Cài đặt Windows có thể làm mất dữ liệu nếu chọn nhầm ổ đĩa hoặc phân vùng.

### Lab 04: Configure Windows After Installation

**Objective:** Prepare a newly installed system for use.

**Mục tiêu:** Hoàn thiện hệ thống Windows mới cài đặt.

**Tasks – Các bước thực hiện**

- Check Windows edition, version, and build.
- Inspect Device Manager.
- Install the required drivers.
- Run Windows Update.
- Test network, audio, display, and peripherals.
- Verify Windows activation status.
- Check Windows Security.
- Document the final system state.

- Kiểm tra edition, phiên bản và build Windows.
- Kiểm tra Device Manager.
- Cài đặt driver cần thiết.
- Chạy Windows Update.
- Kiểm tra mạng, âm thanh, màn hình và thiết bị ngoại vi.
- Xác minh trạng thái kích hoạt Windows.
- Kiểm tra Windows Security.
- Ghi nhận trạng thái cuối cùng của hệ thống.

**Expected result – Kết quả mong đợi:** Hoàn thành checklist kiểm tra máy sau cài đặt.

### Lab 05: Troubleshoot Boot Configuration

**Objective:** Understand boot-mode and partition-style compatibility.

**Mục tiêu:** Hiểu tính tương thích giữa chế độ boot và kiểu phân vùng.

**Tasks – Các bước thực hiện**

- Open `msinfo32` and inspect BIOS Mode.
- Use PowerShell to inspect the partition style.
- Compare UEFI/GPT and Legacy BIOS/MBR configurations.
- Identify possible causes of boot compatibility errors.
- Explain the appropriate resolution without deleting data unnecessarily.

- Mở `msinfo32` và kiểm tra BIOS Mode.
- Dùng PowerShell kiểm tra kiểu phân vùng.
- So sánh cấu hình UEFI/GPT và Legacy BIOS/MBR.
- Xác định nguyên nhân có thể gây lỗi tương thích khi boot.
- Giải thích phương án xử lý phù hợp mà không xóa dữ liệu tùy tiện.

**Expected result – Kết quả mong đợi:** Biết cách xác định vấn đề tương thích giữa chế độ boot và kiểu phân vùng trước khi thay đổi hệ thống.

## 5. Safety Checklist – Checklist an toàn

### Before Installation – Trước khi cài đặt

- [ ] Back up important files.
- [ ] Confirm the correct target disk.
- [ ] Verify the installation media source.
- [ ] Check firmware boot mode.
- [ ] Inspect the disk partition style.
- [ ] Check BitLocker or other drive encryption and secure recovery keys.
- [ ] Confirm the intended Windows edition and applicable license.
- [ ] Verify hardware and Windows compatibility.
- [ ] Confirm that required network or storage drivers are available.

### After Installation – Sau khi cài đặt

- [ ] Confirm Windows boots successfully.
- [ ] Verify Windows edition, version, and build.
- [ ] Inspect Device Manager for unresolved device issues.
- [ ] Install required drivers and updates.
- [ ] Test networking and essential peripherals.
- [ ] Verify activation status.
- [ ] Check security settings.
- [ ] Confirm that required user data is restored.
- [ ] Document test results and outstanding issues.

### Tiếng Việt

**Trước khi cài đặt**

- [ ] Sao lưu dữ liệu quan trọng.
- [ ] Xác nhận đúng ổ đĩa mục tiêu.
- [ ] Kiểm tra nguồn bộ cài.
- [ ] Kiểm tra chế độ boot của firmware.
- [ ] Kiểm tra kiểu phân vùng.
- [ ] Kiểm tra BitLocker hoặc cơ chế mã hóa ổ đĩa và lưu khóa khôi phục an toàn.
- [ ] Xác nhận edition Windows và giấy phép phù hợp.
- [ ] Kiểm tra tính tương thích phần cứng và Windows.
- [ ] Chuẩn bị driver mạng hoặc lưu trữ cần thiết nếu có.

**Sau khi cài đặt**

- [ ] Xác nhận Windows khởi động thành công.
- [ ] Kiểm tra edition, phiên bản và build Windows.
- [ ] Kiểm tra lỗi thiết bị trong Device Manager.
- [ ] Cài driver và bản cập nhật cần thiết.
- [ ] Kiểm tra mạng và thiết bị ngoại vi.
- [ ] Xác minh trạng thái kích hoạt.
- [ ] Kiểm tra cấu hình bảo mật.
- [ ] Xác nhận dữ liệu cần thiết đã được khôi phục.
- [ ] Ghi nhận kết quả và các vấn đề còn tồn tại.

**Important / Quan trọng:** Never delete, clean, or format a partition until you have verified the target disk, confirmed the intended action, and protected all data that must be retained.

Không xóa, làm sạch hoặc format phân vùng khi chưa xác nhận đúng ổ đĩa, mục đích thao tác và phương án bảo vệ dữ liệu cần giữ lại.

## 6. Recommended Tools – Công cụ đề xuất

| Tool | Purpose | Mục đích |
|---|---|---|
| Windows Media Creation Tool | Create official installation media when supported. | Tạo bộ cài Windows chính thức khi được hỗ trợ. |
| Windows Setup | Install or upgrade Windows. | Cài đặt hoặc nâng cấp Windows. |
| Disk Management | Inspect and manage disks and volumes. | Kiểm tra và quản lý ổ đĩa, volume. |
| DiskPart | Perform advanced disk-management operations. | Thực hiện thao tác quản lý ổ đĩa nâng cao. |
| PowerShell | Inspect disks and system configuration. | Kiểm tra ổ đĩa và cấu hình hệ thống. |
| `msinfo32` | Review system information and BIOS Mode. | Xem thông tin hệ thống và BIOS Mode. |
| `slmgr.vbs` | Inspect Windows licensing information. | Kiểm tra thông tin cấp phép Windows. |
| Device Manager | Inspect device and driver status. | Kiểm tra trạng thái thiết bị và driver. |
| Windows Security | Review security status and protections. | Kiểm tra trạng thái bảo mật và các biện pháp bảo vệ. |

**Caution:** DiskPart includes destructive commands. Do not run commands such as `clean`, `format`, or `delete partition` unless the target and intended outcome have been verified.

**Cảnh báo:** DiskPart có các lệnh có thể xóa dữ liệu. Không chạy những lệnh như `clean`, `format` hoặc `delete partition` nếu chưa xác minh ổ đĩa và kết quả mong muốn.

## 7. References – Tài liệu tham khảo

- Windows downloads: https://www.microsoft.com/software-download/
- Microsoft Support: https://support.microsoft.com/windows
- Microsoft Learn: https://learn.microsoft.com/
- MBR2GPT documentation: https://learn.microsoft.com/en-us/windows/deployment/mbr-to-gpt
- Windows installation media guidance: https://support.microsoft.com/windows

Prefer official Microsoft documentation and verify that the instructions apply to the Windows version being installed.

Ưu tiên tài liệu chính thức của Microsoft và xác minh hướng dẫn phù hợp với phiên bản Windows đang cài đặt.

## 8. Documentation Standards – Tiêu chuẩn tài liệu

- Use Markdown (`.md`) format.
- Provide Vietnamese and English explanations.
- Include practical examples, commands, and expected results.
- Explain the purpose, prerequisites, and risks of administrative commands.
- Reference official Microsoft documentation.
- Never include passwords, product keys, or confidential company data.
- Record actual lab results rather than claiming tests that were not performed.
- Keep file names consistent with the links in `README.md`.
- Update documentation when procedures or supported Windows versions change.

### Tiếng Việt

- Sử dụng định dạng Markdown (`.md`).
- Trình bày nội dung bằng tiếng Việt và tiếng Anh.
- Có ví dụ thực hành, lệnh và kết quả mong đợi.
- Giải thích mục đích, điều kiện thực hiện và rủi ro của lệnh quản trị.
- Dẫn nguồn tài liệu chính thức của Microsoft.
- Không đưa mật khẩu, Product Key hoặc dữ liệu nội bộ bảo mật vào tài liệu.
- Chỉ ghi nhận kết quả thực hành đã thực sự thực hiện.
- Đảm bảo tên file thống nhất với các liên kết trong `README.md`.
- Cập nhật tài liệu khi quy trình hoặc phiên bản Windows được hỗ trợ thay đổi.

## 9. Disclaimer – Lưu ý

This repository is an educational IT knowledge base. Procedures may vary depending on the Windows version, hardware, firmware, partition layout, license type, and organizational policy.

Đây là kho kiến thức IT phục vụ học tập và phát triển kỹ năng. Quy trình có thể khác nhau tùy phiên bản Windows, phần cứng, firmware, cấu trúc phân vùng, loại giấy phép và chính sách của tổ chức.

Always verify compatibility, maintain appropriate backups, and protect important data before making system changes.

Luôn kiểm tra tính tương thích, sao lưu phù hợp và bảo vệ dữ liệu quan trọng trước khi thay đổi hệ thống.

