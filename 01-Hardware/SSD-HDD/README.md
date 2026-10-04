
# SSD-HDD – Storage Knowledge Base

## 🇻🇳 Tiếng Việt

## 1. Giới thiệu

Thư mục `SSD-HDD` chứa tài liệu về các thiết bị lưu trữ được sử dụng trong máy tính, laptop, workstation và hệ thống IT.

Mục tiêu của thư mục:

- Hiểu nguyên lý storage.
- Phân biệt HDD, SATA SSD và NVMe SSD.
- Hiểu M.2, SATA, PCIe và NVMe.
- Kiểm tra storage.
- Đánh giá storage health.
- Troubleshoot storage.
- Thực hành quy trình IT Support.

---

## 2. Cấu trúc thư mục

```text
SSD-HDD/
├── HDD.md
├── README.md
├── SSD-NVMe.md
├── SSD-SATA.md
├── Storage-Health.md
├── Storage-Overview.md
├── Storage-Testing.md
└── Storage-Troubleshooting.md
```

---

## 3. Danh sách tài liệu

### [Storage Overview](./Storage-Overview.md)

Tổng quan về:

- Storage
- HDD
- SSD
- SATA
- NVMe
- M.2
- NAND
- DRAM
- HMB
- IOPS
- Latency
- TBW
- TRIM
- SMART

### [HDD](./HDD.md)

Tài liệu về:

- HDD architecture
- Platters
- Read/write heads
- RPM
- Cache
- SATA
- Bad sectors
- SMART
- HDD failure symptoms
- HDD use cases

### [SATA SSD](./SSD-SATA.md)

Tài liệu về:

- SATA SSD
- 2.5-inch SSD
- M.2 SATA
- SATA III
- NAND
- Controller
- DRAM
- HMB
- TRIM
- SATA SSD health

### [NVMe SSD](./SSD-NVMe.md)

Tài liệu về:

- NVMe
- PCIe
- M.2
- PCIe generations
- PCIe lanes
- M.2 keying
- M.2 sizes
- NVMe controller
- Thermal throttling
- NVMe health

### [Storage Health](./Storage-Health.md)

Tập trung vào:

- SMART
- NVMe Health
- Temperature
- Error counters
- TBW
- Percentage Used
- Media errors
- Drive health assessment

### [Storage Testing](./Storage-Testing.md)

Tập trung vào:

- Physical inspection
- BIOS detection
- Windows detection
- Linux detection
- SMART testing
- Read testing
- Write testing
- Benchmark
- Temperature testing
- Test reporting

### [Storage Troubleshooting](./Storage-Troubleshooting.md)

Tập trung vào:

- Drive not detected
- BIOS vs OS detection
- Unallocated disk
- Drive full
- Slow SSD
- NVMe overheating
- HDD clicking
- Bad sectors
- File corruption
- Disk 100%
- Storage troubleshooting workflow

---

## 4. Storage Classification

| Storage | Technology | Interface | Typical Use |
|---|---|---|---|
| HDD | Magnetic | SATA | Backup, archive |
| SATA SSD | NAND Flash | SATA | OS, applications, secondary storage |
| NVMe SSD | NAND Flash | PCIe | OS, development, VM, high-performance workloads |

---

## 5. Important Concepts

### HDD

Mechanical magnetic storage.

### SSD

Solid-state flash storage.

### SATA

Storage interface used by HDDs and SATA SSDs.

### PCIe

High-speed interconnect used by NVMe SSDs.

### NVMe

Storage protocol designed for flash storage.

### M.2

Physical form factor.

### NAND

Non-volatile flash memory.

### SMART

Drive monitoring and diagnostic technology.

### TRIM

OS-to-SSD mechanism for identifying blocks that are no longer required.

### TBW

Terabytes Written endurance metric.

### IOPS

Input/Output Operations Per Second.

### Latency

Time required to complete an I/O operation.

---

## 6. Important Distinction

### M.2 ≠ NVMe

M.2 describes physical form factor.

NVMe describes a storage protocol.

Therefore:

- M.2 SATA exists.
- M.2 NVMe exists.

Always check motherboard/laptop specifications before purchasing or installing an M.2 drive.

---

## 7. Storage Troubleshooting Workflow

Quy trình chuẩn:

```text
Physical Inspection
        ↓
BIOS/UEFI Detection
        ↓
Operating System Detection
        ↓
Capacity Verification
        ↓
SMART / Health Check
        ↓
Temperature Check
        ↓
Read / Write Test
        ↓
Performance Test
        ↓
Troubleshooting
        ↓
Retest
        ↓
Documentation
```

---

## 8. Data Protection

Khi xử lý storage có dấu hiệu lỗi:

> DATA FIRST – REPAIR LATER

Không nên:

- Format ngay.
- Initialize ngay.
- Chạy benchmark liên tục.
- Chạy repair tool nhiều lần.
- Ghi dữ liệu mới lên ổ nghi lỗi.

Nên:

1. Backup.
2. Clone nếu cần.
3. Verify backup.
4. Diagnose.
5. Replace.
6. Restore.

---

## 9. IT Support Checklist

### Before Testing

- [ ] Identify drive model.
- [ ] Identify interface.
- [ ] Check capacity.
- [ ] Ask whether data is important.
- [ ] Check physical condition.
- [ ] Check BIOS detection.

### Health

- [ ] SMART checked.
- [ ] Temperature checked.
- [ ] Error counters checked.
- [ ] TBW/Percentage Used checked where applicable.
- [ ] Firmware checked.

### Performance

- [ ] Sequential read.
- [ ] Sequential write.
- [ ] Random read.
- [ ] Random write.
- [ ] IOPS.
- [ ] Latency.

### Troubleshooting

- [ ] Cable checked.
- [ ] Power checked.
- [ ] Slot checked.
- [ ] BIOS checked.
- [ ] Driver checked.
- [ ] Filesystem checked.
- [ ] Tested on another system.
- [ ] Known-good drive tested.

### Final

- [ ] Problem identified.
- [ ] Fix applied.
- [ ] Retest completed.
- [ ] Data verified.
- [ ] Result documented.

---

## 10. Documentation Standard

Mỗi lần kiểm tra storage thực tế nên ghi lại:

- Date
- Device
- Model
- Serial Number
- Capacity
- Interface
- Firmware
- Health
- Temperature
- SMART
- Test method
- Test result
- Error
- Root cause
- Solution
- Final status

---

## 11. Example Work Log

```text
Device:
Samsung / Kingston / WD / Seagate / etc.

Type:
HDD / SATA SSD / NVMe SSD

Capacity:
1 TB

Interface:
SATA / PCIe NVMe

Symptoms:
Drive intermittently disconnects.

Tests:
- BIOS detection: PASS
- Windows detection: PASS
- SMART: WARNING
- Temperature: Normal
- Read test: Errors detected

Root Cause:
Storage media degradation.

Action:
Backed up user data and recommended replacement.

Final Status:
Drive replacement required.
```

---

## 12. Learning Objectives

Sau khi hoàn thành thư mục này, có thể:

- Identify HDD and SSD types.
- Understand SATA and NVMe.
- Understand M.2.
- Understand PCIe generations.
- Understand NAND.
- Read basic SMART information.
- Test storage.
- Identify common storage failures.
- Troubleshoot storage detection issues.
- Troubleshoot performance issues.
- Protect user data.
- Write professional IT troubleshooting reports.

---

# 🇬🇧 English

## 1. Introduction

The `SSD-HDD` folder contains documentation about storage devices used in computers, laptops, workstations, and IT environments.

The objectives are to understand:

- Storage fundamentals.
- HDDs.
- SATA SSDs.
- NVMe SSDs.
- M.2.
- SATA.
- PCIe.
- Storage health.
- Storage testing.
- Storage troubleshooting.

---

## 2. Folder Structure

```text
SSD-HDD/
├── HDD.md
├── README.md
├── SSD-NVMe.md
├── SSD-SATA.md
├── Storage-Health.md
├── Storage-Overview.md
├── Storage-Testing.md
└── Storage-Troubleshooting.md
```

---

## 3. Documentation

### [Storage Overview](./Storage-Overview.md)

Covers:

- Storage
- HDD
- SSD
- SATA
- NVMe
- M.2
- NAND
- DRAM
- HMB
- IOPS
- Latency
- TBW
- TRIM
- SMART

### [HDD](./HDD.md)

Covers:

- HDD architecture
- Platters
- Read/write heads
- RPM
- Cache
- SATA
- Bad sectors
- SMART
- Failure symptoms
- Use cases

### [SATA SSD](./SSD-SATA.md)

Covers:

- SATA SSD
- 2.5-inch SSD
- M.2 SATA
- SATA III
- NAND
- Controller
- DRAM
- HMB
- TRIM
- Health monitoring

### [NVMe SSD](./SSD-NVMe.md)

Covers:

- NVMe
- PCIe
- M.2
- PCIe generations
- PCIe lanes
- M.2 keying
- M.2 sizes
- Controller
- Thermal throttling
- Health monitoring

### [Storage Health](./Storage-Health.md)

Covers:

- SMART
- NVMe health
- Temperature
- Error counters
- TBW
- Percentage used
- Media errors
- Health assessment

### [Storage Testing](./Storage-Testing.md)

Covers:

- Physical inspection
- BIOS detection
- Windows detection
- Linux detection
- SMART testing
- Read testing
- Write testing
- Benchmarking
- Temperature testing
- Test reports

### [Storage Troubleshooting](./Storage-Troubleshooting.md)

Covers:

- Drive not detected
- BIOS vs OS detection
- Unallocated disks
- Full drives
- Slow SSDs
- NVMe overheating
- HDD clicking
- Bad sectors
- File corruption
- Disk 100% usage
- Troubleshooting workflow

---

## 4. Storage Classification

| Storage | Technology | Interface | Typical Use |
|---|---|---|---|
| HDD | Magnetic | SATA | Backup, archive |
| SATA SSD | NAND Flash | SATA | OS, applications, secondary storage |
| NVMe SSD | NAND Flash | PCIe | OS, development, VM, high-performance workloads |

---

## 5. Important Concepts

### HDD

Mechanical magnetic storage.

### SSD

Solid-state flash storage.

### SATA

Storage interface used by HDDs and SATA SSDs.

### PCIe

High-speed interconnect commonly used by NVMe SSDs.

### NVMe

Storage protocol designed for flash storage.

### M.2

Physical form factor.

### NAND

Non-volatile flash memory.

### SMART

Storage monitoring and diagnostic technology.

### TRIM

Mechanism that allows the operating system to identify storage blocks that are no longer needed by the filesystem.

### TBW

Terabytes Written endurance metric.

### IOPS

Input/Output Operations Per Second.

### Latency

Time required to complete an I/O operation.

---

## 6. Important Distinction

### M.2 ≠ NVMe

M.2 describes the physical form factor.

NVMe describes the storage protocol.

Therefore:

- M.2 SATA exists.
- M.2 NVMe exists.

Always check the motherboard or laptop specifications before installation.

---

## 7. Storage Troubleshooting Workflow

```text
Physical Inspection
        ↓
BIOS/UEFI Detection
        ↓
Operating System Detection
        ↓
Capacity Verification
        ↓
SMART / Health Check
        ↓
Temperature Check
        ↓
Read / Write Test
        ↓
Performance Test
        ↓
Troubleshooting
        ↓
Retest
        ↓
Documentation
```

---

## 8. Data Protection

When a storage device shows signs of failure:

> DATA FIRST – REPAIR LATER

Avoid:

- Formatting immediately.
- Initializing immediately.
- Repeated benchmarking.
- Repeated repair operations.
- Writing unnecessary data to the failing drive.

Recommended order:

1. Back up.
2. Clone if necessary.
3. Verify the backup.
4. Diagnose.
5. Replace.
6. Restore.

---

## 9. IT Support Checklist

### Before Testing

- [ ] Identify drive model.
- [ ] Identify interface.
- [ ] Verify capacity.
- [ ] Confirm whether data is important.
- [ ] Inspect physical condition.
- [ ] Check BIOS detection.

### Health

- [ ] SMART checked.
- [ ] Temperature checked.
- [ ] Error counters checked.
- [ ] TBW/Percentage Used checked where applicable.
- [ ] Firmware checked.

### Performance

- [ ] Sequential read.
- [ ] Sequential write.
- [ ] Random read.
- [ ] Random write.
- [ ] IOPS.
- [ ] Latency.

### Troubleshooting

- [ ] Cable checked.
- [ ] Power checked.
- [ ] Slot checked.
- [ ] BIOS checked.
- [ ] Driver checked.
- [ ] Filesystem checked.
- [ ] Tested on another system.
- [ ] Known-good drive tested.

### Final

- [ ] Root cause identified.
- [ ] Fix applied.
- [ ] Retest completed.
- [ ] Data verified.
- [ ] Result documented.

---

## 10. Documentation Standard

For every real storage test, record:

- Date
- Device
- Model
- Serial number
- Capacity
- Interface
- Firmware
- Health
- Temperature
- SMART
- Test method
- Test result
- Error
- Root cause
- Solution
- Final status

---

## 11. Example Work Log

```text
Device:
Samsung / Kingston / WD / Seagate / etc.

Type:
HDD / SATA SSD / NVMe SSD

Capacity:
1 TB

Interface:
SATA / PCIe NVMe

Symptoms:
Drive intermittently disconnects.

Tests:
- BIOS detection: PASS
- Windows detection: PASS
- SMART: WARNING
- Temperature: Normal
- Read test: Errors detected

Root Cause:
Storage media degradation.

Action:
Backed up user data and recommended replacement.

Final Status:
Drive replacement required.
```

---

## 12. Learning Objectives

After completing this section, you should be able to:

- Identify HDD and SSD types.
- Understand SATA and NVMe.
- Understand M.2.
- Understand PCIe generations.
- Understand NAND flash.
- Read basic SMART information.
- Test storage devices.
- Identify common storage failures.
- Troubleshoot storage detection issues.
- Troubleshoot storage performance issues.
- Protect user data.
- Write professional IT troubleshooting reports.
