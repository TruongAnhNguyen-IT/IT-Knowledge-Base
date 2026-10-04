
# Storage Testing

## 🇻🇳 Tiếng Việt

## 1. Mục đích

Storage Testing dùng để xác định:

- Drive có được nhận không.
- Dung lượng có đúng không.
- Health có ổn không.
- Có lỗi đọc/ghi không.
- Có bad sector không.
- Performance có bất thường không.
- Nhiệt độ có quá cao không.

---

## 2. Testing Workflow

Quy trình chuẩn:

1. Physical inspection
2. BIOS detection
3. OS detection
4. Capacity verification
5. SMART/Health check
6. Temperature check
7. Read test
8. Write test
9. Performance test
10. Filesystem test
11. Long-duration test
12. Documentation

---

## 3. Physical Inspection

Kiểm tra:

### HDD

- Connector
- PCB
- Screw
- Physical damage
- Bent connector
- Abnormal noise

### SATA SSD

- SATA connector
- PCB
- Enclosure
- Physical damage

### NVMe

- M.2 edge connector
- PCB
- NAND/controller area
- Screw
- Heatsink
- Thermal pad

---

## 4. BIOS/UEFI Test

Kiểm tra:

- Drive model.
- Capacity.
- Interface.
- NVMe detection.
- SATA detection.

Nếu BIOS không nhận:

> Chưa nên tập trung vào Windows trước.

Cần kiểm tra hardware, slot, cable, firmware và BIOS configuration.

---

## 5. Windows Testing

### Disk Management

Mở:

`diskmgmt.msc`

Kiểm tra:

- Disk number
- Capacity
- Partition
- File system
- Online/Offline
- Unallocated space

### Device Manager

Kiểm tra:

`devmgmt.msc`

Có thể kiểm tra:

- Disk drives
- Storage controllers

---

## 6. PowerShell

Có thể sử dụng:

`Get-PhysicalDisk`

Hoặc:

`Get-CimInstance Win32_DiskDrive`

Mục tiêu:

- Model
- Serial
- Capacity
- Interface
- Status

---

## 7. Linux Testing

Các lệnh hữu ích:

`lsblk`

`sudo smartctl -a /dev/sdX`

`sudo nvme smart-log /dev/nvme0`

`df -h`

`sudo fdisk -l`

Các lệnh phụ thuộc vào package/tool được cài đặt.

---

## 8. SMART Test

SMART có thể dùng để kiểm tra:

- Temperature
- Error counters
- Power-on hours
- Bad sectors
- Percentage used
- Media errors

Không nên chỉ đọc một giá trị "Health".

---

## 9. Read Test

Read test kiểm tra khả năng đọc dữ liệu.

Có thể dùng:

- Manufacturer diagnostic tool
- SMART self-test
- Disk utility
- Read benchmark

Với HDD nghi lỗi:

> Không nên chạy stress test trước khi bảo vệ dữ liệu quan trọng.

---

## 10. Write Test

Write test có thể làm thay đổi hoặc xóa dữ liệu.

Trước khi test:

> Xác nhận drive có dữ liệu quan trọng hay không.

Đối với drive trống:

- Sequential write
- Random write
- Full-drive test

Đối với drive đang sử dụng:

- Không tự ý destructive test.

---

## 11. Benchmark

Các chỉ số:

- Sequential Read
- Sequential Write
- Random Read
- Random Write
- IOPS
- Latency

Benchmark nên được thực hiện:

1. Khi drive ổn định.
2. Không có workload khác.
3. Với dung lượng test phù hợp.
4. Ghi nhận nhiệt độ.
5. So sánh với specification.

---

## 12. NVMe Temperature Test

Quy trình:

1. Idle temperature.
2. Start benchmark.
3. Monitor temperature.
4. Observe performance.
5. Check thermal throttling.
6. Stop if temperature becomes unsafe.

---

## 13. HDD Surface Test

Có thể kiểm tra surface để phát hiện:

- Slow sectors
- Read errors
- Bad sectors

Nhưng nếu HDD chứa dữ liệu quan trọng:

> Backup trước.

---

## 14. Testing One Drive vs System

Khi troubleshooting:

### Drive test

Test riêng drive.

### System test

Test:

- Motherboard
- Cable
- M.2 slot
- SATA controller
- PSU
- OS
- Drivers

Mục tiêu là xác định:

> Drive lỗi hay hệ thống kết nối với drive lỗi.

---

## 15. Test Report

Nên ghi:

| Field | Result |
|---|---|
| Drive Model | |
| Serial Number | |
| Capacity | |
| Interface | |
| Firmware | |
| Health | |
| Temperature | |
| SMART | |
| Read Test | |
| Write Test | |
| Benchmark | |
| Errors | |
| Final Status | |

---

# 🇬🇧 English

## 1. Purpose

Storage testing determines:

- Whether the drive is detected.
- Whether capacity is correct.
- Whether health is acceptable.
- Whether read/write errors exist.
- Whether bad sectors exist.
- Whether performance is abnormal.
- Whether temperatures are excessive.

---

## 2. Testing Workflow

1. Physical inspection
2. BIOS detection
3. OS detection
4. Capacity verification
5. SMART/health check
6. Temperature check
7. Read test
8. Write test
9. Performance test
10. Filesystem test
11. Long-duration testing
12. Documentation

---

## 3. Physical Inspection

Check:

- Connectors
- PCB
- Mounting
- Physical damage
- Bent connectors
- Heatsink installation
- Abnormal noises

---

## 4. BIOS/UEFI Test

Verify:

- Drive model
- Capacity
- Interface
- SATA detection
- NVMe detection

If the drive is not detected in BIOS, investigate the hardware and firmware path before troubleshooting Windows.

---

## 5. Windows Testing

Use:

`diskmgmt.msc`

Check:

- Disk number
- Capacity
- Partitions
- Filesystem
- Online/offline state
- Unallocated space

Use:

`devmgmt.msc`

to inspect:

- Disk drives
- Storage controllers

---

## 6. PowerShell

Useful commands include:

`Get-PhysicalDisk`

and:

`Get-CimInstance Win32_DiskDrive`

These can provide drive information such as model, capacity, and status.

---

## 7. Linux Testing

Useful commands:

`lsblk`

`sudo smartctl -a /dev/sdX`

`sudo nvme smart-log /dev/nvme0`

`df -h`

`sudo fdisk -l`

---

## 8. SMART Testing

Check:

- Temperature
- Error counters
- Power-on hours
- Bad sectors
- Percentage used
- Media errors

Do not rely only on a single health score.

---

## 9. Read Testing

Read tests verify whether data can be read reliably.

Possible tools include:

- Manufacturer diagnostics
- SMART self-tests
- Disk utilities
- Read benchmarks

Protect important data before performing intensive tests on a suspicious HDD.

---

## 10. Write Testing

Write tests may modify or destroy data.

Before testing:

> Confirm that the drive does not contain important data.

Avoid destructive tests on production drives unless the data has been safely backed up.

---

## 11. Benchmarking

Important metrics:

- Sequential read
- Sequential write
- Random read
- Random write
- IOPS
- Latency

Record:

- Test size
- Temperature
- Drive condition
- Background workload

---

## 12. NVMe Temperature Test

Procedure:

1. Record idle temperature.
2. Start benchmark.
3. Monitor temperature.
4. Observe performance.
5. Check for throttling.
6. Stop if temperatures become unsafe.

---

## 13. HDD Surface Test

Surface tests can identify:

- Slow sectors
- Read errors
- Bad sectors

Always protect important data before performing intensive surface testing.

---

## 14. Drive vs System Testing

A storage problem may originate from:

- Drive
- Motherboard
- SATA cable
- M.2 slot
- Storage controller
- PSU
- Driver
- Operating system

The goal is to isolate the actual fault domain.

---

## 15. Test Report

| Field | Result |
|---|---|
| Drive Model | |
| Serial Number | |
| Capacity | |
| Interface | |
| Firmware | |
| Health | |
| Temperature | |
| SMART | |
| Read Test | |
| Write Test | |
| Benchmark | |
| Errors | |
| Final Status | |
