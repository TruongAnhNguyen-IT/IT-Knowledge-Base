# VGA Compatibility

> **Tiếng Việt:** Kiểm tra khả năng tương thích giữa VGA và hệ thống máy tính.  
> **English:** Checking graphics card compatibility with the computer system.

---

# 1. Mục đích | Purpose

## 🇻🇳

Trước khi lắp VGA cần xác định VGA có phù hợp với:

- Motherboard.
- CPU.
- PSU.
- Case.
- Monitor.
- Operating System.
- Driver.
- PCIe interface.

## 🇬🇧

Before installing a GPU, verify compatibility with:

- Motherboard.
- CPU.
- PSU.
- Case.
- Monitor.
- Operating System.
- Driver.
- PCIe interface.

---

# 2. Motherboard Compatibility

## 🇻🇳

Kiểm tra motherboard có khe:

```text
PCIe x16
```

Vị trí thường là khe PCIe x16 đầu tiên gần CPU.

Cần kiểm tra:

- PCIe generation.
- PCIe lane configuration.
- Slot availability.
- BIOS support.
- Physical clearance.

## 🇬🇧

Verify that the motherboard has:

```text
PCIe x16
```

The primary slot is usually the PCIe x16 slot closest to the CPU.

Check:

- PCIe generation.
- PCIe lane configuration.
- Slot availability.
- BIOS support.
- Physical clearance.

---

# 3. PCIe Generation Compatibility

Ví dụ:

```text
Motherboard:
PCIe 4.0 x16

GPU:
PCIe 4.0 x16
```

→ Compatible.

Ví dụ:

```text
Motherboard:
PCIe 3.0 x16

GPU:
PCIe 4.0 x16
```

→ Thường vẫn có thể hoạt động nhưng GPU sẽ giao tiếp theo khả năng chung của nền tảng.

→ Usually works, but the link operates according to the capabilities supported by the platform and GPU.

---

# 4. Physical Compatibility

## 🇻🇳

Kiểm tra:

```text
GPU Length
GPU Height
GPU Thickness
Slot Width
Front Fan Clearance
Radiator Clearance
Drive Cage Clearance
```

Ví dụ:

```text
GPU:
Length = 320 mm

Case:
Maximum GPU Length = 340 mm

Result:
Compatible
```

Nhưng nếu GPU dày 3.5 slot, cần kiểm tra các PCIe slot bên cạnh.

## 🇬🇧

Check:

```text
GPU Length
GPU Height
GPU Thickness
Slot Width
Front Fan Clearance
Radiator Clearance
Drive Cage Clearance
```

Example:

```text
GPU:
Length = 320 mm

Case:
Maximum GPU Length = 340 mm

Result:
Compatible
```

However, a 3.5-slot GPU may block adjacent expansion slots.

---

# 5. PSU Compatibility

## 🇻🇳

Kiểm tra:

1. PSU capacity.
2. PSU quality.
3. GPU power requirement.
4. CPU power consumption.
5. Other system components.
6. Required GPU power connectors.

Không nên chỉ nhìn công suất Watt.

Một PSU 750 W chất lượng tốt có thể phù hợp hơn PSU 850 W chất lượng kém.

## 🇬🇧

Check:

1. PSU capacity.
2. PSU quality.
3. GPU power requirement.
4. CPU power consumption.
5. Other system components.
6. Required GPU power connectors.

Do not judge a PSU only by wattage.

A good-quality 750 W PSU may be a better choice than a poor-quality 850 W PSU.

---

# 6. Power Connector Compatibility

Các loại thường gặp:

```text
6-pin
8-pin
6+2-pin
12VHPWR
12V-2x6
```

### 🇻🇳

Phải sử dụng dây phù hợp với PSU.

Không nên tự ý dùng:

- Dây không rõ nguồn.
- Adapter chất lượng kém.
- Dây modular không đúng chuẩn PSU.

### 🇬🇧

Use cables appropriate for the PSU.

Avoid:

- Unknown cables.
- Poor-quality adapters.
- Modular cables from incompatible PSU platforms.

---

# 7. CPU Compatibility

## 🇻🇳

Không bắt buộc CPU và GPU cùng thương hiệu.

Có thể dùng:

```text
Intel CPU + NVIDIA GPU
Intel CPU + AMD GPU
AMD CPU + NVIDIA GPU
AMD CPU + AMD GPU
```

Cần xem thêm:

- CPU bottleneck.
- PCIe support.
- CPU performance.
- Application requirements.

## 🇬🇧

The CPU and GPU do not need to be from the same manufacturer.

Possible configurations include:

```text
Intel CPU + NVIDIA GPU
Intel CPU + AMD GPU
AMD CPU + NVIDIA GPU
AMD CPU + AMD GPU
```

Also consider:

- CPU bottleneck.
- PCIe support.
- CPU performance.
- Application requirements.

---

# 8. RAM Compatibility

## 🇻🇳

VGA rời có VRAM riêng nên VRAM không cần giống RAM hệ thống.

Ví dụ:

```text
System RAM = 16 GB
GPU VRAM = 8 GB
```

→ Hoàn toàn có thể sử dụng.

RAM hệ thống vẫn ảnh hưởng đến hiệu năng tổng thể của hệ thống.

## 🇬🇧

A discrete GPU has dedicated VRAM, so system RAM does not need to match VRAM.

Example:

```text
System RAM = 16 GB
GPU VRAM = 8 GB
```

→ This is a valid configuration.

System RAM still affects overall system performance.

---

# 9. Case Compatibility

Kiểm tra:

```text
GPU Length
GPU Height
GPU Thickness
PCIe Slot Clearance
Power Cable Clearance
Front Radiator Clearance
Airflow
```

Đặc biệt chú ý đầu nguồn GPU có thể cần khoảng trống để uốn dây đúng cách.

---

# 10. Monitor Compatibility

Kiểm tra:

- HDMI.
- DisplayPort.
- DVI.
- VGA.
- USB-C where supported.

Kiểm tra thêm:

```text
Resolution
Refresh Rate
HDR
Adaptive Sync
Color Depth
Number of Displays
```

---

# 11. Operating System Compatibility

## 🇻🇳

Kiểm tra GPU có driver hỗ trợ:

- Windows 10.
- Windows 11.
- Linux.
- Các OS khác nếu GPU hỗ trợ.

## 🇬🇧

Verify driver support for:

- Windows 10.
- Windows 11.
- Linux.
- Other supported operating systems.

---

# 12. Driver Compatibility

Kiểm tra:

```text
GPU Model
Operating System
Driver Version
Architecture
Application Support
```

Không cài driver chỉ dựa trên tên gần giống.

---

# 13. BIOS/UEFI Compatibility

Trong một số hệ thống cần kiểm tra:

- UEFI.
- Legacy/CSM.
- Primary Display.
- PCIe configuration.
- Resizable BAR.
- Above 4G Decoding.

Không thay đổi BIOS settings nếu không hiểu mục đích.

---

# 14. Multi-GPU Compatibility

Một số hệ thống có thể hỗ trợ nhiều GPU, nhưng cần kiểm tra:

- Motherboard.
- PSU.
- CPU PCIe lanes.
- Software support.
- Physical clearance.
- Cooling.

Không phải mọi GPU đều hỗ trợ multi-GPU gaming.

---

# 15. Compatibility Checklist

```text
Motherboard
[ ] PCIe x16 slot
[ ] Slot available
[ ] BIOS support
[ ] PCIe compatibility

CPU
[ ] Platform supported
[ ] Performance appropriate

PSU
[ ] Sufficient wattage
[ ] Quality PSU
[ ] Correct connectors
[ ] Correct cables

Case
[ ] Length fits
[ ] Height fits
[ ] Thickness fits
[ ] Power cable clearance
[ ] Airflow sufficient

Monitor
[ ] Correct connector
[ ] Resolution supported
[ ] Refresh rate supported

Software
[ ] OS supported
[ ] Driver available
```

---

# 16. Compatibility Report

```text
GPU:
Model:

Motherboard:
Model:
PCIe Slot:

CPU:
Model:

PSU:
Model:
Wattage:
Connectors:

Case:
Maximum GPU Length:

Monitor:
Resolution:
Refresh Rate:
Connector:

Operating System:
Driver:

Result:
[ ] Compatible
[ ] Not Compatible
[ ] Requires Verification

Notes:
```
