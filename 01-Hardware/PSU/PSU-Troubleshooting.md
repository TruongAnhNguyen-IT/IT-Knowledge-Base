# PSU Troubleshooting

## 🇻🇳 Tiếng Việt

# 1. Mục tiêu

PSU troubleshooting nhằm xác định:

```text
Power Source
     ↓
AC Cable
     ↓
PSU
     ↓
Motherboard
     ↓
CPU / RAM / GPU / Storage
```

Lỗi có thể nằm ở bất kỳ bước nào.

---

# 2. PC hoàn toàn không bật

### Symptoms

Nhấn nút Power nhưng:

- Không có đèn
- Không có quạt
- Không có tiếng
- Không có hình

### Kiểm tra

#### Step 1

Kiểm tra ổ điện.

#### Step 2

Kiểm tra AC cable.

#### Step 3

Kiểm tra PSU switch.

#### Step 4

Kiểm tra 24-pin ATX.

#### Step 5

Kiểm tra CPU EPS.

#### Step 6

Kiểm tra front-panel Power Switch.

#### Step 7

Thử PSU khác đã biết hoạt động tốt.

---

# 3. PC bật rồi tắt ngay

### Possible causes

- PSU protection
- Short circuit
- CPU power problem
- Motherboard problem
- GPU problem
- Overcurrent
- Overheating
- Loose connector

### Troubleshooting

```text
Remove unnecessary devices
        ↓
Minimum hardware
        ↓
Check 24-pin
        ↓
Check EPS
        ↓
Test RAM
        ↓
Test GPU
        ↓
Known-Good PSU
```

---

# 4. PC tự restart

Possible causes:

- PSU instability
- Overheating
- RAM
- CPU
- GPU
- Driver
- Windows
- Motherboard

### Procedure

1. Check Event Viewer.
2. Check temperature.
3. Run memory test.
4. Test CPU/GPU load.
5. Check PSU voltages.
6. Test with known-good PSU.

---

# 5. PC tắt khi chơi game

Đây là tình huống cần chú ý.

Game tạo tải lớn cho:

- CPU
- GPU
- PSU

Nếu PC:

```text
Idle = OK
Gaming = Shutdown
```

Cần kiểm tra:

- PSU capacity
- PSU quality
- GPU power connector
- GPU temperature
- CPU temperature
- GPU power behavior
- PSU output stability

Không kết luận ngay rằng PSU hỏng.

---

# 6. GPU Black Screen

Có thể liên quan đến:

- GPU
- PCIe cable
- PSU
- Driver
- GPU temperature
- Motherboard
- Display cable
- Monitor

### Kiểm tra

```text
GPU
 ↓
PCIe Power Cable
 ↓
PSU
```

Kiểm tra connector đã cắm hoàn toàn chưa.

---

# 7. PSU có tiếng ồn

### Possible causes

- Fan bearing
- Fan speed
- Coil whine
- Mechanical vibration
- Dust

### Coil Whine

Có thể xuất hiện dưới:

- GPU load
- CPU load
- High FPS
- Different power states

Coil whine không đồng nghĩa PSU chắc chắn bị hỏng.

---

# 8. PSU Fan không quay

Không phải lúc nào fan không quay cũng có nghĩa PSU hỏng.

Một số PSU có:

```text
Zero RPM / Semi-passive mode
```

Trong chế độ này fan có thể đứng yên khi tải hoặc nhiệt độ thấp.

Cần kiểm tra:

- PSU model
- Fan mode
- Temperature
- Load
- Manufacturer specification

---

# 9. Có mùi khét

Nếu có:

```text
Burning smell
Smoke
Melting
Sparking
```

### Action

```text
Power OFF
   ↓
Disconnect AC
   ↓
Stop using PSU
   ↓
Inspect / Replace
```

Không tiếp tục chạy thử nhiều lần.

---

# 10. Connector bị cháy

Ví dụ:

```text
GPU Connector
    ↓
Burn mark
    ↓
Melted plastic
```

Có thể do:

- Poor connection
- Loose connector
- Excessive current
- Cable problem
- Connector damage
- Installation issue

Không chỉ thay connector mà bỏ qua nguyên nhân.

---

# 11. PSU Voltage thấp

Nếu đo thấy điện áp ngoài phạm vi cho phép:

```text
Measure
   ↓
Verify Measurement
   ↓
Check Instrument
   ↓
Check Cable
   ↓
Retest
   ↓
Known-Good PSU
```

Không nên kết luận dựa trên một lần đo duy nhất.

---

# 12. SSD/HDD mất nguồn

Possible causes:

- SATA power cable
- Connector
- PSU rail
- Storage device
- SATA data cable
- Motherboard

Test:

```text
Storage
 ↓
Different SATA power connector
 ↓
Different cable if available
 ↓
Known-Good PSU
```

---

# 13. Nhiều thiết bị không hoạt động

Ví dụ:

```text
SSD
HDD
Fan Controller
RGB
```

cùng mất nguồn.

Kiểm tra:

- SATA power cable
- Modular PSU port
- PSU output
- Cable splitter

---

# 14. PC chỉ bật khi tháo GPU

Possible causes:

- GPU short/problem
- PSU insufficient or faulty
- PCIe cable problem
- Motherboard PCIe issue

Procedure:

```text
Remove GPU
   ↓
Use iGPU if available
   ↓
Boot
   ↓
Test
```

Sau đó kiểm tra GPU và PSU.

---

# 15. PSU Troubleshooting Flow

```text
                 PC Problem
                     │
                     ▼
              Check AC Power
                     │
                     ▼
                Check PSU
                     │
              ┌──────┴──────┐
              │             │
            Power          No Power
              │             │
              ▼             ▼
       Check connectors   PSU test
              │             │
              ▼             ▼
        Test system     Known-good PSU
              │             │
              └──────┬──────┘
                     ▼
              Compare Results
                     │
                     ▼
              Document Finding
```

---

# 16. Troubleshooting Checklist

```text
[ ] Wall outlet
[ ] AC cable
[ ] PSU switch
[ ] PSU physical condition
[ ] 24-pin ATX
[ ] CPU EPS
[ ] GPU PCIe power
[ ] SATA power
[ ] Modular cable compatibility
[ ] PSU wattage
[ ] +12V capacity
[ ] PSU voltage
[ ] Temperature
[ ] RAM
[ ] GPU
[ ] Motherboard
[ ] Known-good PSU
```

---

# 17. Documentation Example

```text
Problem:
PC randomly shuts down during gaming.

Initial Observation:
System is stable during idle operation.

Checks:
- AC cable: OK
- 24-pin: OK
- EPS: OK
- GPU cable: OK
- Temperature: Normal
- PSU capacity: Adequate
- PSU test: Pass
- Known-good PSU: Stable

Result:
Original PSU remains suspect.

Action:
Replace PSU and perform extended load test.
```

---

## 🇬🇧 English

# PSU Troubleshooting

## 1. Objective

PSU troubleshooting evaluates the complete power path:

```text
Power Source
     ↓
AC Cable
     ↓
PSU
     ↓
Motherboard
     ↓
CPU / RAM / GPU / Storage
```

---

# 2. PC Has No Power

### Symptoms

- No LEDs
- No fans
- No sound
- No display

### Checks

1. Check wall outlet.
2. Check AC cable.
3. Check PSU switch.
4. Check 24-pin ATX.
5. Check CPU EPS.
6. Check front-panel power switch.
7. Test with a known-good PSU.

---

# 3. PC Turns On and Immediately Shuts Down

Possible causes:

- PSU protection
- Short circuit
- CPU power problem
- Motherboard problem
- GPU problem
- Overcurrent
- Overheating
- Loose connector

Basic procedure:

```text
Remove unnecessary devices
        ↓
Minimum hardware
        ↓
Check 24-pin
        ↓
Check EPS
        ↓
Test RAM
        ↓
Test GPU
        ↓
Known-Good PSU
```

---

# 4. Random Restart

Possible causes include:

- PSU instability
- Overheating
- RAM problems
- CPU problems
- GPU problems
- Drivers
- Windows
- Motherboard

Procedure:

1. Check Event Viewer.
2. Check temperatures.
3. Run memory testing.
4. Test CPU/GPU load.
5. Check PSU output.
6. Test with a known-good PSU.

---

# 5. Shutdown During Gaming

Gaming can heavily load:

- CPU
- GPU
- PSU

If:

```text
Idle = Stable
Gaming = Shutdown
```

Check:

- PSU capacity
- PSU quality
- GPU power connector
- GPU temperature
- CPU temperature
- GPU power behavior
- PSU output stability

Do not automatically conclude that the PSU is defective.

---

# 6. GPU Black Screen

Possible causes:

- GPU
- PCIe power cable
- PSU
- Driver
- GPU temperature
- Motherboard
- Display cable
- Monitor

Check:

```text
GPU
 ↓
PCIe Power Cable
 ↓
PSU
```

Make sure the connector is fully inserted.

---

# 7. PSU Noise

Possible causes:

- Fan bearing
- Fan speed
- Coil whine
- Mechanical vibration
- Dust

Coil whine does not automatically mean that the PSU is defective.

---

# 8. PSU Fan Not Spinning

Some PSUs use:

```text
Zero RPM
Semi-passive cooling
```

The fan may remain off at low load or temperature.

Check:

- PSU model
- Fan mode
- Temperature
- Load
- Manufacturer documentation

---

# 9. Burning Smell

If there is:

- Burning smell
- Smoke
- Melting
- Sparking

Action:

```text
Power OFF
   ↓
Disconnect AC
   ↓
Stop using PSU
   ↓
Inspect / Replace
```

Do not repeatedly power on a potentially damaged PSU.

---

# 10. Burned Connector

A burned connector may result from:

- Poor contact
- Loose connector
- Excessive current
- Cable problems
- Connector damage
- Installation issues

The underlying cause should be investigated before continuing to use the system.

---

# 11. Low PSU Voltage

If measured voltage appears outside the expected range:

```text
Measure
   ↓
Verify measurement
   ↓
Check instrument
   ↓
Check cable
   ↓
Retest
   ↓
Known-Good PSU
```

Avoid making a final diagnosis from one measurement.

---

# 12. Storage Devices Losing Power

Possible causes:

- SATA power cable
- Connector
- PSU output
- Storage device
- SATA data cable
- Motherboard

Test:

```text
Storage
 ↓
Different SATA power connector
 ↓
Different cable
 ↓
Known-Good PSU
```

---

# 13. Multiple Devices Lose Power

If several devices lose power simultaneously:

```text
SSD
HDD
Fan Controller
RGB
```

Check:

- SATA power cable
- Modular PSU port
- PSU output
- Splitters

---

# 14. PC Works Only Without GPU

Possible causes:

- GPU fault
- PSU issue
- PCIe cable issue
- Motherboard PCIe problem

Procedure:

```text
Remove GPU
   ↓
Use integrated graphics if available
   ↓
Boot
   ↓
Test
```

Then test the GPU and PSU separately.

---

# 15. Troubleshooting Flow

```text
                PC Problem
                    │
                    ▼
             Check AC Power
                    │
                    ▼
               Check PSU
                    │
             ┌──────┴──────┐
             │             │
           Power          No Power
             │             │
             ▼             ▼
      Check connectors   PSU Test
             │             │
             ▼             ▼
       Test System    Known-Good PSU
             │             │
             └──────┬──────┘
                    ▼
             Compare Results
                    │
                    ▼
             Document Finding
```

---

# 16. Troubleshooting Checklist

```text
[ ] Wall outlet
[ ] AC cable
[ ] PSU switch
[ ] PSU physical condition
[ ] 24-pin ATX
[ ] CPU EPS
[ ] GPU PCIe power
[ ] SATA power
[ ] Modular cable compatibility
[ ] PSU wattage
[ ] +12V capacity
[ ] PSU voltage
[ ] Temperature
[ ] RAM
[ ] GPU
[ ] Motherboard
[ ] Known-good PSU
```

---

# 17. Documentation Example

```text
Problem:
PC randomly shuts down during gaming.

Initial Observation:
System is stable during idle operation.

Checks:
- AC cable: OK
- 24-pin: OK
- EPS: OK
- GPU cable: OK
- Temperature: Normal
- PSU capacity: Adequate
- PSU test: Pass
- Known-good PSU: Stable

Result:
Original PSU remains a suspect.

Action:
Replace PSU and perform an extended load test.
```
