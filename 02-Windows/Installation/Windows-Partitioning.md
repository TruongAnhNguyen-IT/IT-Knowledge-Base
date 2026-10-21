
# Windows Partitioning – Phân vùng ổ đĩa Windows

## 1. Purpose – Mục đích

### Tiếng Việt

Phân vùng ổ đĩa là quá trình chia thiết bị lưu trữ thành các vùng logic để Windows có thể sử dụng và quản lý dữ liệu. Tài liệu này trình bày các khái niệm cơ bản, công cụ quản lý phân vùng và quy trình phân vùng an toàn.

### English

Disk partitioning divides a storage device into logical regions that Windows can use and manage. This document covers partitioning fundamentals, management tools, and safe partitioning procedures.

## 2. Key Terms – Thuật ngữ cơ bản

| Term | Explanation |
|---|---|
| Physical disk | The actual HDD, SSD, or other storage device. |
| Partition | A defined region of a disk. |
| Volume | A storage area Windows can use, often associated with a partition. |
| File system | The method used to organize files, such as NTFS or FAT32. |
| Drive letter | A Windows identifier such as C: or D:. |
| Unallocated space | Disk space that is not currently assigned to a partition. |
| EFI System Partition | A system partition used for UEFI boot files. |
| Recovery partition | A partition used for Windows recovery components. |

### Tiếng Việt

- Physical disk: Thiết bị lưu trữ vật lý.
- Partition: Phân vùng trên ổ đĩa.
- Volume: Vùng lưu trữ mà Windows có thể sử dụng.
- File system: Hệ thống tệp, ví dụ NTFS hoặc FAT32.
- Drive letter: Ký tự ổ đĩa như C: hoặc D:.
- Unallocated space: Dung lượng chưa được phân vùng.
- EFI System Partition: Phân vùng chứa các tệp khởi động UEFI.
- Recovery partition: Phân vùng chứa thành phần khôi phục Windows.

## 3. Common Partition Layout – Bố cục phân vùng phổ biến

A modern Windows UEFI/GPT installation may include:

| Partition | Purpose |
|---|---|
| EFI System Partition (ESP) | Stores UEFI boot files. |
| Microsoft Reserved (MSR) | Reserved for Windows disk management. |
| Windows partition | Stores the Windows operating system and applications. |
| Recovery partition | Supports applicable Windows recovery functions. |
| Data partition (optional) | Stores user data separately when desired. |

### Tiếng Việt

Máy cài Windows theo UEFI/GPT có thể gồm phân vùng EFI, MSR, phân vùng Windows, phân vùng Recovery và phân vùng dữ liệu tùy nhu cầu.

Số lượng, thứ tự và dung lượng phân vùng có thể thay đổi theo phiên bản Windows, cấu hình và phương thức triển khai. Nên để Windows Setup tạo các phân vùng hệ thống cần thiết trong trường hợp cài mới thông thường.

## 4. Recommended File Systems – Hệ thống tệp

| File system | Typical use |
|---|---|
| NTFS | Windows system and general internal storage volumes. |
| FAT32 | Commonly used for EFI system partitions and compatible removable media. |
| exFAT | Commonly used for removable storage shared across platforms. |

Tiếng Việt:

- NTFS: Thường dùng cho phân vùng Windows và ổ dữ liệu nội bộ.
- FAT32: Thường dùng cho phân vùng EFI và một số thiết bị lưu trữ tương thích.
- exFAT: Thường dùng cho thiết bị lưu trữ di động chia sẻ giữa nhiều hệ điều hành.

Choose a file system based on the intended use and platform requirements.

Chọn hệ thống tệp dựa trên mục đích sử dụng và yêu cầu của nền tảng.

## 5. Tool 1: Disk Management – Quản lý đĩa

Open Disk Management:

1. Press `Win + X`.
2. Select Disk Management.
3. Inspect the disk layout.
4. Identify the target disk.
5. Check the disk capacity and existing partitions.
6. Perform only the required operation.

Alternative:

```text
Win + R
diskmgmt.msc
```

### Tiếng Việt

1. Nhấn `Win + X`.
2. Chọn Disk Management.
3. Kiểm tra bố cục ổ đĩa.
4. Xác định đúng ổ đĩa.
5. Kiểm tra dung lượng và các phân vùng.
6. Chỉ thực hiện thao tác cần thiết.

## 6. Tool 2: DiskPart – Quản lý bằng dòng lệnh

Run Command Prompt or Windows Terminal as Administrator.

List disks:

```cmd
diskpart
list disk
```

Select a disk for inspection:

```cmd
select disk 0
detail disk
list partition
list volume
exit
```

Important: Disk 0 is an example, not a guarantee that the intended drive is Disk 0.

### Tiếng Việt

- `list disk`: Liệt kê các ổ đĩa.
- `detail disk`: Hiển thị thông tin ổ đĩa được chọn.
- `list partition`: Liệt kê phân vùng.
- `list volume`: Liệt kê volume.
- `exit`: Thoát DiskPart.

**Warning:** Commands such as `clean`, `delete partition`, `format`, and `convert` can cause data loss or make an existing installation unbootable. Verify the target disk and backup before using them.

**Cảnh báo:** Các lệnh `clean`, `delete partition`, `format` và `convert` có thể làm mất dữ liệu hoặc khiến hệ điều hành không khởi động được. Luôn kiểm tra ổ đĩa và sao lưu trước.

## 7. Create a Data Partition – Tạo phân vùng dữ liệu

For a disk with suitable unallocated space:

1. Open Disk Management.
2. Right-click the unallocated space.
3. Select New Simple Volume.
4. Specify the volume size.
5. Assign an available drive letter.
6. Select a suitable file system, typically NTFS for an internal Windows data volume.
7. Enter a volume label.
8. Confirm the settings.

### Tiếng Việt

1. Mở Disk Management.
2. Nhấp phải vùng Unallocated.
3. Chọn New Simple Volume.
4. Nhập dung lượng.
5. Chọn ký tự ổ đĩa còn trống.
6. Chọn hệ thống tệp phù hợp, thường là NTFS đối với ổ dữ liệu nội bộ.
7. Đặt tên volume.
8. Kiểm tra và xác nhận.

Do not format a volume that contains data you need to preserve.

Không format phân vùng đang chứa dữ liệu cần giữ lại.

## 8. Shrink a Volume – Thu nhỏ phân vùng

1. Open Disk Management.
2. Right-click the target volume.
3. Select Shrink Volume.
4. Wait for Windows to calculate available shrink space.
5. Enter the amount to shrink.
6. Confirm the operation.
7. Verify the resulting unallocated space.

### Tiếng Việt

Thao tác thu nhỏ phân vùng có thể bị giới hạn bởi các tệp không thể di chuyển, dung lượng trống và trạng thái ổ đĩa. Hãy sao lưu dữ liệu quan trọng trước khi thay đổi phân vùng.

## 9. Extend a Volume – Mở rộng phân vùng

Disk Management generally requires suitable unallocated space immediately adjacent to the right of the volume being extended on the same basic disk.

Tiếng Việt:

Disk Management thường yêu cầu vùng Unallocated nằm liền kề bên phải phân vùng cần mở rộng trên cùng một basic disk.

If the Extend Volume option is unavailable, inspect the disk layout before making any changes. Do not delete a recovery or data partition just to make the option available.

Nếu không thể chọn Extend Volume, hãy kiểm tra bố cục ổ đĩa. Không xóa phân vùng Recovery hoặc phân vùng dữ liệu chỉ để mở khóa tùy chọn này.

## 10. Before Changing Partitions – Trước khi thay đổi phân vùng

Before creating, deleting, formatting, shrinking, extending, or converting partitions, complete the following safety checklist to reduce the risk of data loss and system failure.

Trước khi tạo, xóa, định dạng, thu nhỏ, mở rộng hoặc chuyển đổi phân vùng, hãy hoàn thành danh sách kiểm tra an toàn sau để giảm nguy cơ mất dữ liệu và lỗi hệ thống.

### 10.1 Pre-Operation Checklist – Danh sách kiểm tra trước khi thao tác

- [ ] **Confirm the correct physical disk – Xác nhận đúng ổ đĩa vật lý.**
  - Verify the disk number, model, capacity, and existing partitions.
  - Kiểm tra số thứ tự ổ đĩa, model, dung lượng và các phân vùng hiện có.
  - Do not identify a disk by its number alone.
  - Không xác định ổ đĩa chỉ dựa vào số thứ tự.

  ```powershell
  Get-Disk | Select-Object Number, FriendlyName, PartitionStyle, Size
  ```

- [ ] **Record the existing partition layout – Ghi lại cấu trúc phân vùng hiện tại.**
  - Record partition sizes, drive letters, file systems, and their purposes.
  - Ghi lại dung lượng, ký tự ổ đĩa, hệ thống tệp và mục đích của từng phân vùng.
  - Take screenshots of Disk Management before making changes.
  - Chụp ảnh Disk Management trước khi thay đổi.

- [ ] **Back up important data – Sao lưu dữ liệu quan trọng.**
  - Back up important files to another physical drive or a trusted backup location.
  - Sao lưu các tệp quan trọng sang ổ đĩa vật lý khác hoặc vị trí sao lưu đáng tin cậy.
  - Verify that the backup is accessible and the important files are intact.
  - Kiểm tra bản sao lưu để bảo đảm có thể truy cập và các tệp quan trọng vẫn nguyên vẹn.

- [ ] **Check BitLocker status and prepare the recovery key – Kiểm tra BitLocker và chuẩn bị khóa khôi phục.**
  - Check whether BitLocker or Device Encryption is enabled.
  - Kiểm tra BitLocker hoặc Device Encryption có đang bật hay không.
  - Ensure the recovery key is accessible and stored separately from the affected device.
  - Bảo đảm có thể truy cập khóa khôi phục và lưu khóa ở nơi riêng biệt với thiết bị đang thao tác.

  ```powershell
  Get-BitLockerVolume
  ```

- [ ] **Confirm the intended operation – Xác nhận thao tác dự định thực hiện.**
  - Confirm whether the task involves creating, deleting, formatting, shrinking, extending, or converting a partition.
  - Xác định thao tác cần thực hiện là tạo, xóa, định dạng, thu nhỏ, mở rộng hay chuyển đổi phân vùng.
  - Verify the target disk and partition before confirming any changes.
  - Kiểm tra lại ổ đĩa và phân vùng mục tiêu trước khi xác nhận thay đổi.

- [ ] **Ensure sufficient free space – Đảm bảo đủ dung lượng trống.**
  - Check available space before shrinking or modifying a volume.
  - Kiểm tra dung lượng còn trống trước khi thu nhỏ hoặc chỉnh sửa phân vùng.
  - When extending a volume, verify that suitable unallocated space is available in the required location.
  - Khi mở rộng phân vùng, xác minh có vùng chưa phân bổ phù hợp tại vị trí cần thiết.

- [ ] **Avoid interrupting partition operations – Tránh làm gián đoạn thao tác phân vùng.**
  - Ensure a stable power supply before starting.
  - Bảo đảm nguồn điện ổn định trước khi bắt đầu.
  - Do not force shutdown, restart, or disconnect the drive while an operation is in progress.
  - Không tắt máy cưỡng bức, khởi động lại hoặc ngắt kết nối ổ đĩa khi thao tác đang diễn ra.
  - Wait for the operation to complete before proceeding.
  - Chờ thao tác hoàn tất trước khi tiếp tục.

### 10.2 Safety Notes – Lưu ý an toàn

- Never delete or format a partition if its purpose is unknown.
- Không xóa hoặc định dạng phân vùng khi chưa biết rõ mục đích sử dụng.
- Do not initialize or format a disk simply because Windows cannot read it; doing so may complicate data recovery.
- Không khởi tạo hoặc định dạng ổ đĩa chỉ vì Windows không đọc được; việc này có thể khiến quá trình khôi phục dữ liệu phức tạp hơn.
- If a disk shows signs of physical failure, prioritize data recovery and avoid unnecessary write operations.
- Nếu ổ đĩa có dấu hiệu hư hỏng vật lý, hãy ưu tiên khôi phục dữ liệu và tránh các thao tác ghi không cần thiết.

**Important – Quan trọng:** If any safety requirement cannot be verified, stop and investigate before changing partitions.

Nếu chưa xác minh được bất kỳ yêu cầu an toàn nào, hãy dừng lại và kiểm tra trước khi thay đổi phân vùng.

## 11. Troubleshooting – Xử lý sự cố


## 11. Troubleshooting – Xử lý sự cố phân vùng ổ đĩa

| Issue – Sự cố | Possible Cause – Nguyên nhân có thể | Recommended Action – Hướng xử lý |
|---|---|---|
| Disk is not visible – Không thấy ổ đĩa | Loose connection, disabled storage controller, missing driver, or hardware failure. / Kết nối lỏng, bộ điều khiển lưu trữ bị tắt, thiếu driver hoặc lỗi phần cứng. | Check SATA/power cables or SSD installation, inspect BIOS/UEFI, and install the appropriate storage driver. / Kiểm tra cáp SATA/nguồn hoặc vị trí lắp SSD, kiểm tra BIOS/UEFI và cài driver lưu trữ phù hợp. |
| Volume has no drive letter – Phân vùng không có ký tự ổ đĩa | Drive letter was removed, is unavailable, or the volume is not mounted. / Ký tự ổ đĩa bị gỡ, không khả dụng hoặc volume chưa được gắn kết. | Open Disk Management, inspect the volume, and assign an available drive letter if appropriate. / Mở Disk Management, kiểm tra volume và gán ký tự còn trống nếu phù hợp. |
| Cannot shrink sufficiently – Không thể thu nhỏ phân vùng theo dung lượng mong muốn | Insufficient free space or unmovable files near the end of the volume. / Không đủ dung lượng trống hoặc có tệp không thể di chuyển gần cuối phân vùng. | Check available free space, remove unnecessary files, and retry. Back up important data before making changes. / Kiểm tra dung lượng trống, xóa tệp không cần thiết và thử lại. Sao lưu dữ liệu quan trọng trước khi thay đổi. |
| Cannot extend volume – Không thể mở rộng phân vùng | No suitable unallocated space immediately to the right of the volume, or unsupported disk configuration. / Không có vùng Unallocated phù hợp nằm ngay bên phải phân vùng hoặc cấu hình ổ đĩa không được hỗ trợ. | Inspect the disk layout in Disk Management. Plan a supported partition change or use an appropriate tool after backing up data. / Kiểm tra bố cục ổ đĩa trong Disk Management. Lập phương án thay đổi phân vùng được hỗ trợ sau khi sao lưu dữ liệu. |
| Partition appears RAW – Phân vùng hiển thị RAW | File system is corrupted, unrecognized, or inaccessible. / Hệ thống tệp bị hỏng, không được nhận diện hoặc không thể truy cập. | Stop writing to the disk. Do not format the partition if data recovery is required. Assess recovery options or consult a data recovery specialist. / Ngừng ghi dữ liệu lên ổ đĩa. Không format nếu cần khôi phục dữ liệu. Đánh giá phương án cứu dữ liệu hoặc liên hệ chuyên gia. |
| Disk reports errors – Ổ đĩa báo lỗi | File system errors, bad sectors, device degradation, or connection problems. / Lỗi hệ thống tệp, sector lỗi, ổ đĩa xuống cấp hoặc sự cố kết nối. | Back up important data immediately if the disk is accessible. Check the manufacturer's drive health tools and investigate hardware or file system errors. / Sao lưu dữ liệu quan trọng ngay nếu còn truy cập được. Kiểm tra công cụ đánh giá tình trạng ổ đĩa của nhà sản xuất và xác định lỗi phần cứng hoặc hệ thống tệp. |

### Additional Diagnostic Commands – Lệnh kiểm tra bổ sung

#### 1. List disks – Liệt kê ổ đĩa

Run PowerShell as Administrator:

```powershell
Get-Disk |
    Select-Object Number, FriendlyName, OperationalStatus, HealthStatus, PartitionStyle, Size
```

Purpose: Inspect detected disks, their reported status, partition style, and capacity.

Mục đích: Kiểm tra các ổ đĩa được nhận diện, trạng thái do hệ thống báo cáo, kiểu phân vùng và dung lượng.

Note: `HealthStatus` is not a definitive hardware diagnostic. Some devices and storage controllers may not provide complete health information.

Lưu ý: `HealthStatus` không phải kết quả chẩn đoán phần cứng tuyệt đối. Một số thiết bị hoặc bộ điều khiển lưu trữ không cung cấp đầy đủ thông tin tình trạng.

#### 2. List volumes – Liệt kê volume

```powershell
Get-Volume |
    Select-Object DriveLetter, FileSystem, FileSystemLabel, HealthStatus, Size, SizeRemaining
```

Purpose: Review drive letters, file systems, labels, and available space.

Mục đích: Kiểm tra ký tự ổ đĩa, hệ thống tệp, nhãn volume và dung lượng còn trống.

#### 3. Check a file system – Kiểm tra hệ thống tệp

```cmd
chkdsk C: /scan
```

Purpose: Scan the supported file system on drive C: for errors without requesting an offline repair.

Mục đích: Quét lỗi hệ thống tệp được hỗ trợ trên ổ C: mà không yêu cầu sửa chữa ngoại tuyến.

Replace `C:` with the correct volume letter.

Thay `C:` bằng ký tự volume phù hợp.

**Warning – Cảnh báo:** If a drive may be physically failing or contains irreplaceable data, prioritize data recovery and backup before running repair operations. Do not format or initialize a disk simply because Windows cannot read it.

Nếu nghi ngờ ổ đĩa hỏng vật lý hoặc chứa dữ liệu không thể thay thế, hãy ưu tiên cứu dữ liệu và sao lưu trước khi sửa chữa. Không format hoặc initialize ổ đĩa chỉ vì Windows không đọc được.


## 12. References – Tài liệu tham khảo

- Microsoft Support: https://support.microsoft.com/
- Microsoft Learn: https://learn.microsoft.com/

