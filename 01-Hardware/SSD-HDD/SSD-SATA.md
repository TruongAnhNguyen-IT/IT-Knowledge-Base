
# SATA SSD

## 🇻🇳 Tiếng Việt

## 1. SATA SSD là gì?

SATA SSD là SSD sử dụng NAND Flash và giao tiếp SATA.

SATA SSD nhanh hơn HDD trong hầu hết workload thông thường và không có bộ phận cơ học chuyển động.

SATA III có giới hạn liên kết lý thuyết 6 Gb/s, nên hiệu năng tuần tự của SATA SSD thường bị giới hạn quanh vùng 500–600 MB/s tùy hệ thống và drive.

---

## 2. Các dạng SATA SSD

### 2.1 2.5-inch SATA SSD

Có kích thước phổ biến 2.5-inch.

Cần:

- SATA data cable
- SATA power cable

### 2.2 M.2 SATA SSD

Có form factor M.2 nhưng giao tiếp SATA.

Không được nhầm với NVMe M.2.

---

## 3. SATA SSD Components

Một SATA SSD có thể gồm:

- NAND Flash
- Controller
- DRAM
- Firmware
- Cache
- Power management
- SATA interface

---

## 4. SATA Controller

Controller chịu trách nhiệm:

- Quản lý NAND.
- Mapping logical address.
- Error correction.
- Wear leveling.
- Garbage collection.
- TRIM handling.
- Data management.

---

## 5. NAND

Các loại phổ biến:

- TLC
- QLC

Một số sản phẩm có loại NAND khác tùy phân khúc.

Không nên chỉ nhìn NAND để đánh giá SSD.

---

## 6. DRAM SSD

SSD có DRAM riêng có thể sử dụng DRAM để lưu mapping table và hỗ trợ một số workload.

DRAM-less SSD có thể sử dụng HMB tùy thiết kế/platform.

---

## 7. SATA SSD Performance

Các thông số:

- Sequential Read
- Sequential Write
- Random Read
- Random Write
- IOPS
- Latency

Không nên chỉ nhìn Sequential Read.

Ví dụ một SSD có sequential read cao nhưng random performance thấp vẫn có thể cho trải nghiệm khác trong workload OS/database.

---

## 8. SATA SSD Installation

### Desktop 2.5-inch

1. Tắt máy.
2. Ngắt nguồn.
3. Lắp SSD.
4. Kết nối SATA power.
5. Kết nối SATA data.
6. Khởi động.
7. Kiểm tra BIOS.
8. Kiểm tra Disk Management.

### M.2 SATA

1. Kiểm tra M.2 slot.
2. Xác nhận slot hỗ trợ SATA.
3. Lắp SSD.
4. Bắt screw/standoff.
5. Kiểm tra BIOS.
6. Kiểm tra OS.

---

## 9. SATA SSD không nhận

Kiểm tra theo thứ tự:

1. SATA power.
2. SATA data.
3. SATA port.
4. BIOS.
5. Disk Management.
6. Device Manager.
7. Storage controller.
8. Cable khác.
9. Port khác.
10. SSD trên máy khác.

---

## 10. TRIM

TRIM giúp OS thông báo các block không còn được sử dụng.

SSD có thể dùng thông tin này để garbage collection và quản lý NAND hiệu quả hơn.

---

## 11. SATA SSD Health

Theo dõi:

- SMART
- Temperature
- Percentage Used
- TBW
- Media errors
- Unsafe shutdowns
- Power-on hours

Các SMART attribute có thể khác nhau tùy manufacturer/model.

---

## 12. Khi nào chọn SATA SSD?

SATA SSD phù hợp khi:

- Máy chỉ hỗ trợ SATA.
- Cần nâng cấp HDD.
- Cần storage phụ.
- NAS/desktop cần nhiều ổ.
- Không cần NVMe performance.

---

# 🇬🇧 English

## 1. What is a SATA SSD?

A SATA SSD is a solid-state drive using NAND flash and the SATA interface.

It has no mechanical moving parts and is significantly faster than HDDs for many workloads.

SATA III has a 6 Gb/s link limit, which generally limits SATA SSD sequential performance to roughly the 500–600 MB/s range depending on the drive and system.

---

## 2. SATA SSD Form Factors

Common formats:

- 2.5-inch SATA SSD
- M.2 SATA SSD

M.2 is a physical form factor and does not automatically mean NVMe.

---

## 3. Components

A SATA SSD may contain:

- NAND flash
- Controller
- DRAM
- Firmware
- Cache
- Power-management circuitry
- SATA interface

---

## 4. Controller

The controller manages:

- NAND mapping
- Error correction
- Wear leveling
- Garbage collection
- TRIM
- Data management
- Flash translation layer

---

## 5. NAND

Common NAND types include:

- TLC
- QLC

NAND type should be evaluated together with controller, firmware, endurance, performance, and warranty.

---

## 6. DRAM

DRAM can be used for mapping information and caching.

DRAM-less SSDs may use HMB depending on platform and implementation.

---

## 7. Performance

Important metrics:

- Sequential read
- Sequential write
- Random read
- Random write
- IOPS
- Latency

Sequential speed alone does not fully represent real-world performance.

---

## 8. Installation

### 2.5-inch SATA SSD

1. Power off the computer.
2. Disconnect power.
3. Mount the SSD.
4. Connect SATA power.
5. Connect SATA data.
6. Boot the computer.
7. Check BIOS.
8. Check Disk Management.

### M.2 SATA

1. Verify M.2 slot support.
2. Confirm SATA support.
3. Install the drive.
4. Secure it.
5. Check BIOS.
6. Check the operating system.

---

## 9. SATA SSD Not Detected

Check:

1. Power cable.
2. Data cable.
3. SATA port.
4. BIOS.
5. Disk Management.
6. Device Manager.
7. Storage controller.
8. Another cable.
9. Another port.
10. Another computer.

---

## 10. TRIM

TRIM allows the operating system to identify storage blocks that are no longer required.

The SSD can use this information for garbage collection and NAND management.

---

## 11. Health Monitoring

Monitor:

- SMART
- Temperature
- Percentage used
- TBW
- Media errors
- Unsafe shutdowns
- Power-on hours

SMART attributes vary by vendor and model.

---

## 12. When to Choose SATA SSD

SATA SSD is a good choice when:

- The system only supports SATA.
- Replacing an HDD.
- Adding secondary storage.
- Expanding NAS or desktop storage.
- NVMe performance is unnecessary.
