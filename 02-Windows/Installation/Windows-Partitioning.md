
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

- [ ] Confirm the correct physical disk.
- [ ] Record the existing partition layout.
- [ ] Back up important data.
- [ ] Check BitLocker status and prepare the recovery key.
- [ ] Confirm the intended operation.
- [ ] Ensure sufficient free space.
- [ ] Avoid interrupting partition operations.

## 11. Troubleshooting – Xử lý sự cố

| Issue | Possible action |
|---|---|
| Disk is not visible | Check connections, firmware, and storage drivers. |
| Volume has no drive letter | Check Disk Management and assign a letter if appropriate. |
| Cannot shrink sufficiently | Check free space and immovable files. |
| Cannot extend volume | Inspect adjacent unallocated space and disk type. |
| Partition appears RAW | Stop writing to the volume and investigate recovery options. |
| Disk reports errors | Check disk health and back up important data. |

## 12. References – Tài liệu tham khảo

- Microsoft Support: https://support.microsoft.com/
- Microsoft Learn: https://learn.microsoft.com/

