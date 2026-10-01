# RAM – Random Access Memory

## 🇻🇳 Tiếng Việt

### 1. Giới thiệu

**RAM (Random Access Memory)** là bộ nhớ truy cập ngẫu nhiên, được sử dụng để lưu trữ tạm thời dữ liệu và chương trình mà CPU đang cần xử lý.

RAM là một trong những thành phần quan trọng của máy tính và ảnh hưởng trực tiếp đến:

- Khả năng chạy nhiều ứng dụng cùng lúc
- Khả năng xử lý các tác vụ nặng
- Hiệu suất của hệ điều hành
- Khả năng chạy máy ảo
- Hiệu suất gaming
- Khả năng xử lý các ứng dụng chuyên dụng

RAM là bộ nhớ **volatile**, nghĩa là dữ liệu trong RAM sẽ mất khi hệ thống mất nguồn.

---

## 2. Mục tiêu của thư mục

Thư mục `RAM/` dùng để lưu trữ kiến thức và tài liệu thực hành về:

- RAM fundamentals
- RAM specifications
- RAM generations
- RAM form factors
- RAM compatibility
- RAM installation
- RAM testing
- RAM troubleshooting
- RAM upgrade
- Dual-channel / Multi-channel
- XMP / EXPO
- ECC / Non-ECC
- UDIMM / SO-DIMM
- Memory frequency
- Memory timings
- Memory capacity

---

## 3. Cấu trúc tài liệu

```text
RAM/
├── RAM-Compatibility.md
├── RAM-Overview.md
├── RAM-Testing.md
├── RAM-Troubleshooting.md
├── RAM-Upgrade.md
└── README.md
```

---

## 4. Nội dung từng file

| File | Nội dung |
|---|---|
| `RAM-Overview.md` | Tổng quan về RAM |
| `RAM-Compatibility.md` | Kiểm tra khả năng tương thích |
| `RAM-Testing.md` | Kiểm tra và test RAM |
| `RAM-Troubleshooting.md` | Chẩn đoán lỗi RAM |
| `RAM-Upgrade.md` | Nâng cấp RAM |
| `README.md` | Tổng quan thư mục |

---

## 5. Các loại RAM phổ biến

### Desktop

- DDR3 UDIMM
- DDR4 UDIMM
- DDR5 UDIMM

### Laptop

- DDR3 SO-DIMM
- DDR4 SO-DIMM
- DDR5 SO-DIMM

### Server / Workstation

- ECC UDIMM
- Registered DIMM
- Load-Reduced DIMM
- Các loại memory module chuyên dụng khác

---

## 6. Các thông số RAM quan trọng

Khi kiểm tra RAM cần quan tâm:

- Generation
- Capacity
- Module configuration
- Form factor
- Frequency / Data rate
- CAS Latency
- Timings
- Voltage
- Rank
- ECC
- Buffered / Unbuffered
- XMP / EXPO
- Number of modules
- Maximum motherboard capacity

---

## 7. RAM và hiệu năng

RAM không chỉ được đánh giá bằng dung lượng.

Ví dụ:

```text
16GB DDR4
```

chưa đủ thông tin.

Cần biết thêm:

```text
16GB
DDR4
3200 MT/s
CL16
1.35V
UDIMM
Non-ECC
```

---

## 8. Quy trình RAM cơ bản

```text
Identify RAM
     ↓
Check Specifications
     ↓
Check Compatibility
     ↓
Install RAM
     ↓
Verify BIOS/UEFI
     ↓
Boot Windows
     ↓
Test Memory
     ↓
Stress Test
     ↓
Document Result
```

---

## 9. An toàn khi thao tác RAM

- Tắt máy trước khi tháo RAM.
- Rút nguồn AC.
- Với laptop, ngắt pin nếu quy trình của nhà sản xuất yêu cầu.
- Không chạm vào các chân tiếp xúc.
- Cầm RAM ở cạnh PCB.
- Không bẻ cong module.
- Không ép RAM vào khe sai hướng.
- Đảm bảo hai bên latch đã khóa.
- Tránh tĩnh điện.

---

## 🇬🇧 English

# RAM – Random Access Memory

## 1. Introduction

**RAM (Random Access Memory)** is temporary working memory used by the CPU and operating system to store data and programs currently in use.

RAM affects:

- Multitasking
- Application performance
- Operating system responsiveness
- Virtual machines
- Gaming
- Professional workloads

RAM is **volatile memory**, meaning its contents are lost when power is removed.

---

## 2. Folder Objectives

The `RAM/` directory documents:

- RAM fundamentals
- RAM specifications
- RAM generations
- Form factors
- Compatibility
- Installation
- Testing
- Troubleshooting
- Upgrades
- Memory channels
- XMP / EXPO
- ECC / Non-ECC
- UDIMM / SO-DIMM
- Frequency
- Timings
- Capacity

---

## 3. Documentation Structure

```text
RAM/
├── RAM-Compatibility.md
├── RAM-Overview.md
├── RAM-Testing.md
├── RAM-Troubleshooting.md
├── RAM-Upgrade.md
└── README.md
```

---

## 4. Common RAM Types

### Desktop

- DDR3 UDIMM
- DDR4 UDIMM
- DDR5 UDIMM

### Laptop

- DDR3 SO-DIMM
- DDR4 SO-DIMM
- DDR5 SO-DIMM

### Server / Workstation

- ECC UDIMM
- Registered DIMM
- Load-Reduced DIMM
- Other specialized memory modules

---

## 5. Important RAM Specifications

Important specifications include:

- Memory generation
- Capacity
- Module configuration
- Form factor
- Frequency / Data rate
- CAS Latency
- Timings
- Voltage
- Rank
- ECC
- Buffered / Unbuffered
- XMP / EXPO
- Module count
- Maximum supported capacity

---

## 6. RAM Performance

RAM should not be evaluated by capacity alone.

For example:

```text
16GB DDR4
```

does not provide enough information.

A complete description may be:

```text
16GB
DDR4
3200 MT/s
CL16
1.35V
UDIMM
Non-ECC
```

---

## 7. Basic RAM Workflow

```text
Identify RAM
     ↓
Check Specifications
     ↓
Check Compatibility
     ↓
Install RAM
     ↓
Verify BIOS/UEFI
     ↓
Boot Windows
     ↓
Memory Test
     ↓
Stress Test
     ↓
Document Result
```

---

## 8. RAM Safety

- Shut down the computer before removing RAM.
- Disconnect AC power.
- Disconnect the laptop battery when required by the manufacturer's procedure.
- Do not touch the gold contacts.
- Hold the module by its edges.
- Do not bend the PCB.
- Never force a module into the slot.
- Make sure the retention clips are locked.
- Take appropriate ESD precautions.
