# RAM Testing

## 🇻🇳 Tiếng Việt

# 1. Mục tiêu

RAM testing nhằm xác định:

- RAM có được nhận hay không.
- RAM có đúng dung lượng không.
- RAM có chạy đúng cấu hình không.
- RAM có lỗi phần cứng không.
- Hệ thống có ổn định không.

---

# 2. Các công cụ kiểm tra

Có thể sử dụng:

- BIOS/UEFI
- Windows Task Manager
- Windows Memory Diagnostic
- MemTest86
- HWiNFO
- CPU-Z
- Thaiphoon Burner hoặc công cụ SPD tương ứng nếu phù hợp
- Stress testing software

---

# 3. Kiểm tra vật lý

Trước tiên:

```text
Power Off
   ↓
Disconnect AC
   ↓
Remove RAM
   ↓
Inspect
```

Kiểm tra:

- PCB
- Gold contacts
- Notch
- IC
- Label
- Burn marks
- Corrosion
- Physical damage

---

# 4. Kiểm tra RAM trong BIOS/UEFI

Khởi động BIOS/UEFI.

Kiểm tra:

```text
Memory Capacity
Memory Speed
Memory Mode
Detected DIMMs
```

Ví dụ:

```text
Installed Memory:
32GB

Memory Speed:
3200 MT/s
```

---

# 5. Kiểm tra trong Windows

Mở:

```text
Task Manager
→ Performance
→ Memory
```

Có thể xem:

- Total memory
- Speed
- Slots used
- Form factor
- Hardware reserved

---

# 6. Windows Memory Diagnostic

Có thể mở:

```text
Win + R
```

Nhập:

```text
mdsched.exe
```

Chọn:

```text
Restart now and check for problems
```

Windows sẽ restart và thực hiện memory test.

---

# 7. MemTest86

MemTest86 là công cụ bootable dùng để kiểm tra RAM độc lập với Windows.

Quy trình:

```text
Create Bootable USB
       ↓
Boot from USB
       ↓
Run Memory Test
       ↓
Complete Passes
       ↓
Review Errors
```

---

# 8. Test nhiều Pass

Một lần test chưa chắc đủ.

Có thể chạy nhiều pass để tăng khả năng phát hiện lỗi không ổn định.

---

# 9. Interpreting Errors

Nếu memory test báo:

```text
Errors > 0
```

cần điều tra.

Nguyên nhân có thể:

- RAM defective
- Memory controller
- Motherboard slot
- BIOS settings
- Overclocking
- XMP/EXPO instability
- Voltage
- Temperature

Không nên ngay lập tức kết luận chỉ thanh RAM hỏng.

---

# 10. Test từng thanh

Nếu có:

```text
2 × 16GB
```

có thể test:

```text
DIMM A alone
DIMM B alone
```

Mục tiêu:

```text
Identify defective module
```

---

# 11. Test từng Slot

Nếu nghi ngờ motherboard:

```text
Same RAM
↓
Slot A
↓
Slot B
↓
Compare
```

Nếu lỗi chỉ xuất hiện ở một slot, motherboard có thể là suspect.

---

# 12. Test Default Settings

Nếu hệ thống đang bật:

- XMP
- EXPO
- Manual overclock
- Manual timing
- Manual voltage

Hãy thử:

```text
Load BIOS Defaults
```

sau đó test lại.

---

# 13. Test XMP/EXPO

Quy trình:

```text
Default
 ↓
Memory Test
 ↓
Enable XMP/EXPO
 ↓
Memory Test
 ↓
Compare
```

Nếu chỉ lỗi khi XMP/EXPO bật:

```text
Profile / memory / CPU IMC / motherboard compatibility
```

cần được điều tra.

---

# 14. Stress Test

Có thể sử dụng các memory stress tools để kiểm tra:

- Stability
- Temperature
- Errors
- Long-duration behavior

---

# 15. Testing Workflow

```text
Visual Inspection
       ↓
BIOS Detection
       ↓
Windows Detection
       ↓
Default Settings
       ↓
Memory Diagnostic
       ↓
MemTest
       ↓
Individual DIMM Test
       ↓
Slot Test
       ↓
XMP/EXPO Test
       ↓
Document Result
```

---

# 16. Test Record

```text
Date:
System:
Motherboard:
CPU:
RAM Brand:
RAM Model:
Capacity:
Data Rate:
Timings:
Voltage:

BIOS:
Windows:
Memory Test:
MemTest86:

Errors:
DIMM 1:
DIMM 2:
Slot A:
Slot B:

XMP/EXPO:
Result:
Conclusion:
```

---

## 🇬🇧 English

# RAM Testing

## 1. Testing Objectives

RAM testing determines:

- Whether memory is detected.
- Whether the correct capacity is detected.
- Whether the memory is operating correctly.
- Whether memory errors exist.
- Whether the system is stable.

---

## 2. Testing Tools

Useful tools include:

- BIOS/UEFI
- Windows Task Manager
- Windows Memory Diagnostic
- MemTest86
- HWiNFO
- CPU-Z
- SPD information tools
- Memory stress-testing software

---

## 3. Physical Inspection

Procedure:

```text
Power Off
   ↓
Disconnect AC
   ↓
Remove RAM
   ↓
Inspect
```

Check:

- PCB
- Gold contacts
- Notch
- ICs
- Label
- Burn marks
- Corrosion
- Physical damage

---

## 4. BIOS/UEFI Test

Check:

```text
Memory Capacity
Memory Speed
Memory Mode
Detected DIMMs
```

Example:

```text
Installed Memory:
32GB

Memory Speed:
3200 MT/s
```

---

## 5. Windows Task Manager

Open:

```text
Task Manager
→ Performance
→ Memory
```

Possible information:

- Total memory
- Speed
- Slots used
- Form factor
- Hardware reserved

---

## 6. Windows Memory Diagnostic

Run:

```text
Win + R
```

Enter:

```text
mdsched.exe
```

Select:

```text
Restart now and check for problems
```

Windows will restart and perform a memory diagnostic.

---

## 7. MemTest86

MemTest86 is a bootable memory-testing environment.

Basic workflow:

```text
Create Bootable USB
       ↓
Boot from USB
       ↓
Run Memory Test
       ↓
Complete Test Passes
       ↓
Review Errors
```

---

## 8. Multiple Passes

A single pass may not detect every intermittent problem.

Multiple passes can increase the chance of detecting marginal memory stability.

---

## 9. Interpreting Errors

If:

```text
Errors > 0
```

investigate:

- Defective RAM
- Memory controller
- Motherboard slot
- BIOS configuration
- Overclocking
- XMP/EXPO instability
- Voltage
- Temperature

An error does not automatically prove that the DIMM itself is defective.

---

## 10. Test Individual DIMMs

For:

```text
2 × 16GB
```

test:

```text
DIMM A alone
DIMM B alone
```

This helps isolate a potentially defective module.

---

## 11. Test Individual Slots

Use the same module in different slots:

```text
Same RAM
 ↓
Slot A
 ↓
Slot B
 ↓
Compare
```

If errors occur only in one slot, the motherboard may be the suspect.

---

## 12. Test Default Settings

If the system uses:

- XMP
- EXPO
- Manual overclocking
- Manual timings
- Manual voltage

test again using:

```text
BIOS Defaults
```

---

## 13. XMP/EXPO Testing

Procedure:

```text
Default
 ↓
Memory Test
 ↓
Enable XMP/EXPO
 ↓
Memory Test
 ↓
Compare
```

If errors occur only with XMP/EXPO enabled, investigate:

- Memory profile
- DIMMs
- CPU memory controller
- Motherboard
- Compatibility

---

## 14. Stress Testing

Memory stress tests can evaluate:

- Stability
- Temperature
- Errors
- Long-duration behavior

---

## 15. Testing Workflow

```text
Physical Inspection
       ↓
BIOS Detection
       ↓
Windows Detection
       ↓
Default Settings
       ↓
Memory Diagnostic
       ↓
MemTest
       ↓
Individual DIMM Test
       ↓
Slot Test
       ↓
XMP/EXPO Test
       ↓
Document Result
```

---

## 16. Test Record

```text
Date:
System:
Motherboard:
CPU:
RAM Brand:
RAM Model:
Capacity:
Data Rate:
Timings:
Voltage:

BIOS:
Windows:
Memory Test:
MemTest86:

Errors:
DIMM 1:
DIMM 2:
Slot A:
Slot B:

XMP/EXPO:
Result:
Conclusion:
```
