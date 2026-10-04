
# HDD – Hard Disk Drive

## 🇻🇳 Tiếng Việt

## 1. HDD là gì?

HDD (Hard Disk Drive) là thiết bị lưu trữ dữ liệu sử dụng công nghệ từ tính.

HDD lưu dữ liệu trên các platter quay với tốc độ cao.

Khác với SSD, HDD có nhiều bộ phận cơ học chuyển động.

---

## 2. Cấu tạo HDD

### 2.1 Platters

Platters là các đĩa từ dùng để lưu dữ liệu.

Dữ liệu được ghi trên bề mặt platter.

### 2.2 Spindle Motor

Motor làm platter quay.

Tốc độ thường gặp:

- 5400 RPM
- 7200 RPM

Một số HDD enterprise có tốc độ cao hơn.

### 2.3 Read/Write Head

Đầu đọc/ghi dùng để đọc hoặc ghi dữ liệu lên platter.

### 2.4 Actuator Arm

Cánh tay cơ học di chuyển đầu đọc/ghi tới vị trí cần thiết.

### 2.5 Actuator

Điều khiển chuyển động của actuator arm.

### 2.6 PCB

PCB điều khiển:

- Motor
- Head
- Communication
- Power
- Firmware

---

## 3. Form Factor

### 3.1 3.5-inch HDD

Phổ biến trong:

- Desktop
- Server
- NAS

### 3.2 2.5-inch HDD

Phổ biến trong:

- Laptop
- External enclosure
- Một số mini PC

---

## 4. RPM

RPM = Revolutions Per Minute.

RPM càng cao thường giúp giảm thời gian chờ quay và cải thiện access performance, nhưng không phải là yếu tố duy nhất quyết định hiệu năng.

Ví dụ:

- 5400 RPM
- 7200 RPM

HDD 7200 RPM thường nhanh hơn HDD 5400 RPM trong nhiều workload, nhưng còn phụ thuộc:

- Areal density
- Cache
- Firmware
- Seek time
- Interface
- Workload

---

## 5. HDD Cache

HDD có thể sử dụng bộ nhớ cache trên drive.

Cache giúp xử lý một số thao tác đọc/ghi tạm thời.

Dung lượng cache không nên được dùng làm tiêu chí duy nhất để đánh giá HDD.

---

## 6. SATA Interface

HDD desktop/laptop phổ biến sử dụng SATA.

Một ổ SATA HDD thường cần:

- SATA power
- SATA data

Nếu HDD không được nhận:

1. Kiểm tra power.
2. Kiểm tra SATA cable.
3. Thử SATA port khác.
4. Kiểm tra BIOS.
5. Kiểm tra Disk Management.
6. Kiểm tra SMART.

---

## 7. HDD Performance

Các yếu tố:

- RPM
- Seek time
- Sequential throughput
- Random I/O
- Cache
- Platter density
- Interface
- Workload

HDD đặc biệt yếu ở random I/O vì phải di chuyển đầu đọc/ghi.

---

## 8. HDD Bad Sector

Bad sector là vùng lưu trữ không thể đọc/ghi dữ liệu một cách đáng tin cậy.

Các dấu hiệu:

- File đọc rất chậm.
- Copy file bị lỗi.
- Windows báo lỗi I/O.
- HDD phát tiếng động bất thường.
- SMART báo sector problems.
- System freezes khi truy cập ổ.

Các khái niệm liên quan:

### Reallocated Sector

Sector lỗi được thay thế bằng sector dự phòng.

### Current Pending Sector

Sector đang được drive đánh dấu nghi ngờ và chờ xử lý.

### Uncorrectable Sector

Sector không thể sửa/chỉnh đọc được bằng cơ chế hiện tại.

---

## 9. Dấu hiệu HDD sắp lỗi

Có thể gặp:

- Clicking
- Grinding
- Repeated spin-up
- Slow response
- File corruption
- I/O errors
- SMART warning
- Increasing bad sectors
- Unexpected disconnect

Nếu dữ liệu quan trọng:

> Backup/clone dữ liệu trước khi chạy các bài test nặng.

---

## 10. HDD và nhiệt độ

Nhiệt độ cao kéo dài có thể ảnh hưởng đến độ ổn định và tuổi thọ.

Cần:

- Airflow tốt.
- Không đặt HDD sát nguồn nhiệt.
- Không để HDD bị rung.
- Theo dõi temperature.

---

## 11. HDD dành cho mục đích nào?

Phù hợp:

- Backup
- Archive
- Media storage
- CCTV storage
- NAS
- File server
- Large-capacity secondary storage

Không tối ưu cho:

- OS cần tốc độ cao.
- VM workload nặng.
- Database random I/O.
- Application cần latency thấp.

---

## 12. Quy trình kiểm tra HDD

1. Kiểm tra ngoại hình.
2. Kiểm tra cable.
3. Kiểm tra BIOS.
4. Kiểm tra Disk Management.
5. Kiểm tra SMART.
6. Kiểm tra bad sectors.
7. Kiểm tra read/write.
8. Kiểm tra temperature.
9. Backup dữ liệu.
10. Ghi nhận kết quả.

---

# 🇬🇧 English

## 1. What is an HDD?

HDD stands for Hard Disk Drive.

It stores data magnetically on rotating platters.

Unlike SSDs, HDDs contain mechanical moving components.

---

## 2. HDD Components

Main components include:

- Platters
- Spindle motor
- Read/write heads
- Actuator arm
- Actuator
- PCB
- Firmware
- Cache

---

## 3. Form Factors

Common form factors:

### 3.5-inch

Used in:

- Desktop computers
- Servers
- NAS systems

### 2.5-inch

Used in:

- Laptops
- External enclosures
- Some compact computers

---

## 4. RPM

RPM means Revolutions Per Minute.

Common speeds:

- 5400 RPM
- 7200 RPM

Higher RPM can reduce rotational latency, but overall performance also depends on platter density, firmware, cache, seek behavior, and workload.

---

## 5. HDD Cache

HDDs may include onboard cache memory.

Cache can temporarily improve certain read/write operations.

Cache size alone should not be used to evaluate an HDD.

---

## 6. SATA Interface

Most modern consumer HDDs use SATA.

A SATA HDD normally requires:

- SATA power
- SATA data

---

## 7. HDD Performance

Important factors:

- RPM
- Seek time
- Sequential throughput
- Random I/O
- Cache
- Platter density
- Interface
- Workload

Random performance is usually limited because the mechanical head must physically move.

---

## 8. Bad Sectors

A bad sector is an area of storage that cannot reliably store or retrieve data.

Symptoms include:

- Very slow file access
- Copy errors
- I/O errors
- System freezes
- SMART warnings
- Abnormal noises

Important SMART concepts include:

- Reallocated sectors
- Pending sectors
- Uncorrectable sectors

---

## 9. Failure Symptoms

Possible warning signs:

- Clicking sounds
- Grinding sounds
- Repeated spin-up attempts
- Slow response
- File corruption
- I/O errors
- SMART warnings
- Increasing bad sectors
- Unexpected disconnects

Always prioritize data backup when a drive shows signs of failure.

---

## 10. Temperature

Good airflow is important.

Avoid:

- Excessive heat
- Poor ventilation
- Strong vibration
- Physical shocks

---

## 11. Recommended Use Cases

HDDs are suitable for:

- Backup
- Archive
- Media storage
- CCTV
- NAS
- File servers
- Large secondary storage

They are less suitable for:

- High-performance OS workloads
- Heavy virtual machines
- High-random-I/O databases
- Low-latency applications

---

## 12. HDD Testing Workflow

1. Inspect the drive.
2. Check cables.
3. Check BIOS detection.
4. Check Disk Management.
5. Review SMART.
6. Check for bad sectors.
7. Test read/write behavior.
8. Check temperature.
9. Back up important data.
10. Document the results.
