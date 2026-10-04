
# Storage Troubleshooting

## 🇻🇳 Tiếng Việt

## 1. Mục tiêu

Mục tiêu troubleshooting là xác định:

> Storage lỗi, kết nối lỗi, motherboard lỗi, cấu hình lỗi hay OS lỗi?

Không nên ngay lập tức kết luận:

> "Ổ cứng hỏng."

---

## 2. Storage không được nhận

### Triệu chứng

- BIOS không thấy drive.
- Windows không thấy drive.
- Disk Management không thấy.
- Linux không thấy.

### Quy trình

1. Tắt máy.
2. Kiểm tra cable.
3. Kiểm tra power.
4. Reseat drive.
5. Thử SATA port khác.
6. Thử M.2 slot khác.
7. Kiểm tra BIOS.
8. Kiểm tra BIOS storage settings.
9. Test drive trên máy khác.
10. Test drive khác trên hệ thống hiện tại.

---

## 3. BIOS nhận nhưng Windows không nhận

Kiểm tra:

1. Disk Management.
2. Device Manager.
3. Disk status.
4. Driver.
5. Partition.
6. Filesystem.
7. Offline/Online state.

Có thể drive chưa được:

- Initialized
- Partitioned
- Assigned drive letter

Không được format nếu dữ liệu quan trọng chưa được backup.

---

## 4. Drive báo Unallocated

Unallocated nghĩa là vùng storage chưa thuộc partition hiện tại.

Nếu là ổ mới:

- Create partition.
- Format.
- Assign drive letter.

Nếu là ổ cũ có dữ liệu:

> Không tự ý tạo partition mới hoặc format.

---

## 5. Drive Full

SSD/HDD gần đầy có thể gây:

- Thiếu không gian.
- Giảm hiệu năng.
- Windows update lỗi.
- Application lỗi.
- Không thể tạo file tạm.

Xử lý:

1. Xóa file không cần.
2. Di chuyển archive.
3. Uninstall application không dùng.
4. Dọn temporary files.
5. Mở rộng partition nếu phù hợp.
6. Upgrade storage.

---

## 6. SSD chạy chậm

Nguyên nhân:

- Drive gần đầy.
- Thermal throttling.
- Background workload.
- Firmware.
- Health degradation.
- Benchmark cache behavior.
- SATA limitation.
- PCIe lane limitation.
- Wrong M.2 configuration.
- Low free space.

Kiểm tra:

1. Health.
2. Temperature.
3. Free space.
4. Interface.
5. Benchmark.
6. Firmware.
7. Background tasks.

---

## 7. NVMe quá nóng

Nguyên nhân:

- Heatsink không có.
- Thermal pad tiếp xúc kém.
- Airflow kém.
- SSD nằm dưới GPU.
- Workload nặng.
- Firmware behavior.

Xử lý:

- Kiểm tra heatsink.
- Kiểm tra thermal pad.
- Cải thiện airflow.
- Cập nhật firmware khi phù hợp.
- Kiểm tra temperature.

---

## 8. HDD phát tiếng Click

Nếu HDD phát tiếng click bất thường:

> Xem đây là dấu hiệu cảnh báo nghiêm trọng.

Không nên:

- Tiếp tục benchmark nhiều lần.
- Chạy repair tool liên tục.
- Reformat trước khi backup.

Ưu tiên:

1. Backup.
2. Clone.
3. Thay drive.

---

## 9. HDD bad sector

Nếu số sector lỗi tăng:

- Backup dữ liệu.
- Kiểm tra SMART.
- Kiểm tra filesystem.
- Đánh giá khả năng thay ổ.

Nếu ổ dùng cho dữ liệu quan trọng:

> Không tiếp tục sử dụng như storage chính chỉ vì "vẫn còn đọc được".

---

## 10. SSD Health Warning

Nếu SSD báo warning:

1. Backup.
2. Ghi SMART.
3. Kiểm tra firmware.
4. Kiểm tra temperature.
5. Kiểm tra error counters.
6. Đánh giá warranty.
7. Chuẩn bị replacement.

---

## 11. BSOD liên quan storage

Một số lỗi có thể liên quan:

- Disk I/O
- Storage driver
- Filesystem
- SSD/HDD failure
- Controller
- Cable
- Power

Không nên kết luận BSOD = storage lỗi.

Cần kiểm tra:

- Event Viewer
- Reliability Monitor
- SMART
- Minidump
- Driver
- Filesystem

---

## 12. File bị corrupt

Có thể do:

- Bad sectors
- SSD failure
- RAM errors
- Power loss
- Filesystem corruption
- Unsafe shutdown
- Software issue

Quy trình:

1. Backup dữ liệu còn đọc được.
2. Check health.
3. Check filesystem.
4. Check RAM nếu lỗi không giải thích được.
5. Check PSU/power.
6. Replace storage nếu cần.

---

## 13. Copy file bị lỗi

Nếu copy file lỗi:

1. Thử file khác.
2. Thử destination khác.
3. Kiểm tra source drive.
4. Kiểm tra destination drive.
5. Kiểm tra cable.
6. Kiểm tra SMART.
7. Kiểm tra filesystem.

---

## 14. Disk 100% Usage

Windows có thể báo Disk 100%.

Điều này không nhất thiết có nghĩa:

> Disk đã hỏng.

Có thể do:

- HDD chậm.
- Windows Update.
- Antivirus.
- Search indexing.
- Application.
- Paging.
- Background process.

Cần kiểm tra:

- Task Manager
- Resource Monitor
- Process I/O
- Storage health
- Disk latency

---

## 15. Storage Troubleshooting Decision Tree

### Step 1

Drive có được BIOS nhận không?

**Không:**

- Cable
- Power
- Slot
- BIOS
- Drive
- Motherboard

**Có:**

→ Sang Step 2.

### Step 2

OS có nhận không?

**Không:**

- Driver
- Controller
- Disk Management
- Partition
- Filesystem

**Có:**

→ Sang Step 3.

### Step 3

Health có tốt không?

**Không:**

→ Backup + replace.

**Có:**

→ Sang Step 4.

### Step 4

Performance có bất thường không?

Kiểm tra:

- Temperature
- Free space
- Interface
- Firmware
- Background workload
- Benchmark

---

## 16. Nguyên tắc xử lý dữ liệu

Khi nghi storage sắp chết:

> Data first, repair later.

Ưu tiên:

1. Backup.
2. Clone.
3. Verify data.
4. Diagnose.
5. Replace.
6. Restore.

---

# 🇬🇧 English

## 1. Goal

The goal of storage troubleshooting is to determine whether the problem is caused by:

- Drive
- Cable
- Power
- Motherboard
- Slot
- Controller
- Firmware
- Operating system
- Filesystem

Do not immediately conclude that the drive itself is defective.

---

## 2. Drive Not Detected

Check:

1. Power.
2. Cable.
3. Drive seating.
4. SATA port.
5. M.2 slot.
6. BIOS.
7. Storage configuration.
8. Another system.
9. Another known-good drive.

---

## 3. BIOS Detects Drive but Windows Does Not

Check:

- Disk Management
- Device Manager
- Disk status
- Drivers
- Partition
- Filesystem
- Drive letter
- Offline/online status

Do not format a drive containing important data.

---

## 4. Unallocated Drive

For a new empty drive:

- Create partition.
- Format.
- Assign drive letter.

For an existing data drive:

> Do not immediately create a new partition or format it.

---

## 5. Drive Is Full

A nearly full drive can cause:

- Low free space
- Application errors
- Update failures
- Temporary-file problems
- Reduced performance in some workloads

Solutions:

- Remove unnecessary files.
- Move archives.
- Uninstall unused applications.
- Clean temporary data.
- Expand the partition if appropriate.
- Upgrade storage.

---

## 6. SSD Is Slow

Possible causes:

- Low free space
- Thermal throttling
- Background workloads
- Firmware
- Health degradation
- Cache behavior
- SATA limitation
- PCIe limitation
- Incorrect M.2 configuration

Check:

1. Health.
2. Temperature.
3. Free space.
4. Interface.
5. Benchmark.
6. Firmware.
7. Background activity.

---

## 7. NVMe Overheating

Possible causes:

- No heatsink
- Poor thermal-pad contact
- Poor airflow
- GPU heat
- Heavy workload
- Firmware behavior

Solutions:

- Check heatsink installation.
- Check thermal pad contact.
- Improve airflow.
- Check firmware.
- Monitor temperature.

---

## 8. HDD Clicking

Abnormal clicking should be treated as a serious warning.

Avoid:

- Repeated benchmarking.
- Repeated repair attempts.
- Formatting before backup.

Priority:

1. Back up.
2. Clone.
3. Replace the drive.

---

## 9. Bad Sectors

If bad-sector indicators are increasing:

1. Back up data.
2. Review SMART.
3. Check filesystem.
4. Evaluate drive replacement.

---

## 10. SSD Health Warning

Recommended response:

1. Back up data.
2. Record health information.
3. Check firmware.
4. Check temperature.
5. Review error counters.
6. Check warranty.
7. Prepare a replacement.

---

## 11. Storage-Related BSOD

Possible causes include:

- Storage failure
- Storage drivers
- Filesystem corruption
- Controller issues
- Cable problems
- Power problems

A BSOD does not automatically prove that the storage drive is defective.

Check:

- Event Viewer
- Reliability Monitor
- SMART
- Minidumps
- Drivers
- Filesystem

---

## 12. Corrupted Files

Possible causes:

- Bad sectors
- SSD failure
- RAM errors
- Power loss
- Filesystem corruption
- Unsafe shutdown
- Software problems

Procedure:

1. Back up readable data.
2. Check drive health.
3. Check filesystem.
4. Test RAM if necessary.
5. Check power.
6. Replace storage if required.

---

## 13. Copy Errors

Check:

1. Source file.
2. Destination.
3. Source drive.
4. Destination drive.
5. Cable.
6. SMART.
7. Filesystem.

---

## 14. Disk 100% Usage

100% disk usage in Windows does not automatically mean that the drive is failing.

Possible causes:

- Slow HDD
- Windows Update
- Antivirus
- Search indexing
- Applications
- Paging
- Background processes

Check:

- Task Manager
- Resource Monitor
- I/O activity
- Storage health
- Disk latency

---

## 15. Troubleshooting Decision Tree

### Step 1 – BIOS Detection

If the drive is not detected:

- Power
- Cable
- Slot
- BIOS
- Drive
- Motherboard

If detected, continue.

### Step 2 – OS Detection

If the OS does not detect it:

- Driver
- Controller
- Disk Management
- Partition
- Filesystem

If detected, continue.

### Step 3 – Health

If health is poor:

> Back up and replace.

If health is good, continue.

### Step 4 – Performance

Check:

- Temperature
- Free space
- Interface
- Firmware
- Background workload
- Benchmark

---

## 16. Data Protection Principle

When storage failure is suspected:

> Data first, repair later.

Recommended priority:

1. Back up.
2. Clone.
3. Verify the data.
4. Diagnose.
5. Replace.
6. Restore.
