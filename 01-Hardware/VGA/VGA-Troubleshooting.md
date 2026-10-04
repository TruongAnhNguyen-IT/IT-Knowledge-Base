# VGA Troubleshooting

> **Tiếng Việt:** Quy trình chẩn đoán và xử lý sự cố VGA.  
> **English:** Graphics card troubleshooting and diagnostic procedures.

---

# 1. Troubleshooting Methodology

## 🇻🇳

Không nên thay linh kiện ngẫu nhiên.

Quy trình:

```text
Identify Problem
↓
Collect Information
↓
Reproduce Problem
↓
Check Basic Causes
↓
Isolate Hardware / Software
↓
Test One Variable
↓
Apply Fix
↓
Verify
↓
Document
```

## 🇬🇧

Do not randomly replace components.

Use:

```text
Identify Problem
↓
Collect Information
↓
Reproduce Problem
↓
Check Basic Causes
↓
Isolate Hardware / Software
↓
Test One Variable
↓
Apply Fix
↓
Verify
↓
Document
```

---

# 2. VGA Not Detected

## Symptoms

### 🇻🇳

- Windows không nhận GPU.
- Device Manager không hiển thị VGA.
- GPU-Z không nhận.
- Không có display output.

### 🇬🇧

- Windows does not detect the GPU.
- GPU is missing from Device Manager.
- GPU-Z does not detect it.
- No display output.

## Troubleshooting

```text
Power Off
↓
Reseat GPU
↓
Check PCIe Slot
↓
Check Power
↓
Check Monitor Cable
↓
Check BIOS
↓
Test Another PCIe Slot
↓
Test Another GPU
↓
Test GPU in Another PC
```

---

# 3. No Display / Black Screen

Possible causes:

```text
Monitor
Cable
Wrong Input
GPU
GPU Power
RAM
PSU
Motherboard
Driver
```

Quy trình:

```text
Check Monitor
↓
Check Input Source
↓
Check Cable
↓
Check GPU
↓
Check GPU Power
↓
Check RAM
↓
Check BIOS
↓
Test iGPU
↓
Test Another GPU
```

---

# 4. Black Screen After Windows Boot

## 🇻🇳

Nếu BIOS hiển thị bình thường nhưng Windows vào màn hình đen:

Có thể liên quan:

- Driver.
- Resolution.
- Refresh rate.
- Windows.
- GPU acceleration.

Thử:

```text
Safe Mode
↓
Remove Driver
↓
Restart
↓
Install Correct Driver
↓
Restart
↓
Test
```

## 🇬🇧

If BIOS displays correctly but Windows becomes black:

Possible causes include:

- Driver.
- Resolution.
- Refresh rate.
- Windows.
- GPU acceleration.

Try:

```text
Safe Mode
↓
Remove Driver
↓
Restart
↓
Install Correct Driver
↓
Restart
↓
Test
```

---

# 5. Code 43

## 🇻🇳

Code 43 không đồng nghĩa chắc chắn VGA hỏng.

Cần kiểm tra:

```text
Driver
GPU
VRAM
Power
PCIe
BIOS
Windows
```

## 🇬🇧

Code 43 does not automatically mean the GPU is physically defective.

Check:

```text
Driver
GPU
VRAM
Power
PCIe
BIOS
Windows
```

---

# 6. Driver Crash

Triệu chứng:

- Game crash.
- Black screen.
- Driver reset.
- Screen flickering.
- Application crash.

Xử lý:

```text
Check Driver
↓
Clean Install
↓
Remove Overclock
↓
Check Temperature
↓
Check PSU
↓
Stress Test
```

---

# 7. Artifact

## Symptoms

```text
Colored Dots
Lines
Texture Corruption
Geometry Errors
Flickering
Distorted Image
```

## Possible Causes

```text
VRAM Failure
GPU Failure
Overclock
Temperature
Driver
Power
```

## Troubleshooting

```text
Return to Stock
↓
Check Temperature
↓
Reinstall Driver
↓
Check Power
↓
Stress Test
↓
VRAM Test
↓
Cross-Test
```

---

# 8. GPU Overheating

## Symptoms

- High GPU temperature.
- Fan noise.
- Performance reduction.
- Thermal throttling.
- Crash.

## Causes

- Dust.
- Poor airflow.
- Fan failure.
- Thermal paste degradation.
- Thermal pad problem.
- High ambient temperature.

## Solution

```text
Clean GPU
↓
Check Fans
↓
Check Heatsink
↓
Improve Airflow
↓
Check Thermal Interface
↓
Retest
```

---

# 9. GPU Fan Not Spinning

### 🇻🇳

Trước tiên kiểm tra GPU có:

```text
Zero RPM
Fan Stop
0dB
```

Nếu có, fan không quay khi idle có thể hoàn toàn bình thường.

Nếu GPU nóng nhưng fan không quay:

```text
Check Fan
↓
Check Fan Connector
↓
Check Fan Curve
↓
Test Under Load
```

### 🇬🇧

First determine whether the GPU supports:

```text
Zero RPM
Fan Stop
0dB
```

If so, the fan may normally remain stopped at low temperatures.

If the GPU becomes hot while the fan remains stopped:

```text
Check Fan
↓
Check Fan Connector
↓
Check Fan Curve
↓
Test Under Load
```

---

# 10. GPU Crash Under Load

Possible causes:

```text
GPU Temperature
PSU
Driver
VRAM
GPU Hardware
Overclock
Power Delivery
```

Troubleshooting:

```text
Return to Stock
↓
Monitor Temperature
↓
Check PSU
↓
Reinstall Driver
↓
Stress Test
↓
Cross-Test
```

---

# 11. Low GPU Performance

Kiểm tra:

```text
GPU Utilization
GPU Clock
Memory Clock
VRAM Usage
Temperature
Power Limit
CPU Usage
Driver
PCIe Link
Background Applications
```

Các nguyên nhân:

- Thermal throttling.
- CPU bottleneck.
- Power limit.
- Driver.
- PCIe configuration.
- Background applications.
- Incorrect settings.

---

# 12. PCIe Link Problem

GPU-Z có thể hiển thị:

```text
PCIe x16 @ x16
```

Nếu dưới tải vẫn chỉ:

```text
PCIe x16 @ x1
```

cần kiểm tra:

- GPU seating.
- PCIe slot.
- BIOS.
- CPU PCIe lanes.
- Motherboard.
- Hardware.

**Lưu ý:** Khi idle GPU có thể tự giảm link speed để tiết kiệm điện.

---

# 13. Screen Flickering

Possible causes:

```text
Display Cable
Monitor
Driver
Refresh Rate
Adaptive Sync
GPU
```

Troubleshooting:

```text
Replace Cable
↓
Change Monitor Input
↓
Change Refresh Rate
↓
Disable Adaptive Sync Temporarily
↓
Reinstall Driver
↓
Test Another Monitor
↓
Test Another GPU
```

---

# 14. Random Restart

Có thể do:

- PSU.
- GPU.
- CPU.
- RAM.
- Motherboard.
- Temperature.
- Driver.

Kiểm tra:

```text
Event Viewer
PSU
GPU Temperature
CPU Temperature
RAM
GPU Stress Test
CPU Stress Test
```

---

# 15. GPU Works in Another PC

Nếu VGA hoạt động tốt ở PC khác:

Khả năng lỗi nằm ở:

```text
Current Motherboard
Current PSU
BIOS
PCIe Slot
Driver
Platform
Power
```

Thực hiện cross-test:

```text
Known-Good GPU
+
Problem PC
```

---

# 16. GPU Fails in Multiple PCs

Nếu VGA không hoạt động trên nhiều hệ thống đã biết là tốt:

Khả năng phần cứng lỗi tăng lên.

Có thể liên quan:

- GPU core.
- VRAM.
- VRM.
- Power circuit.
- PCB.
- VBIOS.

Cần sửa chữa chuyên sâu nếu cần.

---

# 17. Troubleshooting Decision Tree

```text
                    VGA PROBLEM
                         |
                  GPU DETECTED?
                   /          \
                 NO            YES
                 |              |
          Check Hardware     Driver OK?
          Check Power         /      \
          Check PCIe         NO      YES
          Check BIOS         |         |
                         Fix Driver   Stable?
                                      /   \
                                    NO     YES
                                    |       |
                              Check Temp   PASS
                              Check PSU
                              Check VRAM
                              Check GPU
```

---

# 18. Troubleshooting Checklist

```text
[ ] Problem reproduced
[ ] Monitor checked
[ ] Cable checked
[ ] GPU reseated
[ ] PCIe slot checked
[ ] GPU power checked
[ ] PSU checked
[ ] BIOS checked
[ ] Device Manager checked
[ ] Driver checked
[ ] GPU temperature checked
[ ] Fan checked
[ ] GPU clock checked
[ ] VRAM checked
[ ] Stress test performed
[ ] Cross-test performed
[ ] Final result documented
```

---

# 19. Troubleshooting Report

```text
=================================
VGA TROUBLESHOOTING REPORT
=================================

Date:
Technician:

GPU:
Model:
Serial Number:

Problem:

Symptoms:

System:
CPU:
Motherboard:
RAM:
PSU:
OS:
Driver:

Initial Diagnosis:

Tests Performed:

Test Results:

Root Cause:

Solution:

Verification:

Final Status:

[ ] Resolved
[ ] Partially Resolved
[ ] Hardware Failure
[ ] Requires Further Diagnosis

Notes:
```
