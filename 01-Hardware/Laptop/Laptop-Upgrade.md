# Laptop Upgrade / Nâng cấp Laptop

## 1. Overview / Tổng quan

Laptop upgrade là quá trình thay thế hoặc bổ sung phần cứng để cải thiện dung lượng, khả năng sử dụng hoặc hiệu năng của thiết bị.

**English:**

Laptop upgrading is the process of replacing or adding hardware to improve capacity, usability, or performance.

---

# 2. Common Upgrade Options / Các linh kiện thường nâng cấp

Các nâng cấp phổ biến:

- RAM
- SSD
- Wi-Fi card trên một số model
- Battery replacement
- CPU/GPU trên một số thiết kế đặc biệt

Tuy nhiên, khả năng nâng cấp phụ thuộc hoàn toàn vào model laptop.

---

# 3. Upgradeability / Khả năng nâng cấp

Laptop components có thể thuộc các loại:

### Replaceable

Có thể tháo và thay thế.

### Upgradeable

Có thể nâng cấp sang linh kiện có thông số cao hơn.

### Soldered

Hàn trực tiếp trên motherboard và không thể nâng cấp theo cách thông thường.

Ví dụ:

- Soldered RAM
- Soldered Wi-Fi
- Soldered CPU/SoC

---

# 4. RAM Upgrade / Nâng cấp RAM

Trước khi nâng RAM cần kiểm tra:

- RAM type
- Capacity
- Speed
- SO-DIMM
- Number of slots
- Maximum supported capacity
- Motherboard limitations
- Soldered memory

Ví dụ:

```text
Current:
8 GB DDR4

Upgrade:
16 GB DDR4
```

Không nên chỉ nhìn dung lượng; cần kiểm tra khả năng hỗ trợ của laptop.

---

# 5. SSD Upgrade / Nâng cấp SSD

Các chuẩn phổ biến:

- 2.5-inch SATA
- M.2 SATA
- M.2 NVMe

Cần xác định chính xác laptop hỗ trợ loại nào.

---

# 6. M.2 SSD Compatibility / Tương thích M.2

Cần kiểm tra:

- M.2 form factor
- Key type
- SATA or NVMe
- PCIe generation
- Supported capacity
- Physical clearance

Ví dụ:

```text
M.2 2280
NVMe
PCIe
```

---

# 7. SSD Migration / Chuyển hệ điều hành sang SSD

Quy trình:

```text
Backup Data
     ↓
Check New SSD
     ↓
Install SSD
     ↓
Clone Disk
     ↓
Verify Clone
     ↓
Boot from New SSD
     ↓
Check Windows
     ↓
Verify Data
```

Luôn backup dữ liệu quan trọng trước khi clone hoặc thay ổ.

---

# 8. Battery Replacement / Thay pin

Trước khi thay:

- Check battery model
- Check voltage
- Check connector
- Check physical dimensions
- Check manufacturer compatibility

Không sử dụng pin không rõ nguồn gốc hoặc không tương thích.

---

# 9. Wi-Fi Card Upgrade / Nâng cấp Wi-Fi

Nếu laptop sử dụng Wi-Fi card dạng module có thể tháo:

Kiểm tra:

- Form factor
- Interface
- Supported Wi-Fi standard
- Bluetooth
- Antenna connectors
- OS driver support
- BIOS restrictions

---

# 10. CPU/GPU Upgrade / Nâng cấp CPU/GPU

Đa số laptop hiện đại có CPU và GPU hàn trên motherboard.

Do đó:

```text
Desktop:
CPU/GPU upgrade → Common

Laptop:
CPU/GPU upgrade → Usually not practical
```

Một số laptop/workstation đặc biệt có thiết kế khác, nhưng cần kiểm tra model cụ thể.

---

# 11. Upgrade Planning / Lập kế hoạch nâng cấp

Quy trình:

```text
Identify Problem
       ↓
Identify Current Hardware
       ↓
Check Laptop Specifications
       ↓
Check Service Manual
       ↓
Check Compatibility
       ↓
Select Upgrade
       ↓
Backup Data
       ↓
Install Hardware
       ↓
Install Drivers
       ↓
Test
       ↓
Document
```

---

# 12. Upgrade Compatibility Checklist

| Item | Check |
|---|---|
| Laptop Model | ☐ |
| Service Manual | ☐ |
| RAM Type | ☐ |
| RAM Capacity | ☐ |
| RAM Speed | ☐ |
| RAM Slots | ☐ |
| SSD Form Factor | ☐ |
| SSD Interface | ☐ |
| SSD Capacity | ☐ |
| Battery Model | ☐ |
| Wi-Fi Card | ☐ |
| BIOS | ☐ |
| Driver | ☐ |
| Physical Clearance | ☐ |

---

# 13. Common Upgrade Mistakes / Lỗi thường gặp

### Mistake 1

Mua RAM chỉ dựa vào dung lượng.

### Mistake 2

Mua SSD M.2 nhưng không kiểm tra laptop hỗ trợ SATA hay NVMe.

### Mistake 3

Không kiểm tra số lượng RAM slots.

### Mistake 4

Không kiểm tra maximum supported capacity.

### Mistake 5

Không backup dữ liệu.

### Mistake 6

Không kiểm tra service manual.

### Mistake 7

Không test thiết bị sau nâng cấp.

---

# 14. Post-Upgrade Testing / Kiểm tra sau nâng cấp

Sau khi nâng cấp:

### RAM

Check:

- Capacity
- Speed
- Stability

### SSD

Check:

- Capacity
- Health
- Performance
- Boot

### Battery

Check:

- Charging
- Battery detection
- Runtime

### Wi-Fi

Check:

- Adapter detection
- Driver
- Connection
- Stability

---

# 15. Upgrade Documentation / Ghi nhận nâng cấp

```text
Date:

Laptop:
Model:
Serial Number:

Original Hardware:

RAM:
Storage:
Battery:
Wi-Fi:

Upgrade:

Old Component:
New Component:

Reason:

Compatibility Check:

Installation:

Test Result:

Final Result:
```

**English:**

```text
Date:

Laptop:
Model:
Serial Number:

Original Hardware:

RAM:
Storage:
Battery:
Wi-Fi:

Upgrade:

Old Component:
New Component:

Reason:

Compatibility Check:

Installation:

Test Result:

Final Result:
```
