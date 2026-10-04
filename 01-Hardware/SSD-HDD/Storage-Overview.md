
# Storage Overview

## 🇻🇳 Tiếng Việt

## 1. Giới thiệu

Storage là thành phần dùng để lưu trữ dữ liệu lâu dài trên máy tính. Khác với RAM, dữ liệu trên storage vẫn được giữ lại khi máy tính tắt nguồn.

Các loại storage phổ biến:

- HDD – Hard Disk Drive
- SATA SSD – Solid State Drive sử dụng giao tiếp SATA
- NVMe SSD – SSD sử dụng giao thức NVMe trên PCIe
- M.2 SSD – dạng vật lý, có thể là SATA hoặc NVMe
- External Storage – thiết bị lưu trữ gắn ngoài
- USB Flash Drive
- NAS Storage
- Enterprise Storage

Trong phạm vi tài liệu này tập trung vào:

- HDD
- SATA SSD
- NVMe SSD
- Storage Health
- Storage Testing
- Storage Troubleshooting

---

## 2. HDD là gì?

HDD (Hard Disk Drive) là thiết bị lưu trữ sử dụng các đĩa từ quay và đầu đọc/ghi cơ học.

Các thành phần chính:

- Platters
- Spindle Motor
- Read/Write Heads
- Actuator Arm
- Actuator
- PCB
- Firmware
- Cache

Dữ liệu được ghi lên bề mặt platter bằng từ tính.

### Đặc điểm

- Có bộ phận chuyển động.
- Có tiếng động cơ học.
- Nhạy cảm với va đập.
- Tốc độ thấp hơn SSD.
- Giá thành trên mỗi GB thường thấp.
- Phù hợp lưu trữ dung lượng lớn.

---

## 3. SSD là gì?

SSD (Solid State Drive) là thiết bị lưu trữ sử dụng bộ nhớ flash NAND để lưu dữ liệu.

SSD không sử dụng platter hoặc đầu đọc cơ học như HDD.

Các thành phần chính:

- NAND Flash
- Controller
- Firmware
- DRAM hoặc HMB tùy thiết kế
- Cache
- Power Management

### Đặc điểm

- Không có bộ phận chuyển động.
- Truy xuất dữ liệu nhanh.
- Độ trễ thấp.
- Hoạt động êm.
- Chống rung tốt hơn HDD.
- Có giới hạn ghi của NAND.

---

## 4. SATA SSD

SATA SSD sử dụng giao tiếp SATA.

SATA III có tốc độ liên kết lý thuyết 6 Gb/s và tốc độ truyền dữ liệu thực tế của SSD thường nằm quanh giới hạn khoảng 500–600 MB/s tùy thiết bị và hệ thống.

SATA SSD thường có hai dạng:

### 2.5-inch SATA SSD

Sử dụng:

- SATA Data cable
- SATA Power cable

Thường gặp trong:

- Desktop
- Laptop
- Mini PC
- NAS

### M.2 SATA SSD

Có hình dạng M.2 nhưng sử dụng giao tiếp SATA.

Điểm quan trọng:

> M.2 không đồng nghĩa với NVMe.

Cần kiểm tra motherboard/laptop hỗ trợ M.2 SATA hay M.2 NVMe.

---

## 5. NVMe SSD

NVMe (Non-Volatile Memory Express) là giao thức được thiết kế cho bộ nhớ flash và thường giao tiếp thông qua PCIe.

NVMe SSD có:

- Độ trễ thấp.
- Khả năng xử lý nhiều queue/command.
- Băng thông cao hơn SATA.
- Hiệu năng tốt trong workload lớn.

Các thế hệ PCIe phổ biến:

- PCIe Gen 3
- PCIe Gen 4
- PCIe Gen 5

Một NVMe SSD có thể sử dụng:

- PCIe x2
- PCIe x4
- PCIe lanes khác tùy thiết bị.

Hiệu năng thực tế phụ thuộc vào:

- PCIe generation
- Số lane
- Controller
- NAND
- Firmware
- Temperature
- Workload
- Thermal throttling
- Dung lượng còn trống

---

## 6. M.2 là gì?

M.2 là một form factor.

M.2 không phải là giao thức.

Một M.2 SSD có thể là:

- M.2 SATA
- M.2 NVMe

Do đó khi lắp SSD M.2 cần kiểm tra:

1. M.2 slot hỗ trợ giao thức nào.
2. Kích thước SSD.
3. Keying.
4. PCIe generation.
5. Số lane.
6. Hỗ trợ boot hay không.
7. BIOS/UEFI compatibility.

---

## 7. NAND Flash

NAND Flash là bộ nhớ không mất dữ liệu khi mất điện.

Một số loại NAND:

| Loại | Bits / Cell | Đặc điểm |
|---|---:|---|
| SLC | 1 | Hiệu năng và endurance cao |
| MLC | 2 | Cân bằng tốt |
| TLC | 3 | Phổ biến |
| QLC | 4 | Mật độ cao, giá/GB tốt |

Không nên chỉ dựa vào loại NAND để đánh giá SSD.

Cần xem thêm:

- Controller
- TBW
- Warranty
- Random I/O
- Sustained write
- Cache
- Thermal behavior
- Firmware

---

## 8. DRAM Cache và HMB

Một số SSD có DRAM riêng để lưu bảng ánh xạ dữ liệu.

Một số SSD DRAM-less sử dụng HMB (Host Memory Buffer) để sử dụng một phần RAM hệ thống cho mục đích quản lý dữ liệu.

DRAM-less không đồng nghĩa với SSD kém.

Hiệu năng phụ thuộc vào toàn bộ thiết kế SSD.

---

## 9. Sequential và Random Performance

### Sequential

Đọc/ghi các vùng dữ liệu liên tiếp.

Ví dụ:

- Copy file ISO lớn.
- Video.
- Backup.
- File database lớn.

### Random

Đọc/ghi các block dữ liệu ở các vị trí khác nhau.

Quan trọng đối với:

- Operating System
- Application
- Database
- Virtual Machine
- Development environment

Các thông số thường gặp:

- Sequential Read
- Sequential Write
- Random Read
- Random Write
- IOPS
- Latency

---

## 10. IOPS

IOPS = Input/Output Operations Per Second.

IOPS biểu thị số lượng thao tác I/O mà storage có thể xử lý trong một giây.

IOPS đặc biệt quan trọng đối với:

- Database
- VM
- Server
- Application workloads
- Random workloads

---

## 11. Latency

Latency là thời gian hệ thống cần để hoàn thành một thao tác I/O.

Latency càng thấp thì storage phản hồi càng nhanh.

SSD thường có latency thấp hơn HDD do không phải di chuyển đầu đọc cơ học.

---

## 12. TBW và Endurance

TBW = Terabytes Written.

TBW thể hiện lượng dữ liệu ghi được mà nhà sản xuất sử dụng làm chỉ số endurance của SSD.

Ví dụ:

> SSD có TBW 600 TB

Không có nghĩa ổ sẽ chắc chắn hỏng ngay sau khi ghi đúng 600 TB.

TBW là thông số endurance/warranty theo thiết kế và điều kiện của nhà sản xuất.

Các yếu tố khác:

- NAND type
- Write amplification
- Temperature
- Workload
- Power loss
- Firmware

---

## 13. TRIM

TRIM cho phép hệ điều hành thông báo cho SSD rằng các block dữ liệu không còn được sử dụng.

SSD có thể sử dụng thông tin này cho:

- Garbage Collection
- Reclaim blocks
- Giảm write amplification
- Duy trì hiệu năng

TRIM khác với việc "xóa file ngay lập tức khỏi NAND".

TRIM là một phần của cơ chế quản lý storage và phụ thuộc vào OS, controller, filesystem và đường truyền.

---

## 14. SMART

SMART = Self-Monitoring, Analysis and Reporting Technology.

SMART cung cấp thông tin giúp theo dõi tình trạng storage và phát hiện các dấu hiệu bất thường.

Các thông tin có thể gặp:

- Temperature
- Power-On Hours
- Power Cycle Count
- Reallocated Sector Count
- Pending Sector
- Uncorrectable Errors
- Percentage Used
- Available Spare
- Media Errors
- Unsafe Shutdowns
- Total Host Writes

Không phải mọi ổ đều có cùng bộ SMART attributes.

---

## 15. HDD vs SATA SSD vs NVMe SSD

| Tiêu chí | HDD | SATA SSD | NVMe SSD |
|---|---|---|---|
| Công nghệ | Magnetic | NAND Flash | NAND Flash |
| Bộ phận chuyển động | Có | Không | Không |
| Giao tiếp | SATA | SATA | PCIe |
| Protocol | ATA/SATA | SATA/AHCI | NVMe |
| Độ trễ | Cao | Thấp | Rất thấp |
| Tốc độ | Thấp | Trung bình | Cao |
| Giá/GB | Thấp | Trung bình | Trung bình/Cao |
| Chống rung | Thấp | Cao | Cao |
| OS Drive | Có thể | Tốt | Rất tốt |
| Backup lớn | Tốt | Có | Có |
| VM | Hạn chế | Tốt | Rất tốt |

---

## 16. Quy trình xử lý storage trong IT Support

Quy trình cơ bản:

1. Identify storage.
2. Check interface.
3. Check capacity.
4. Check health.
5. Check temperature.
6. Check SMART.
7. Test read/write.
8. Check filesystem.
9. Check cable/slot.
10. Check BIOS/UEFI detection.
11. Check OS detection.
12. Backup important data.
13. Troubleshoot.
14. Retest.
15. Document result.

---

## 17. Best Practices

- Không tháo HDD khi đang hoạt động nếu không phải hot-swap.
- Không để HDD bị va đập khi đang quay.
- Không sử dụng SSD gần đầy liên tục.
- Theo dõi SMART.
- Theo dõi nhiệt độ NVMe.
- Backup dữ liệu quan trọng.
- Không coi SMART "Good" là đảm bảo ổ chắc chắn không hỏng.
- Không chạy benchmark nặng trên ổ đang có dấu hiệu lỗi trước khi backup dữ liệu.
- Khi nghi ngờ storage failure, ưu tiên bảo toàn dữ liệu trước khi sửa chữa.

---

# 🇬🇧 English

## 1. Introduction

Storage is the component used to retain data persistently.

Unlike RAM, storage keeps data when the computer is powered off.

Common storage technologies include:

- HDD
- SATA SSD
- NVMe SSD
- M.2 SSD
- External storage
- USB flash storage
- NAS
- Enterprise storage

This documentation focuses on HDD, SATA SSD, NVMe SSD, health monitoring, testing, and troubleshooting.

---

## 2. HDD

HDD stands for Hard Disk Drive.

It stores data magnetically on rotating platters.

Main components:

- Platters
- Spindle motor
- Read/write heads
- Actuator arm
- Actuator
- PCB
- Firmware
- Cache

HDDs contain moving mechanical components and are therefore more sensitive to shock and vibration.

---

## 3. SSD

SSD stands for Solid State Drive.

It uses NAND flash instead of rotating magnetic platters.

Main components may include:

- NAND flash
- Controller
- Firmware
- DRAM
- HMB
- Cache
- Power-management circuitry

SSDs generally provide lower latency, higher performance, and better resistance to vibration than HDDs.

---

## 4. SATA SSD

SATA SSDs communicate through the SATA interface.

Common form factors:

- 2.5-inch SATA SSD
- M.2 SATA SSD

A 2.5-inch SATA SSD normally requires:

- SATA data cable
- SATA power cable

An M.2 SATA SSD uses the M.2 physical form factor but communicates using SATA.

---

## 5. NVMe SSD

NVMe stands for Non-Volatile Memory Express.

It is a storage protocol designed for flash storage and commonly operates over PCIe.

Common PCIe generations:

- Gen 3
- Gen 4
- Gen 5

Performance depends on:

- PCIe generation
- Lane configuration
- Controller
- NAND
- Firmware
- Temperature
- Workload
- Available capacity
- Thermal throttling

---

## 6. M.2

M.2 is a physical form factor, not a storage protocol.

An M.2 drive may use:

- SATA
- NVMe/PCIe

Always check motherboard or laptop specifications before installation.

---

## 7. NAND Flash

Common NAND types:

- SLC
- MLC
- TLC
- QLC

NAND type alone should not be used to judge overall SSD quality.

Other important specifications include:

- Controller
- TBW
- Random performance
- Sustained write performance
- Firmware
- Thermal behavior
- Warranty

---

## 8. DRAM and HMB

Some SSDs contain dedicated DRAM.

DRAM-less SSDs may use HMB to use a portion of system RAM for certain mapping operations.

DRAM-less does not automatically mean low quality.

---

## 9. Sequential and Random Performance

Sequential performance involves accessing data continuously.

Typical workloads:

- Large file transfers
- Video files
- Backups

Random performance involves accessing data across different locations.

It is particularly important for:

- Operating systems
- Applications
- Databases
- Virtual machines

---

## 10. IOPS

IOPS means Input/Output Operations Per Second.

It represents how many I/O operations a storage device can process per second.

It is especially important for random workloads.

---

## 11. Latency

Latency is the time required to complete an I/O operation.

Lower latency generally means faster storage response.

---

## 12. TBW

TBW means Terabytes Written.

It is commonly used as an SSD endurance metric.

TBW should be interpreted together with:

- NAND type
- Controller
- Workload
- Temperature
- Firmware
- Write amplification

---

## 13. TRIM

TRIM allows the operating system to inform an SSD which storage blocks are no longer needed.

The SSD can then use this information for garbage collection and block management.

TRIM is different from simply deleting a file.

---

## 14. SMART

SMART stands for Self-Monitoring, Analysis and Reporting Technology.

It provides health and diagnostic information.

Common metrics include:

- Temperature
- Power-on hours
- Power cycles
- Reallocated sectors
- Pending sectors
- Uncorrectable errors
- Percentage used
- Available spare
- Media errors
- Unsafe shutdowns
- Host writes

SMART fields vary between drive models and vendors.

---

## 15. Storage Comparison

| Feature | HDD | SATA SSD | NVMe SSD |
|---|---|---|---|
| Technology | Magnetic | NAND Flash | NAND Flash |
| Moving parts | Yes | No | No |
| Interface | SATA | SATA | PCIe |
| Protocol | ATA/SATA | SATA/AHCI | NVMe |
| Latency | High | Low | Very low |
| Performance | Low | Medium | High |
| Cost/GB | Low | Medium | Medium/High |
| Shock resistance | Lower | High | High |
| OS drive | Possible | Good | Excellent |
| VM workload | Limited | Good | Excellent |

---

## 16. Storage Troubleshooting Workflow

1. Identify the drive.
2. Identify the interface.
3. Verify capacity.
4. Check health.
5. Check temperature.
6. Review SMART.
7. Test read/write performance.
8. Check filesystem.
9. Check cables and slots.
10. Check BIOS/UEFI.
11. Check operating-system detection.
12. Back up important data.
13. Troubleshoot.
14. Retest.
15. Document the result.

---

## 17. Best Practices

- Avoid physical shocks to HDDs.
- Monitor SSD health.
- Monitor NVMe temperature.
- Keep important data backed up.
- Do not assume a SMART "Good" status guarantees future reliability.
- Prioritize data preservation when a drive shows signs of failure.
- Document storage failures and test results.
