# RAM Overview

## 🇻🇳 Tiếng Việt

# 1. RAM là gì?

**RAM (Random Access Memory)** là bộ nhớ tạm thời được hệ điều hành và ứng dụng sử dụng trong quá trình máy tính hoạt động.

Ví dụ:

```text
Storage
   ↓
Load Application
   ↓
RAM
   ↓
CPU
   ↓
Processing
```

SSD/HDD lưu dữ liệu lâu dài, trong khi RAM giữ dữ liệu đang được sử dụng.

---

# 2. RAM hoạt động như thế nào?

Khi mở ứng dụng:

```text
Application stored on SSD
          ↓
Operating System loads data
          ↓
RAM
          ↓
CPU accesses data
```

RAM có tốc độ truy cập cao hơn storage và được sử dụng làm vùng làm việc cho hệ thống.

---

# 3. RAM là Volatile Memory

RAM cần nguồn điện để giữ dữ liệu.

Khi:

```text
Power ON
```

RAM chứa dữ liệu.

Khi:

```text
Power OFF
```

Dữ liệu trong RAM bị mất.

---

# 4. RAM vs Storage

| Đặc điểm | RAM | SSD/HDD |
|---|---|---|
| Mục đích | Working memory | Long-term storage |
| Volatile | Có | Không |
| Tốc độ | Rất cao | Thấp hơn RAM |
| Dung lượng | Thường nhỏ hơn | Lớn hơn |
| Dữ liệu khi mất điện | Mất | Vẫn còn |

---

# 5. RAM Generations

Các thế hệ DDR phổ biến:

```text
DDR
DDR2
DDR3
DDR4
DDR5
```

Các thế hệ không tương thích trực tiếp với nhau.

Ví dụ:

```text
DDR4 ≠ DDR5
```

Không thể lắp DDR4 vào khe DDR5 chỉ vì hình thức module tương tự.

---

# 6. DDR

DDR là viết tắt của:

**Double Data Rate**

Bộ nhớ DDR truyền dữ liệu trên cả hai cạnh của tín hiệu clock.

Các thế hệ sau cải thiện:

- Data rate
- Capacity
- Efficiency
- Power management
- Memory architecture

---

# 7. Capacity

Dung lượng RAM thường được biểu thị bằng:

- GB
- TB đối với hệ thống lớn

Ví dụ:

```text
4GB
8GB
16GB
32GB
64GB
128GB
```

Dung lượng thực tế hỗ trợ phụ thuộc motherboard/CPU/platform.

---

# 8. Form Factor

## UDIMM

Thường dùng cho desktop.

## SO-DIMM

Thường dùng cho:

- Laptop
- Mini PC
- Small form factor systems

## RDIMM

Thường dùng trong server/workstation phù hợp.

## LRDIMM

Load-Reduced DIMM dành cho hệ thống server hỗ trợ loại module này.

---

# 9. Frequency vs Data Rate

RAM DDR thường được quảng cáo bằng tốc độ truyền dữ liệu.

Ví dụ:

```text
DDR4-3200
```

Con số 3200 thường biểu thị:

```text
3200 MT/s
```

Không nên gọi trực tiếp 3200 MT/s là 3200 MHz.

Clock thực tế của DDR4-3200 là khoảng:

```text
1600 MHz
```

vì DDR truyền dữ liệu hai lần mỗi clock cycle.

---

# 10. Memory Bandwidth

Công thức lý thuyết đơn giản:

```text
Bandwidth =
Data Rate × Bus Width ÷ 8
```

Ví dụ một module có:

```text
3200 MT/s
64-bit
```

Bandwidth lý thuyết:

```text
3200 × 64 ÷ 8
= 25,600 MB/s
```

≈

```text
25.6 GB/s
```

Đây là bandwidth lý thuyết của một memory channel/module trong điều kiện tương ứng, không phải tốc độ thực tế của toàn hệ thống.

---

# 11. CAS Latency

**CAS Latency (CL)** là số chu kỳ clock liên quan đến thời gian từ yêu cầu đọc đến khi dữ liệu bắt đầu xuất hiện trong một số điều kiện hoạt động.

Ví dụ:

```text
DDR4-3200 CL16
DDR4-3200 CL22
```

CL thấp hơn không phải lúc nào cũng đồng nghĩa toàn hệ thống nhanh hơn; cần xem cùng data rate và timing configuration.

---

# 12. RAM Timings

Ví dụ:

```text
16-18-18-38
```

Có thể bao gồm:

- CL
- tRCD
- tRP
- tRAS

Các timing khác có thể xuất hiện tùy module và công cụ đọc SPD.

---

# 13. RAM Voltage

Ví dụ:

```text
DDR4 JEDEC = commonly around 1.2V
```

Một số profile hiệu năng có thể sử dụng điện áp cao hơn.

Không nên tự tăng voltage nếu không hiểu rõ memory specification và platform.

---

# 14. Single Channel

Một memory module có thể hoạt động ở single-channel tùy platform/configuration.

```text
CPU
 ↓
Memory Controller
 ↓
RAM
```

---

# 15. Dual Channel

Hai module được cấu hình đúng trên motherboard có thể cho phép dual-channel operation.

```text
CPU
 ↓
Memory Controller
 ├── RAM
 └── RAM
```

Dual-channel có thể tăng memory bandwidth so với single-channel.

---

# 16. Multi-Channel

Một số nền tảng hỗ trợ:

- Dual-channel
- Quad-channel
- Hexa-channel
- Octa-channel

Khả năng cụ thể phụ thuộc CPU và motherboard/platform.

---

# 17. ECC

**ECC = Error-Correcting Code**

ECC memory có khả năng phát hiện và trong các cấu hình hỗ trợ, sửa một số lỗi bit.

Thường được sử dụng trong:

- Servers
- Workstations
- Mission-critical systems

Không phải CPU/motherboard nào cũng hỗ trợ ECC.

---

# 18. Non-ECC

RAM desktop phổ thông thường là:

```text
Non-ECC
```

Nó không có chức năng ECC như memory dành cho các hệ thống hỗ trợ ECC.

---

# 19. Buffered vs Unbuffered

### Unbuffered

Memory controller giao tiếp trực tiếp với DRAM module.

Phổ biến ở:

- Desktop
- Laptop

### Registered / Buffered

Có register/buffer giữa memory controller và DRAM.

Phổ biến ở server.

Không thể tùy ý thay thế UDIMM bằng RDIMM.

---

# 20. SPD

**SPD (Serial Presence Detect)** chứa thông tin cấu hình của RAM.

Có thể bao gồm:

- Capacity
- Memory type
- Supported data rates
- Timings
- Voltage
- Module information

BIOS/UEFI có thể sử dụng thông tin SPD để cấu hình bộ nhớ.

---

# 21. XMP

**XMP = Extreme Memory Profile**

Là profile cấu hình hiệu năng do Intel phát triển cho memory modules hỗ trợ XMP.

XMP có thể chứa:

- Data rate
- Timings
- Voltage

Khi bật XMP, hệ thống có thể chạy ngoài cấu hình JEDEC mặc định tùy profile và platform.

---

# 22. EXPO

**EXPO = Extended Profiles for Overclocking**

Là profile bộ nhớ được AMD phát triển cho nền tảng tương thích.

Tương tự XMP, EXPO cung cấp các thông số cấu hình bộ nhớ được lưu trong module.

---

# 23. JEDEC

JEDEC định nghĩa các chuẩn và thông số bộ nhớ.

Khi RAM hoạt động theo JEDEC profile, hệ thống thường sử dụng cấu hình chuẩn được module/platform hỗ trợ.

---

# 24. RAM Rank

RAM có thể được mô tả theo:

- Single Rank
- Dual Rank
- Multi-rank

Rank không đồng nghĩa với số lượng module.

---

# 25. Memory Channel vs RAM Slot

Ví dụ motherboard:

```text
A1
A2
B1
B2
```

Có thể tương ứng:

```text
Channel A
Channel B
```

Cách đánh số và vị trí ưu tiên phụ thuộc motherboard.

---

# 26. RAM Label

Một label có thể ghi:

```text
16GB DDR4-3200 CL16
1.35V
```

Có thể hiểu:

```text
Capacity = 16GB
Generation = DDR4
Data Rate = 3200 MT/s
CAS Latency = CL16
Voltage = 1.35V
```

---

# 27. RAM Specifications Checklist

```text
[ ] Capacity
[ ] DDR Generation
[ ] Form Factor
[ ] Data Rate
[ ] CAS Latency
[ ] Timings
[ ] Voltage
[ ] Rank
[ ] ECC
[ ] Registered / Unbuffered
[ ] XMP / EXPO
```

---

## 🇬🇧 English

# RAM Overview

## 1. What Is RAM?

**Random Access Memory (RAM)** is temporary working memory used by the operating system, applications, and CPU.

Typical workflow:

```text
Storage
   ↓
Application Load
   ↓
RAM
   ↓
CPU
   ↓
Processing
```

---

## 2. How RAM Works

When an application is opened:

```text
Application on Storage
        ↓
Operating System
        ↓
RAM
        ↓
CPU
```

RAM provides high-speed working memory for active processes.

---

## 3. Volatile Memory

RAM is volatile memory.

When power is removed:

```text
RAM Data = Lost
```

---

## 4. RAM vs Storage

| Feature | RAM | SSD/HDD |
|---|---|---|
| Purpose | Working memory | Long-term storage |
| Volatile | Yes | No |
| Speed | Very high | Lower |
| Capacity | Usually smaller | Usually larger |
| Data after power loss | Lost | Retained |

---

## 5. DDR Generations

Common generations:

```text
DDR
DDR2
DDR3
DDR4
DDR5
```

Different generations are not directly interchangeable.

Example:

```text
DDR4 ≠ DDR5
```

---

## 6. Capacity

Common capacities include:

```text
4GB
8GB
16GB
32GB
64GB
128GB
```

Actual supported capacity depends on the platform.

---

## 7. Form Factors

### UDIMM

Commonly used in desktop systems.

### SO-DIMM

Commonly used in:

- Laptops
- Mini PCs
- Small-form-factor systems

### RDIMM

Commonly used in supported servers/workstations.

### LRDIMM

Load-Reduced DIMM for supported server platforms.

---

## 8. Frequency vs Data Rate

DDR memory is commonly specified using data rate.

Example:

```text
DDR4-3200
```

Typically means:

```text
3200 MT/s
```

The actual memory clock is approximately:

```text
1600 MHz
```

because DDR transfers data twice per clock cycle.

---

## 9. Memory Bandwidth

Simplified theoretical formula:

```text
Bandwidth =
Data Rate × Bus Width ÷ 8
```

Example:

```text
3200 MT/s × 64-bit ÷ 8
= 25,600 MB/s
```

≈

```text
25.6 GB/s
```

Actual system performance depends on the complete memory architecture and workload.

---

## 10. CAS Latency

**CAS Latency (CL)** represents the number of memory clock cycles associated with a read access under a specified configuration.

Example:

```text
DDR4-3200 CL16
DDR4-3200 CL22
```

Lower CL does not automatically mean better overall performance; data rate and the complete timing configuration also matter.

---

## 11. Memory Timings

Example:

```text
16-18-18-38
```

May represent:

- CL
- tRCD
- tRP
- tRAS

---

## 12. RAM Voltage

A common DDR4 baseline is around:

```text
1.2V
```

Performance profiles may use higher voltage.

Always follow the module and motherboard specifications.

---

## 13. Single Channel

A memory configuration may operate in single-channel mode.

```text
CPU
 ↓
Memory Controller
 ↓
RAM
```

---

## 14. Dual Channel

Two correctly installed modules can enable dual-channel operation on supported platforms.

```text
CPU
 ↓
Memory Controller
 ├── RAM
 └── RAM
```

This can increase memory bandwidth compared with single-channel operation.

---

## 15. Multi-Channel

Some platforms support:

- Dual-channel
- Quad-channel
- Hexa-channel
- Octa-channel

Support depends on the CPU and motherboard/platform.

---

## 16. ECC

**ECC = Error-Correcting Code**

ECC memory provides error detection and, in supported implementations, correction of certain memory errors.

Common in:

- Servers
- Workstations
- Reliability-focused systems

---

## 17. Non-ECC

Common consumer desktop memory is often:

```text
Non-ECC
```

It does not provide ECC functionality.

---

## 18. Buffered vs Unbuffered

### Unbuffered

The memory controller communicates directly with the memory devices.

Common in consumer desktops and laptops.

### Registered / Buffered

A register or buffer is placed between the memory controller and DRAM.

Common in servers.

RDIMM and UDIMM should not be treated as interchangeable.

---

## 19. SPD

**SPD (Serial Presence Detect)** stores memory module configuration information.

It may contain:

- Capacity
- Memory type
- Supported data rates
- Timings
- Voltage
- Module information

---

## 20. XMP

**XMP (Extreme Memory Profile)** is a memory profile technology developed by Intel.

A profile may contain:

- Data rate
- Timings
- Voltage

Enabling XMP can configure the memory beyond the default JEDEC configuration depending on the module and platform.

---

## 21. EXPO

**EXPO (Extended Profiles for Overclocking)** is AMD's memory profile technology for compatible platforms.

It provides predefined memory settings stored on supported modules.

---

## 22. JEDEC

JEDEC defines memory standards and specifications.

JEDEC profiles represent standardized memory operating configurations supported by the module/platform.

---

## 23. RAM Rank

Memory modules can be described as:

- Single-rank
- Dual-rank
- Multi-rank

Rank is not the same thing as the number of installed modules.

---

## 24. Memory Channels and Slots

A motherboard may have:

```text
A1
A2
B1
B2
```

These may correspond to:

```text
Channel A
Channel B
```

The recommended slots depend on the motherboard manual.

---

## 25. RAM Label Example

Example:

```text
16GB DDR4-3200 CL16
1.35V
```

Meaning:

```text
Capacity = 16GB
Generation = DDR4
Data Rate = 3200 MT/s
CAS Latency = CL16
Voltage = 1.35V
```

---

## 26. RAM Specification Checklist

```text
[ ] Capacity
[ ] DDR Generation
[ ] Form Factor
[ ] Data Rate
[ ] CAS Latency
[ ] Timings
[ ] Voltage
[ ] Rank
[ ] ECC
[ ] Registered / Unbuffered
[ ] XMP / EXPO
```
