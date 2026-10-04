
# NVMe SSD

## 🇻🇳 Tiếng Việt

## 1. NVMe là gì?

NVMe = Non-Volatile Memory Express.

NVMe là giao thức được thiết kế cho storage sử dụng non-volatile memory, đặc biệt là NAND flash.

NVMe thường hoạt động trên PCIe thay vì SATA.

Điều này cho phép NVMe SSD đạt throughput và parallelism cao hơn SATA SSD.

---

## 2. NVMe không phải là M.2

Đây là điểm rất quan trọng.

- M.2 = form factor.
- NVMe = protocol.
- PCIe = interconnect/interface.

Một M.2 SSD có thể là:

- M.2 SATA
- M.2 NVMe

Vì vậy:

> Không phải mọi M.2 SSD đều là NVMe.

---

## 3. NVMe Form Factors

NVMe có thể xuất hiện dưới:

- M.2
- U.2
- PCIe Add-in Card
- Một số enterprise form factors

Trong PC/laptop phổ thông, M.2 NVMe là dạng phổ biến nhất.

---

## 4. PCIe Generations

Các thế hệ thường gặp:

- PCIe Gen 3
- PCIe Gen 4
- PCIe Gen 5

Băng thông tăng theo thế hệ.

Tuy nhiên SSD PCIe Gen 5 không tự động chạy ở Gen 5 nếu motherboard/CPU chỉ hỗ trợ Gen 4.

---

## 5. PCIe Lanes

NVMe SSD phổ biến sử dụng:

- PCIe x4

Một số thiết bị có thể dùng cấu hình khác.

Cần kiểm tra:

- CPU lanes
- Chipset lanes
- M.2 slot wiring
- PCIe generation

---

## 6. M.2 Keying

M.2 SSD có nhiều loại keying.

Phổ biến:

- B-key
- M-key
- B+M key

Keying giúp xác định khả năng tương thích vật lý, nhưng không nên chỉ dựa vào notch.

Phải đọc specification của motherboard/laptop.

---

## 7. M.2 Size

Kích thước thường gặp:

- 2230
- 2242
- 2260
- 2280
- 22110

Ví dụ:

> 2280 = 22 mm width × 80 mm length.

---

## 8. NVMe Controller

Controller thực hiện:

- NAND management
- Error correction
- Wear leveling
- Garbage collection
- Mapping
- Queue management
- Thermal management
- Encryption tùy thiết kế

---

## 9. NVMe Performance

Các thông số:

- Sequential Read
- Sequential Write
- Random Read
- Random Write
- IOPS
- Latency

NVMe đặc biệt có lợi trong:

- Large file transfer
- Video editing
- Virtual machines
- Database
- Software development
- Heavy multitasking
- High-I/O workloads

---

## 10. NVMe Thermal Throttling

NVMe SSD hiệu năng cao có thể sinh nhiều nhiệt.

Khi nhiệt độ tăng cao, firmware có thể giảm hiệu năng để bảo vệ thiết bị.

Dấu hiệu:

- Benchmark lần đầu nhanh.
- Benchmark sau chậm.
- Copy file lớn bị giảm tốc độ.
- Temperature tăng mạnh.

Giải pháp:

- Heatsink.
- Thermal pad đúng cách.
- Airflow.
- Không che kín M.2.
- Kiểm tra motherboard heatsink.

---

## 11. NVMe Health

Theo dõi:

- Critical Warning
- Temperature
- Available Spare
- Percentage Used
- Data Units Read
- Data Units Written
- Power Cycles
- Power-on Hours
- Unsafe Shutdowns
- Media and Data Integrity Errors

NVMe health information có các trường tiêu chuẩn hơn SATA SMART, mặc dù vendor vẫn có thể bổ sung thông tin riêng.

---

## 12. NVMe Not Detected

Kiểm tra:

1. M.2 slot.
2. SSD seating.
3. BIOS/UEFI.
4. PCIe generation.
5. M.2 slot configuration.
6. CPU/chipset lane sharing.
7. Disable/enable relevant BIOS storage settings.
8. Test SSD in another compatible system.
9. BIOS update if appropriate.

---

## 13. NVMe Installation

1. Power off.
2. Disconnect power.
3. Locate M.2 slot.
4. Check supported protocol and size.
5. Install standoff.
6. Insert SSD at angle.
7. Press SSD down.
8. Secure screw.
9. Install heatsink if applicable.
10. Boot.
11. Check BIOS.
12. Initialize/partition drive if necessary.
13. Test health and performance.

---

# 🇬🇧 English

## 1. What is NVMe?

NVMe stands for Non-Volatile Memory Express.

It is a storage protocol designed for non-volatile flash storage and commonly operates over PCIe.

NVMe provides greater parallelism and throughput than SATA-based storage.

---

## 2. NVMe Is Not the Same as M.2

Important distinction:

- M.2 = physical form factor.
- NVMe = storage protocol.
- PCIe = interconnect.

An M.2 drive can be:

- SATA
- NVMe

Therefore:

> Not every M.2 SSD is an NVMe SSD.

---

## 3. NVMe Form Factors

Common NVMe form factors include:

- M.2
- U.2
- PCIe add-in cards
- Enterprise form factors

M.2 is the most common format for consumer PCs and laptops.

---

## 4. PCIe Generations

Common generations:

- PCIe Gen 3
- PCIe Gen 4
- PCIe Gen 5

A Gen 5 SSD will not automatically operate at Gen 5 if the platform only supports Gen 4.

---

## 5. PCIe Lanes

Many consumer NVMe SSDs use:

- PCIe x4

Always check motherboard and CPU lane configuration.

---

## 6. M.2 Keying

Common key types include:

- B-key
- M-key
- B+M key

Physical keying alone is not enough to determine compatibility.

Always verify the motherboard specification.

---

## 7. M.2 Sizes

Common sizes:

- 2230
- 2242
- 2260
- 2280
- 22110

For example:

> 2280 = 22 mm × 80 mm.

---

## 8. NVMe Controller

The controller manages:

- NAND
- Error correction
- Wear leveling
- Garbage collection
- Address mapping
- Queue management
- Thermal behavior
- Encryption features

---

## 9. Performance

Important metrics:

- Sequential read
- Sequential write
- Random read
- Random write
- IOPS
- Latency

NVMe is especially useful for:

- Large file transfers
- Video editing
- Virtual machines
- Databases
- Software development
- Heavy multitasking
- High-I/O workloads

---

## 10. Thermal Throttling

High-performance NVMe drives can generate significant heat.

When temperatures become excessive, the controller may reduce performance.

Symptoms:

- First benchmark is fast.
- Later benchmarks become slower.
- Large file transfers slow down.
- Temperature increases significantly.

Solutions may include:

- Heatsink
- Correct thermal pad installation
- Better airflow
- Proper motherboard heatsink installation

---

## 11. Health Monitoring

Important NVMe health fields include:

- Critical Warning
- Temperature
- Available Spare
- Percentage Used
- Data Units Read
- Data Units Written
- Power Cycles
- Power-on Hours
- Unsafe Shutdowns
- Media and Data Integrity Errors

---

## 12. NVMe Not Detected

Check:

1. M.2 slot.
2. SSD seating.
3. BIOS/UEFI.
4. PCIe generation.
5. M.2 configuration.
6. PCIe lane sharing.
7. Storage settings.
8. Another compatible system.
9. BIOS update when appropriate.

---

## 13. Installation

1. Power off.
2. Disconnect power.
3. Locate the M.2 slot.
4. Verify supported protocol and size.
5. Install the standoff.
6. Insert the SSD at an angle.
7. Press it down.
8. Secure the screw.
9. Install the heatsink if required.
10. Boot the system.
11. Check BIOS.
12. Initialize/partition if necessary.
13. Test health and performance.
