# CPU Compatibility / Khả năng tương thích CPU

## 1. Overview / Tổng quan

**Tiếng Việt**

CPU Compatibility là quá trình kiểm tra CPU có thể hoạt động với motherboard và các thành phần liên quan hay không.

**English**

CPU compatibility is the process of determining whether a processor can operate correctly with a motherboard and related hardware.

---

# 2. Compatibility Factors / Các yếu tố cần kiểm tra

Khi kiểm tra CPU compatibility, cần kiểm tra:

1. CPU Socket
2. Motherboard Socket
3. Chipset
4. BIOS/UEFI
5. CPU Support List
6. RAM Compatibility
7. Power Requirements
8. VRM capability
9. CPU Cooler
10. PCIe compatibility

---

# 3. CPU Socket / Socket CPU

CPU và motherboard phải có socket tương thích.

Ví dụ:

```text
CPU:
Intel Core i5-10400

Socket:
LGA1200
```

Motherboard phải hỗ trợ LGA1200.

Không thể lắp CPU LGA1200 trực tiếp vào motherboard LGA1700.

---

# 4. Chipset Compatibility / Tương thích chipset

Chipset motherboard quyết định nhiều tính năng mà CPU có thể sử dụng.

Ví dụ với Intel Core i5-10400:

Một số chipset liên quan:

- H410
- B460
- H470
- Z490

Một số chipset 500-series cũng có thể hỗ trợ CPU LGA1200 tùy motherboard và BIOS.

**Important / Quan trọng:**

Không nên chỉ dựa vào socket.

Cần kiểm tra CPU Support List của chính motherboard.

---

# 5. BIOS Compatibility / Tương thích BIOS

Một motherboard có thể sử dụng đúng socket nhưng vẫn không nhận CPU nếu BIOS không hỗ trợ CPU đó.

**English**

A motherboard may have the correct socket but still fail to recognize a processor if the BIOS version does not support it.

---

# 6. CPU Support List / Danh sách CPU hỗ trợ

Motherboard manufacturers thường cung cấp CPU Support List.

Khi kiểm tra:

```text
Motherboard Model
        ↓
CPU Support List
        ↓
CPU Model
        ↓
Required BIOS Version
```

Ví dụ:

```text
Motherboard:
Example B560 Motherboard

CPU:
Intel Core i5-11400

Check:
- CPU support
- Required BIOS version
```

---

# 7. RAM Compatibility / Tương thích RAM

Cần kiểm tra:

- DDR4 / DDR5
- Maximum RAM capacity
- Number of memory channels
- Supported memory speed
- ECC support nếu cần

CPU và motherboard phải hỗ trợ loại RAM tương ứng.

---

# 8. Power Requirements / Yêu cầu nguồn

Cần kiểm tra:

- PSU capacity
- CPU power connector
- Motherboard VRM
- CPU power consumption
- Cooling capability

Đặc biệt với CPU hiệu năng cao, cần kiểm tra motherboard VRM và hệ thống tản nhiệt.

---

# 9. CPU Cooler Compatibility / Tương thích tản nhiệt

Cần kiểm tra:

- CPU socket support
- Cooler mounting bracket
- Cooler thermal capacity
- Case clearance
- RAM clearance

Ví dụ:

```text
CPU Socket:
LGA1700

Cooler:
Must support LGA1700 mounting.
```

---

# 10. Practical Compatibility Checklist / Checklist thực tế

| Item | Check |
|---|---|
| CPU Model | ☐ |
| CPU Socket | ☐ |
| Motherboard Model | ☐ |
| Motherboard Socket | ☐ |
| Chipset | ☐ |
| BIOS Version | ☐ |
| CPU Support List | ☐ |
| RAM Type | ☐ |
| RAM Capacity | ☐ |
| PSU | ☐ |
| CPU Power Connector | ☐ |
| CPU Cooler | ☐ |
| Case Clearance | ☐ |

---

# 11. Example: Intel Core i5-10400

## CPU Information

| Specification | Value |
|---|---|
| CPU | Intel Core i5-10400 |
| Generation | 10th Gen |
| Codename | Comet Lake |
| Socket | LGA1200 |
| Cores | 6 |
| Threads | 12 |
| Memory | DDR4 |
| iGPU | Intel UHD Graphics 630 |

## Compatibility Process

### Step 1

Identify motherboard model.

### Step 2

Check motherboard socket.

### Step 3

Check chipset.

### Step 4

Check BIOS version.

### Step 5

Check CPU Support List.

### Step 6

Check RAM compatibility.

### Step 7

Check CPU cooler.

### Step 8

Check PSU and CPU power connector.

---

# 12. Common Compatibility Mistakes / Lỗi thường gặp

### Mistake 1

Only checking socket.

**Sai:** Socket giống nhau không đảm bảo mọi CPU đều được hỗ trợ.

### Mistake 2

Ignoring BIOS version.

**Sai:** BIOS cũ có thể không hỗ trợ CPU mới.

### Mistake 3

Ignoring RAM generation.

Ví dụ:

```text
DDR4 motherboard
≠
DDR5 RAM
```

### Mistake 4

Ignoring cooler compatibility.

CPU có thể lắp được nhưng cooler chưa chắc có mounting kit phù hợp.

---

# 13. Compatibility Rule / Nguyên tắc

> **Always verify the motherboard manufacturer's CPU Support List before installing or upgrading a CPU.**

> **Luôn kiểm tra CPU Support List của nhà sản xuất motherboard trước khi lắp hoặc nâng cấp CPU.**
