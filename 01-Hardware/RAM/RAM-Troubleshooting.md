# RAM Troubleshooting

## 🇻🇳 Tiếng Việt

# 1. RAM không được nhận đủ dung lượng

### Ví dụ

Lắp:

```text
2 × 16GB = 32GB
```

nhưng Windows chỉ nhận:

```text
16GB
```

### Kiểm tra

1. BIOS nhận bao nhiêu RAM?
2. Windows nhận bao nhiêu?
3. Có module nào không nhận?
4. Test từng DIMM.
5. Test từng slot.
6. Kiểm tra CPU socket.
7. Kiểm tra BIOS.
8. Kiểm tra giới hạn motherboard.

---

# 2. PC không POST sau khi lắp RAM

Symptoms:

- Black screen
- No POST
- Beep code
- DRAM debug LED
- Restart loop

### Procedure

```text
Power Off
   ↓
Remove recently installed RAM
   ↓
Test known-good module
   ↓
Clear CMOS if appropriate
   ↓
Load BIOS defaults
   ↓
Test each DIMM
```

---

# 3. PC bật nhưng màn hình đen

Possible causes:

- RAM not seated
- RAM incompatible
- RAM defective
- Memory training failure
- BIOS issue
- Motherboard slot
- CPU memory controller

---

# 4. RAM chưa cắm đúng

Một thanh RAM chưa khóa hoàn toàn có thể khiến hệ thống:

- Không POST
- Không nhận RAM
- Restart
- DRAM LED

Cần đảm bảo:

```text
Both retention clips locked
```

hoặc đúng cơ chế khóa của motherboard.

---

# 5. RAM chạy thấp hơn thông số

Ví dụ:

```text
RAM:
DDR4-3200
```

nhưng BIOS:

```text
2666 MT/s
```

Có thể do:

- XMP chưa bật
- CPU limitation
- Motherboard limitation
- JEDEC default
- DIMM configuration

---

# 6. XMP/EXPO không ổn định

Symptoms:

- BSOD
- Game crash
- Random restart
- Memory errors
- Boot failure

Procedure:

```text
Disable XMP/EXPO
      ↓
Run memory test
      ↓
If stable
      ↓
Investigate profile settings
```

---

# 7. Windows bị BSOD

Các lỗi liên quan memory có thể xuất hiện như:

- MEMORY_MANAGEMENT
- PAGE_FAULT_IN_NONPAGED_AREA
- IRQL_NOT_LESS_OR_EQUAL

Nhưng BSOD không đồng nghĩa chắc chắn RAM hỏng.

Cần kiểm tra:

- RAM
- Drivers
- Storage
- Windows
- CPU
- Motherboard

---

# 8. Ứng dụng tự crash

Ví dụ:

```text
Game crashes
Browser crashes
Software closes unexpectedly
```

Có thể liên quan RAM nhưng cũng có nhiều nguyên nhân khác.

Test memory trước khi kết luận.

---

# 9. PC restart ngẫu nhiên

Possible causes:

- RAM instability
- XMP/EXPO
- PSU
- CPU
- GPU
- Motherboard
- Overheating

---

# 10. DRAM Debug LED

Nếu motherboard có:

```text
DRAM LED
```

và đèn sáng, kiểm tra:

1. RAM seating
2. Correct slot
3. Single DIMM
4. CMOS
5. BIOS
6. Compatibility
7. CPU socket
8. Motherboard
9. RAM

---

# 11. Memory Training

DDR4/DDR5 systems có thể thực hiện memory training khi boot.

Sau khi:

- Thay RAM
- Thay CPU
- Clear CMOS
- Thay memory configuration

lần boot đầu có thể mất nhiều thời gian hơn bình thường.

Không nên lập tức tắt máy nếu motherboard đang thực hiện memory training theo quy trình của nhà sản xuất.

---

# 12. RAM gây lỗi chỉ khi tải cao

Nếu:

```text
Idle = OK
Memory Stress = Error
```

có thể liên quan:

- RAM
- Memory controller
- XMP/EXPO
- Voltage
- Temperature
- Motherboard

---

# 13. Một thanh RAM lỗi

Test:

```text
DIMM A
```

Nếu lỗi:

```text
Test DIMM B
```

Nếu chỉ DIMM A lỗi ở nhiều slot:

```text
DIMM A = Suspect
```

Nếu lỗi theo slot:

```text
Motherboard slot = Suspect
```

---

# 14. RAM lỗi theo cặp

Nếu:

```text
A = Pass
B = Pass
```

nhưng:

```text
A + B = Fail
```

Có thể liên quan:

- Dual-channel configuration
- XMP/EXPO
- Memory controller
- BIOS
- Compatibility
- Signal integrity

---

# 15. RAM không chạy Dual Channel

Kiểm tra:

- DIMM slot
- Motherboard manual
- Module configuration
- BIOS
- CPU platform

Ví dụ motherboard có:

```text
A1 A2 B1 B2
```

nhiều motherboard khuyến nghị:

```text
A2 + B2
```

nhưng phải theo manual của chính motherboard.

---

# 16. Hardware Reserved quá nhiều

Nếu Windows hiển thị:

```text
Installed: 16GB
Usable: 8GB
```

có thể kiểm tra:

- BIOS memory detection
- Integrated GPU allocation
- BIOS settings
- Memory remapping
- Hardware reservation
- Faulty DIMM

---

# 17. Troubleshooting Flow

```text
             RAM Problem
                  │
                  ▼
           Check Physical RAM
                  │
                  ▼
             Check BIOS
                  │
                  ▼
          Test Single DIMM
                  │
            ┌─────┴─────┐
            │           │
          Pass         Fail
            │           │
            ▼           ▼
       Test Other     Replace/Test
          DIMM          Module
            │
            ▼
        Test Slots
            │
            ▼
       Run Memory Test
            │
            ▼
      Default Settings
            │
            ▼
       XMP / EXPO Test
            │
            ▼
       Document Result
```

---

# 18. Troubleshooting Checklist

```text
[ ] Power off
[ ] Reseat RAM
[ ] Check correct slots
[ ] Check BIOS
[ ] Check capacity
[ ] Check data rate
[ ] Test one DIMM
[ ] Test other DIMM
[ ] Test different slots
[ ] Clear CMOS if appropriate
[ ] Disable XMP/EXPO
[ ] Run memory test
[ ] Check CPU socket
[ ] Check BIOS version
[ ] Check motherboard compatibility
[ ] Document result
```

---

## 🇬🇧 English

# RAM Troubleshooting

## 1. RAM Capacity Is Not Fully Detected

Example:

```text
Installed:
2 × 16GB = 32GB
```

But Windows reports:

```text
16GB
```

Check:

1. BIOS detected capacity.
2. Windows detected capacity.
3. Individual DIMMs.
4. Individual slots.
5. CPU socket.
6. BIOS.
7. Motherboard limits.

---

## 2. No POST After RAM Installation

Symptoms:

- Black screen
- No POST
- Beep codes
- DRAM debug LED
- Restart loop

Procedure:

```text
Power Off
   ↓
Remove Recently Installed RAM
   ↓
Test Known-Good Module
   ↓
Clear CMOS if appropriate
   ↓
Load BIOS Defaults
   ↓
Test Individual DIMMs
```

---

## 3. PC Powers On but No Display

Possible causes:

- RAM not seated correctly
- Incompatible RAM
- Defective RAM
- Memory training failure
- BIOS issue
- Motherboard slot
- CPU memory controller

---

## 4. RAM Not Fully Seated

Improperly installed RAM can cause:

- No POST
- Missing memory
- Restart loops
- DRAM LED

Ensure the module is fully inserted and the retention mechanism is properly locked.

---

## 5. RAM Runs Below Advertised Speed

Example:

```text
RAM:
DDR4-3200
```

But BIOS reports:

```text
2666 MT/s
```

Possible causes:

- XMP not enabled
- CPU limitation
- Motherboard limitation
- JEDEC default profile
- DIMM configuration

---

## 6. XMP/EXPO Instability

Symptoms:

- BSOD
- Game crashes
- Random restarts
- Memory errors
- Boot failure

Procedure:

```text
Disable XMP/EXPO
       ↓
Run Memory Test
       ↓
If Stable
       ↓
Investigate Profile Configuration
```

---

## 7. BSOD

Possible memory-related stop codes include:

- MEMORY_MANAGEMENT
- PAGE_FAULT_IN_NONPAGED_AREA
- IRQL_NOT_LESS_OR_EQUAL

However, a BSOD does not automatically prove that RAM is defective.

Also investigate:

- Drivers
- Storage
- Windows
- CPU
- Motherboard

---

## 8. Applications Crash

Examples:

```text
Game crashes
Browser crashes
Application closes unexpectedly
```

Memory instability can cause these symptoms, but other hardware/software causes are possible.

---

## 9. Random Restart

Possible causes:

- RAM instability
- XMP/EXPO
- PSU
- CPU
- GPU
- Motherboard
- Overheating

---

## 10. DRAM Debug LED

If the motherboard displays:

```text
DRAM LED
```

check:

1. RAM seating
2. Recommended slots
3. Single-DIMM configuration
4. CMOS
5. BIOS
6. Compatibility
7. CPU socket
8. Motherboard
9. RAM module

---

## 11. Memory Training

DDR4/DDR5 platforms may perform memory training during boot.

This may happen after:

- Installing new RAM
- Installing a new CPU
- Clearing CMOS
- Changing memory configuration

The first boot may take longer than usual.

Follow the motherboard manufacturer's procedure and allow the training process to complete when appropriate.

---

## 12. Errors Only Under High Memory Load

If:

```text
Idle = Stable
Memory Stress = Error
```

possible causes include:

- RAM
- Memory controller
- XMP/EXPO
- Voltage
- Temperature
- Motherboard

---

## 13. One DIMM Is Faulty

Test:

```text
DIMM A
```

If it fails:

```text
Test DIMM B
```

If DIMM A fails across multiple known-good slots while DIMM B passes:

```text
DIMM A = Suspect
```

---

## 14. Pair Works Individually but Fails Together

If:

```text
A = Pass
B = Pass
```

but:

```text
A + B = Fail
```

possible causes include:

- Dual-channel configuration
- XMP/EXPO
- Memory controller
- BIOS
- Compatibility
- Signal integrity

---

## 15. Dual-Channel Not Working

Check:

- DIMM slots
- Motherboard manual
- Module configuration
- BIOS
- CPU platform

Example:

```text
A1 A2 B1 B2
```

Many boards recommend:

```text
A2 + B2
```

but always follow the specific motherboard manual.

---

## 16. Excessive Hardware Reserved Memory

Example:

```text
Installed: 16GB
Usable: 8GB
```

Check:

- BIOS memory detection
- Integrated graphics allocation
- BIOS settings
- Memory remapping
- Hardware reservation
- Faulty DIMM

---

## 17. Troubleshooting Flow

```text
             RAM Problem
                  │
                  ▼
           Check Physical RAM
                  │
                  ▼
             Check BIOS
                  │
                  ▼
          Test Single DIMM
                  │
            ┌─────┴─────┐
            │           │
          Pass         Fail
            │           │
            ▼           ▼
       Test Other     Replace/Test
          DIMM          Module
            │
            ▼
        Test Slots
            │
            ▼
       Run Memory Test
            │
            ▼
      Default Settings
            │
            ▼
       XMP / EXPO Test
            │
            ▼
       Document Result
```

---

## 18. Troubleshooting Checklist

```text
[ ] Power off
[ ] Reseat RAM
[ ] Check recommended slots
[ ] Check BIOS
[ ] Check capacity
[ ] Check data rate
[ ] Test one DIMM
[ ] Test other DIMM
[ ] Test different slots
[ ] Clear CMOS if appropriate
[ ] Disable XMP/EXPO
[ ] Run memory test
[ ] Check CPU socket
[ ] Check BIOS version
[ ] Check motherboard compatibility
[ ] Document result
```
