# RAM Upgrade

## 🇻🇳 Tiếng Việt

# 1. RAM Upgrade là gì?

RAM upgrade là quá trình tăng dung lượng hoặc thay đổi cấu hình bộ nhớ của hệ thống.

Ví dụ:

```text
8GB
 ↓
16GB
```

hoặc:

```text
16GB
 ↓
32GB
```

---

# 2. Khi nào nên nâng cấp RAM?

Có thể cân nhắc nâng cấp khi:

- RAM thường xuyên gần 100%.
- Windows sử dụng nhiều memory.
- Hệ thống swap/pagefile thường xuyên.
- Multitasking bị chậm.
- Chạy VM thiếu RAM.
- Editing bị thiếu memory.
- Gaming bị giới hạn bởi RAM.
- Ứng dụng yêu cầu dung lượng cao hơn.

---

# 3. Kiểm tra RAM hiện tại

Trước khi nâng cấp:

```text
Task Manager
→ Performance
→ Memory
```

Ghi lại:

- Capacity
- Speed
- Slots used
- Form factor

Sau đó kiểm tra thêm:

- CPU
- Motherboard
- BIOS
- RAM model

---

# 4. Xác định Maximum RAM

Kiểm tra:

```text
CPU maximum memory
+
Motherboard maximum memory
+
BIOS support
```

Giới hạn thực tế có thể phụ thuộc cả CPU và motherboard.

---

# 5. Kiểm tra số khe RAM

Ví dụ:

```text
4 DIMM slots
```

Nếu đang sử dụng:

```text
2 × 8GB
```

có thể:

```text
Add 2 × 8GB
```

hoặc:

```text
Replace with 2 × 16GB
```

Tùy khả năng hỗ trợ.

---

# 6. Upgrade bằng cách thêm RAM

Ví dụ:

```text
Existing:
2 × 8GB

Upgrade:
+ 2 × 8GB

Total:
32GB
```

Ưu điểm:

- Giữ lại RAM cũ.
- Chi phí thấp hơn.

Nhược điểm:

- Có thể khó chạy profile tốc độ cao.
- Khả năng tương thích phụ thuộc module.
- 4 DIMM có thể gây thêm áp lực cho memory controller trên một số platform.

---

# 7. Upgrade bằng cách thay RAM

Ví dụ:

```text
Existing:
2 × 8GB

Replace:
2 × 16GB

Total:
32GB
```

Ưu điểm:

- Matched kit.
- Dễ kiểm soát cấu hình.
- Có thể thuận lợi hơn cho stability.

Nhược điểm:

- Chi phí cao hơn.
- RAM cũ không được sử dụng.

---

# 8. Single vs Dual Channel

Ví dụ:

```text
1 × 16GB
```

so với:

```text
2 × 8GB
```

Hai cấu hình đều có:

```text
16GB
```

nhưng cấu hình 2 × 8GB có thể tận dụng dual-channel trên nền tảng hỗ trợ nếu lắp đúng slot.

---

# 9. 2 × 16GB vs 4 × 8GB

Cả hai đều:

```text
32GB
```

Nhưng:

```text
2 × 16GB
```

thường dễ cấu hình hơn trên nhiều desktop platform so với:

```text
4 × 8GB
```

Không phải mọi nền tảng đều giống nhau.

Cần kiểm tra motherboard/CPU memory support.

---

# 10. Laptop RAM Upgrade

Laptop có thể:

```text
Soldered RAM
```

hoặc:

```text
SO-DIMM
```

hoặc kết hợp cả hai.

Ví dụ:

```text
8GB soldered
+
1 × SO-DIMM
```

Nếu RAM soldered, không thể tháo module đó như DIMM thông thường.

---

# 11. RAM Soldered

Một số laptop có RAM được hàn trực tiếp trên motherboard.

Ưu điểm:

- Tiết kiệm không gian.
- Thiết kế mỏng.

Nhược điểm:

- Không thể thay module soldered.
- Khả năng nâng cấp bị giới hạn.

---

# 12. Chọn RAM Upgrade

Cần xác định:

```text
DDR Generation
Form Factor
Capacity
Data Rate
Voltage
ECC
Rank
Module Type
```

---

# 13. Ví dụ nâng cấp Desktop

### Existing

```text
CPU:
Intel platform

Motherboard:
DDR4
4 DIMM slots

RAM:
2 × 8GB DDR4-3200
```

### Option A

```text
Add:
2 × 8GB DDR4-3200
```

Total:

```text
32GB
```

### Option B

```text
Replace:
2 × 16GB DDR4-3200
```

Total:

```text
32GB
```

Cần kiểm tra manual/QVL và platform support trước khi quyết định.

---

# 14. Ví dụ nâng cấp Laptop

### Existing

```text
8GB SO-DIMM
```

Upgrade:

```text
16GB SO-DIMM
```

hoặc:

```text
8GB + 16GB
```

Tùy laptop hỗ trợ.

---

# 15. Quy trình nâng cấp

```text
Identify Current RAM
        ↓
Check CPU Support
        ↓
Check Motherboard/Laptop Manual
        ↓
Check Maximum Capacity
        ↓
Check Form Factor
        ↓
Check DDR Generation
        ↓
Select RAM
        ↓
Power Off
        ↓
Install RAM
        ↓
BIOS Check
        ↓
Windows Check
        ↓
Memory Test
        ↓
Document
```

---

# 16. Sau khi nâng cấp

Kiểm tra:

### BIOS

```text
Total Memory
```

### Windows

```text
Task Manager
→ Performance
→ Memory
```

### Testing

Chạy:

- Windows Memory Diagnostic
- MemTest86
- Stress test

---

# 17. Lỗi sau nâng cấp

Nếu sau khi nâng cấp:

```text
No POST
```

thực hiện:

```text
Remove new RAM
      ↓
Test old RAM
      ↓
Test new RAM individually
      ↓
Check slots
      ↓
Clear CMOS if appropriate
      ↓
Check compatibility
```

---

# 18. RAM Upgrade Best Practices

- Ưu tiên matched kit.
- Kiểm tra motherboard manual.
- Kiểm tra CPU memory support.
- Kiểm tra QVL khi cần.
- Không trộn RAM một cách tùy tiện.
- Không ép XMP/EXPO nếu hệ thống không ổn định.
- Test RAM sau upgrade.
- Ghi lại cấu hình trước và sau upgrade.

---

# 19. Upgrade Documentation

```text
Date:

System:
CPU:
Motherboard:

Before:
RAM:
Capacity:
Speed:
Slots:

Upgrade:
Old RAM:
New RAM:

After:
Total Capacity:
Operating Speed:
Channel Mode:

Test:
Memory Diagnostic:
MemTest86:
Stress Test:

Result:
```

---

## 🇬🇧 English

# RAM Upgrade

## 1. What Is a RAM Upgrade?

A RAM upgrade increases memory capacity or changes the system memory configuration.

Example:

```text
8GB
 ↓
16GB
```

or:

```text
16GB
 ↓
32GB
```

---

## 2. When Should RAM Be Upgraded?

Consider upgrading when:

- Memory usage frequently approaches 100%.
- Applications consume most available RAM.
- Paging occurs frequently.
- Multitasking becomes slow.
- Virtual machines need more memory.
- Editing workloads need additional memory.
- Games require more memory.

---

## 3. Check Current RAM

Open:

```text
Task Manager
→ Performance
→ Memory
```

Record:

- Capacity
- Speed
- Slots used
- Form factor

Also identify:

- CPU
- Motherboard
- BIOS
- RAM model

---

## 4. Determine Maximum RAM

Check:

```text
CPU Maximum Memory
+
Motherboard Maximum Memory
+
BIOS Support
```

Actual limits depend on the complete platform.

---

## 5. Check RAM Slots

Example:

```text
4 DIMM slots
```

Existing:

```text
2 × 8GB
```

Possible upgrades may include:

```text
Add 2 × 8GB
```

or:

```text
Replace with 2 × 16GB
```

depending on platform support.

---

## 6. Adding More RAM

Example:

```text
Existing:
2 × 8GB

Add:
2 × 8GB

Total:
32GB
```

Advantages:

- Reuses existing modules.
- Potentially lower cost.

Disadvantages:

- Mixed kits may have compatibility issues.
- Higher module count can affect memory stability.
- High-speed profiles may not work as expected.

---

## 7. Replacing RAM

Example:

```text
Existing:
2 × 8GB

Replace:
2 × 16GB

Total:
32GB
```

Advantages:

- Matched kit.
- Easier configuration.
- Potentially easier stability at advertised settings.

Disadvantages:

- Higher cost.
- Existing RAM may no longer be used.

---

## 8. Single vs Dual Channel

Example:

```text
1 × 16GB
```

and:

```text
2 × 8GB
```

both provide:

```text
16GB
```

However, two correctly installed modules may enable dual-channel operation on supported platforms.

---

## 9. 2 × 16GB vs 4 × 8GB

Both configurations provide:

```text
32GB
```

But:

```text
2 × 16GB
```

may be easier to configure on many desktop platforms than:

```text
4 × 8GB
```

Platform-specific support must still be checked.

---

## 10. Laptop RAM Upgrade

Laptop memory may be:

```text
Soldered
```

or:

```text
SO-DIMM
```

or a combination of both.

Example:

```text
8GB soldered
+
1 × SO-DIMM
```

---

## 11. Soldered RAM

Some laptops have memory soldered directly onto the motherboard.

Advantages:

- Saves space.
- Enables thinner designs.

Disadvantages:

- Cannot be removed like a standard DIMM.
- Upgrade options may be limited.

---

## 12. Selecting RAM

Check:

```text
DDR Generation
Form Factor
Capacity
Data Rate
Voltage
ECC
Rank
Module Type
```

---

## 13. Desktop Upgrade Example

Existing:

```text
CPU:
Intel platform

Motherboard:
DDR4
4 DIMM slots

RAM:
2 × 8GB DDR4-3200
```

Option A:

```text
Add:
2 × 8GB DDR4-3200
```

Total:

```text
32GB
```

Option B:

```text
Replace:
2 × 16GB DDR4-3200
```

Total:

```text
32GB
```

Verify the motherboard manual, QVL, and platform support.

---

## 14. Laptop Upgrade Example

Existing:

```text
8GB SO-DIMM
```

Possible upgrade:

```text
16GB SO-DIMM
```

or:

```text
8GB + 16GB
```

depending on the laptop design.

---

## 15. Upgrade Workflow

```text
Identify Current RAM
        ↓
Check CPU Support
        ↓
Check Motherboard/Laptop Manual
        ↓
Check Maximum Capacity
        ↓
Check Form Factor
        ↓
Check DDR Generation
        ↓
Select RAM
        ↓
Power Off
        ↓
Install RAM
        ↓
BIOS Check
        ↓
Windows Check
        ↓
Memory Test
        ↓
Document
```

---

## 16. After Upgrade

Check:

### BIOS

```text
Total Memory
```

### Windows

```text
Task Manager
→ Performance
→ Memory
```

### Testing

Run:

- Windows Memory Diagnostic
- MemTest86
- Memory stress test

---

## 17. No POST After Upgrade

If the system does not POST:

```text
Remove New RAM
      ↓
Test Old RAM
      ↓
Test New RAM Individually
      ↓
Check Slots
      ↓
Clear CMOS if appropriate
      ↓
Check Compatibility
```

---

## 18. RAM Upgrade Best Practices

- Prefer matched kits when practical.
- Check the motherboard manual.
- Check CPU memory support.
- Check QVL when useful.
- Avoid unnecessary mixing.
- Do not force unstable XMP/EXPO settings.
- Test memory after upgrading.
- Document the before/after configuration.

---

## 19. Upgrade Documentation

```text
Date:

System:
CPU:
Motherboard:

Before:
RAM:
Capacity:
Speed:
Slots:

Upgrade:
Old RAM:
New RAM:

After:
Total Capacity:
Operating Speed:
Channel Mode:

Testing:
Memory Diagnostic:
MemTest86:
Stress Test:

Result:
```
