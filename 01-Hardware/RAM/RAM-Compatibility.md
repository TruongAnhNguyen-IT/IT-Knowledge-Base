# RAM Compatibility

## 🇻🇳 Tiếng Việt

# 1. RAM Compatibility là gì?

RAM compatibility là quá trình xác định một module RAM có thể hoạt động ổn định với:

- CPU
- Motherboard
- BIOS/UEFI
- Memory controller
- Các RAM module khác

hay không.

---

# 2. Các yếu tố cần kiểm tra

Trước khi mua RAM cần kiểm tra:

```text
DDR Generation
Form Factor
Capacity
Maximum Capacity
Module Count
Data Rate
Voltage
ECC
Buffered / Unbuffered
Rank
Motherboard Support
CPU Support
BIOS Support
```

---

# 3. DDR Generation

Đây là yếu tố đầu tiên phải kiểm tra.

Ví dụ:

```text
Motherboard = DDR4
```

Phải sử dụng:

```text
DDR4 RAM
```

Không sử dụng:

```text
DDR5
```

---

# 4. Form Factor

Desktop thường dùng:

```text
UDIMM
```

Laptop thường dùng:

```text
SO-DIMM
```

Không được mặc định rằng UDIMM và SO-DIMM có thể thay thế cho nhau.

---

# 5. Maximum Capacity

Ví dụ motherboard có specification:

```text
Maximum Memory = 128GB
```

Có thể hỗ trợ:

```text
4 × 32GB
```

Nhưng vẫn phải kiểm tra:

- CPU memory limit
- BIOS
- Module density
- Memory configuration

---

# 6. Number of Slots

Ví dụ:

```text
4 DIMM slots
```

Không có nghĩa bắt buộc phải lắp đủ 4 thanh.

Có thể:

```text
1 × 16GB
2 × 8GB
2 × 16GB
4 × 16GB
```

tùy platform.

---

# 7. Motherboard QVL

**QVL = Qualified Vendor List**

Một số motherboard manufacturer cung cấp danh sách RAM đã được kiểm tra.

QVL có thể giúp xác định:

- Module model
- Capacity
- Speed
- Configuration

Không có trong QVL không nhất thiết có nghĩa RAM không tương thích.

---

# 8. CPU Memory Support

CPU có memory controller và có giới hạn hỗ trợ.

Cần kiểm tra:

- Maximum memory capacity
- Supported memory generation
- Supported data rates
- Number of channels
- ECC support

---

# 9. BIOS/UEFI

BIOS/UEFI có thể ảnh hưởng:

- Memory compatibility
- High-density modules
- Memory training
- XMP/EXPO
- Stability

Nếu RAM mới không nhận, có thể cần cập nhật BIOS theo hướng dẫn motherboard manufacturer.

---

# 10. RAM Speed Compatibility

Ví dụ:

```text
Motherboard supports DDR4
RAM = DDR4-3600
```

Không có nghĩa hệ thống chắc chắn chạy 3600 MT/s.

Có thể bị giới hạn bởi:

- CPU
- Motherboard
- BIOS
- Number of modules
- Memory rank
- DIMM configuration

---

# 11. Mixing RAM

Có thể gặp trường hợp:

```text
8GB DDR4-3200
+
16GB DDR4-3200
```

Hệ thống có thể hoạt động nhưng phụ thuộc platform.

Khi trộn RAM, có thể xảy ra:

- Chạy ở tốc độ thấp hơn
- Timing thay đổi
- Voltage profile thay đổi
- Không ổn định
- Không boot

---

# 12. Different Speeds

Ví dụ:

```text
DDR4-3200
+
DDR4-2666
```

Hệ thống thường phải hoạt động ở cấu hình chung mà memory controller/platform hỗ trợ, thường bị giới hạn bởi module chậm hơn hoặc cấu hình an toàn hơn.

---

# 13. Different Capacities

Ví dụ:

```text
8GB + 16GB
```

Một số platform có thể sử dụng vùng bộ nhớ theo cấu hình bất đối xứng.

Hiệu quả channel có thể khác so với cấu hình hai module giống nhau.

---

# 14. Different Brands

Ví dụ:

```text
Kingston
+
Crucial
```

Không có nghĩa chắc chắn không tương thích.

Điều quan trọng hơn:

- DDR generation
- Module type
- Voltage
- Timings
- Capacity
- Platform support

Tuy nhiên sử dụng matched kit thường dễ đảm bảo tính ổn định hơn.

---

# 15. Matched Kit

Ví dụ:

```text
2 × 16GB DDR5
```

được bán thành một kit.

Các module trong kit được nhà sản xuất lựa chọn để hoạt động cùng nhau theo thông số công bố.

---

# 16. ECC Compatibility

ECC RAM chỉ hoạt động đúng chức năng khi:

```text
CPU
+
Motherboard
+
BIOS
+
Memory
```

cùng hỗ trợ.

Không phải hệ thống desktop nào cũng hỗ trợ ECC.

---

# 17. UDIMM vs RDIMM

Không được tùy ý thay:

```text
UDIMM
```

bằng:

```text
RDIMM
```

Server platform thường có yêu cầu memory type cụ thể.

---

# 18. XMP / EXPO Compatibility

Nếu RAM có:

```text
XMP
```

cần kiểm tra platform có hỗ trợ XMP hay không.

Nếu RAM có:

```text
EXPO
```

cần kiểm tra platform có hỗ trợ EXPO hay không.

Nếu profile không hoạt động, RAM có thể vẫn chạy ở JEDEC/default profile phù hợp.

---

# 19. Compatibility Checklist

```text
[ ] DDR generation
[ ] Form factor
[ ] Maximum capacity
[ ] Motherboard slots
[ ] CPU memory support
[ ] Motherboard QVL
[ ] BIOS version
[ ] Data rate
[ ] Voltage
[ ] ECC
[ ] UDIMM/RDIMM
[ ] Rank
[ ] Module count
[ ] XMP/EXPO
```

---

# 20. Compatibility Example

### System

```text
Motherboard:
DDR4
4 DIMM slots
Maximum 128GB

CPU:
Supports DDR4

Existing RAM:
2 × 8GB DDR4-3200
```

### Upgrade

```text
Add:
2 × 8GB DDR4-3200
```

Expected total:

```text
32GB
```

Cần kiểm tra motherboard manual và QVL nếu muốn xác nhận cấu hình cụ thể.

---

## 🇬🇧 English

# RAM Compatibility

## 1. What Is RAM Compatibility?

RAM compatibility determines whether a memory module can operate correctly with:

- CPU
- Motherboard
- BIOS/UEFI
- Memory controller
- Other installed modules

---

## 2. Compatibility Factors

Check:

```text
DDR Generation
Form Factor
Capacity
Maximum Capacity
Module Count
Data Rate
Voltage
ECC
Buffered / Unbuffered
Rank
Motherboard Support
CPU Support
BIOS Support
```

---

## 3. DDR Generation

If a motherboard supports:

```text
DDR4
```

use:

```text
DDR4
```

not DDR5.

Different generations are not interchangeable.

---

## 4. Form Factor

Desktop systems commonly use:

```text
UDIMM
```

Laptops commonly use:

```text
SO-DIMM
```

---

## 5. Maximum Capacity

Example:

```text
Maximum Memory = 128GB
```

The motherboard may support:

```text
4 × 32GB
```

but CPU, BIOS, module density, and configuration must also be considered.

---

## 6. Number of Slots

A motherboard with four DIMM slots does not necessarily require four modules.

Possible configurations may include:

```text
1 × 16GB
2 × 8GB
2 × 16GB
4 × 16GB
```

Actual support depends on the platform.

---

## 7. QVL

**QVL = Qualified Vendor List**

Motherboard manufacturers may publish tested memory configurations.

A QVL may include:

- Module model
- Capacity
- Speed
- Configuration

Not appearing on the QVL does not automatically mean the module is incompatible.

---

## 8. CPU Memory Support

Check:

- Maximum capacity
- Supported memory generation
- Supported data rates
- Memory channels
- ECC support

---

## 9. BIOS/UEFI

BIOS/UEFI can affect:

- Memory compatibility
- High-density modules
- Memory training
- XMP/EXPO
- Stability

A BIOS update may sometimes improve compatibility.

---

## 10. RAM Speed Compatibility

Example:

```text
Motherboard = DDR4
RAM = DDR4-3600
```

This does not guarantee 3600 MT/s operation.

Actual operating speed may depend on:

- CPU
- Motherboard
- BIOS
- Number of modules
- Rank
- DIMM configuration

---

## 11. Mixing RAM

Example:

```text
8GB DDR4-3200
+
16GB DDR4-3200
```

This may work, but compatibility and stability depend on the platform.

Potential results include:

- Lower operating speed
- Different timings
- Different voltage
- Instability
- Failure to boot

---

## 12. Different Memory Speeds

Example:

```text
DDR4-3200
+
DDR4-2666
```

The memory controller may operate the modules at a common supported configuration, often constrained by the slower module or a safer configuration.

---

## 13. Different Capacities

Example:

```text
8GB + 16GB
```

Some platforms support asymmetric memory configurations.

Channel behavior may differ from a matched configuration.

---

## 14. Different Brands

Example:

```text
Kingston
+
Crucial
```

Different brands are not automatically incompatible.

Important factors include:

- DDR generation
- Module type
- Voltage
- Timings
- Capacity
- Platform support

Matched kits are generally easier to configure consistently.

---

## 15. Matched Kit

Example:

```text
2 × 16GB DDR5
```

sold as a kit.

The modules are selected and validated by the manufacturer for operation together according to the advertised specifications.

---

## 16. ECC Compatibility

ECC functionality requires appropriate support across:

```text
CPU
+
Motherboard
+
BIOS
+
Memory
```

Not every desktop platform supports ECC.

---

## 17. UDIMM vs RDIMM

Do not assume that:

```text
UDIMM
```

and:

```text
RDIMM
```

are interchangeable.

Server platforms generally require specific memory types.

---

## 18. XMP / EXPO

For XMP memory:

```text
Check XMP support
```

For EXPO memory:

```text
Check EXPO support
```

If a performance profile is unavailable, compatible memory may still operate using a standard/default profile.

---

## 19. Compatibility Checklist

```text
[ ] DDR generation
[ ] Form factor
[ ] Maximum capacity
[ ] Motherboard slots
[ ] CPU memory support
[ ] QVL
[ ] BIOS version
[ ] Data rate
[ ] Voltage
[ ] ECC
[ ] UDIMM/RDIMM
[ ] Rank
[ ] Module count
[ ] XMP/EXPO
```

---

## 20. Compatibility Example

Example:

```text
Motherboard:
DDR4
4 DIMM slots
128GB maximum

CPU:
DDR4 supported

Existing:
2 × 8GB DDR4-3200
```

Upgrade:

```text
Add:
2 × 8GB DDR4-3200
```

Expected capacity:

```text
32GB
```

Always verify the motherboard manual and supported memory configurations.
