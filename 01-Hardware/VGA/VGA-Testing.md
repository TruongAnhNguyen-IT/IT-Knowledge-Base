# VGA Testing

> **Tiếng Việt:** Quy trình kiểm tra VGA từ ngoại quan, nhận diện phần cứng, driver, nhiệt độ, stress test đến benchmark.  
> **English:** A complete graphics card testing procedure covering physical inspection, hardware detection, drivers, temperature, stress testing, and benchmarking.

---

# 1. Mục tiêu | Objectives

## 🇻🇳

Mục tiêu kiểm tra:

- VGA có hoạt động không.
- VGA có được nhận không.
- Driver có hoạt động không.
- Nhiệt độ có bình thường không.
- Fan có hoạt động không.
- VRAM có ổn định không.
- GPU có artifact không.
- GPU có crash không.
- Hiệu năng có bất thường không.

## 🇬🇧

Testing objectives:

- Determine whether the GPU works.
- Verify GPU detection.
- Verify driver operation.
- Check temperature.
- Check fan operation.
- Check VRAM stability.
- Detect artifacts.
- Detect crashes.
- Identify abnormal performance.

---

# 2. Visual Inspection

Kiểm tra:

```text
PCB
PCIe Connector
Power Connector
Fans
Heatsink
Backplate
Thermal Pads
Capacitors
VRM Area
Display Outputs
```

Tìm:

- Burn marks.
- Corrosion.
- Broken components.
- Bent PCB.
- Damaged connector.
- Broken fan.

---

# 3. Installation Inspection

Đảm bảo:

```text
GPU fully inserted
PCIe latch locked
GPU bracket secured
Power connectors fully inserted
Display cable connected
```

---

# 4. BIOS/POST Test

Khởi động máy.

Kiểm tra:

- Display output.
- POST.
- BIOS/UEFI.
- GPU initialization.

Nếu không có hình:

```text
Monitor
↓
Cable
↓
GPU
↓
Power
↓
RAM
↓
Motherboard
```

---

# 5. Windows Detection Test

Mở:

```text
Device Manager
→ Display adapters
```

Kết quả mong muốn:

```text
GPU detected
No yellow warning
Device enabled
Driver installed
```

---

# 6. GPU-Z Test

Kiểm tra:

```text
GPU Name
GPU Technology
BIOS Version
VRAM
Memory Type
Memory Bus
Bus Interface
Driver
GPU Clock
Memory Clock
```

---

# 7. HWiNFO Monitoring

Theo dõi:

```text
GPU Temperature
GPU Hotspot
GPU Utilization
GPU Clock
Memory Clock
VRAM Usage
Fan Speed
Power Consumption
```

---

# 8. Idle Test

## 🇻🇳

Khi idle:

- GPU utilization thường thấp.
- Clock có thể giảm.
- Fan có thể dừng tùy GPU.
- Temperature phụ thuộc môi trường.

## 🇬🇧

During idle:

- GPU utilization is usually low.
- GPU clocks may decrease.
- Fans may stop depending on the GPU.
- Temperature depends on the environment.

---

# 9. Load Test

Đưa GPU vào tải bằng:

- FurMark.
- OCCT.
- 3DMark.
- Unigine.

Theo dõi:

```text
Temperature
Clock
Power
Fan
GPU Usage
VRAM
Artifacts
Crashes
```

---

# 10. Stress Test

Stress test phải được thực hiện có kiểm soát.

Quy trình:

```text
Start monitoring
↓
Start stress test
↓
Monitor temperature
↓
Monitor clocks
↓
Monitor power
↓
Observe artifacts
↓
Observe system stability
↓
Stop test
↓
Record result
```

Nếu nhiệt độ hoặc hành vi hệ thống bất thường, dừng test và chẩn đoán.

---

# 11. Benchmark

Có thể sử dụng:

- 3DMark.
- Unigine Heaven.
- Unigine Superposition.

Benchmark dùng để:

- So sánh hiệu năng.
- Kiểm tra hiệu năng sau sửa chữa.
- Phát hiện hiệu năng thấp bất thường.

---

# 12. Artifact Test

Dấu hiệu:

```text
Colored pixels
Lines
Texture corruption
Geometry corruption
Flickering
Screen distortion
```

Nếu xuất hiện:

```text
Check temperature
↓
Remove overclock
↓
Check driver
↓
Check power
↓
Test VRAM
↓
Cross-test GPU
```

---

# 13. Fan Test

Kiểm tra:

- Fan spin.
- Fan speed.
- Fan noise.
- Fan control.
- Bearing noise.

**Lưu ý:** Zero RPM/Fan Stop có thể khiến fan không quay khi GPU tải thấp.

---

# 14. Display Output Test

Kiểm tra từng cổng có trên GPU:

```text
HDMI → PASS / FAIL
DisplayPort → PASS / FAIL
DVI → PASS / FAIL
USB-C → PASS / FAIL
```

Không phải GPU nào cũng có tất cả các cổng.

---

# 15. Multi-Monitor Test

Kiểm tra:

```text
Monitor 1
Monitor 2
Monitor 3
```

Kiểm tra:

- Detection.
- Resolution.
- Refresh rate.
- HDR.
- Adaptive Sync.
- Display arrangement.

---

# 16. Gaming Test

Kiểm tra:

```text
FPS
Frame Time
GPU Usage
CPU Usage
VRAM Usage
GPU Temperature
GPU Clock
Power
Stability
```

Không đánh giá GPU chỉ dựa trên FPS.

---

# 17. Test Matrix

| Test | Result |
|---|---|
| Visual Inspection | PASS / FAIL |
| BIOS Detection | PASS / FAIL |
| Windows Detection | PASS / FAIL |
| Driver | PASS / FAIL |
| GPU-Z | PASS / FAIL |
| Idle | PASS / FAIL |
| Load | PASS / FAIL |
| Temperature | PASS / FAIL |
| Fan | PASS / FAIL |
| Artifact | PASS / FAIL |
| Benchmark | PASS / FAIL |
| Display Output | PASS / FAIL |
| Gaming | PASS / FAIL |

---

# 18. VGA Test Report

```text
=================================
VGA TEST REPORT
=================================

Date:
Technician:

GPU:
Brand:
Model:
Serial Number:

System:
CPU:
Motherboard:
RAM:
PSU:
Case:
OS:
Driver:

---------------------------------
PHYSICAL INSPECTION
---------------------------------

PCB:
PCIe Connector:
Power Connector:
Fans:
Heatsink:
Display Outputs:

Result:

---------------------------------
DETECTION
---------------------------------

BIOS:
Device Manager:
GPU-Z:

Result:

---------------------------------
TEMPERATURE
---------------------------------

Idle:
Load:
Hotspot:

Result:

---------------------------------
STABILITY
---------------------------------

Stress Test:
Duration:
Artifacts:
Crash:

Result:

---------------------------------
BENCHMARK
---------------------------------

Benchmark:
Score:
Average FPS:

Result:

---------------------------------
FINAL RESULT
---------------------------------

[ ] PASS
[ ] FAIL
[ ] NEED FURTHER TESTING

Notes:
```
