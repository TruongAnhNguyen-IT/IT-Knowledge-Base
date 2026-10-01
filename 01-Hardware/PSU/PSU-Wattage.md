# PSU Wattage

## 🇻🇳 Tiếng Việt

## 1. Wattage là gì?

**Watt (W)** là đơn vị công suất.

PSU 650W có nghĩa PSU được thiết kế để cung cấp tổng công suất đầu ra theo giới hạn và điều kiện được nhà sản xuất quy định.

Không có nghĩa PC sẽ luôn tiêu thụ 650W.

Ví dụ:

```text
PSU = 650W
PC Load = 400W

Actual consumption ≠ 650W
```

---

# 2. Công thức cơ bản

```text
Power (W) = Voltage (V) × Current (A)
```

Ví dụ:

```text
12V × 20A = 240W
```

---

# 3. Tính tổng công suất

Có thể ước lượng:

```text
Total System Power
=
CPU
+
GPU
+
Motherboard
+
RAM
+
Storage
+
Fans
+
USB
+
Other Devices
```

---

# 4. CPU Power

CPU có thể tiêu thụ công suất khác nhau tùy:

- Model
- Workload
- Power limit
- Turbo behavior
- BIOS settings
- Temperature

Không nên chỉ dựa vào TDP để xác định chính xác PSU requirement.

---

# 5. GPU Power

GPU thường là một trong những thành phần tiêu thụ điện lớn nhất.

Cần xem:

- GPU model
- Board power
- Power limit
- Transient behavior
- Recommended PSU
- Required connector

---

# 6. Motherboard

Motherboard tiêu thụ điện cho:

- Chipset
- RAM
- Network
- Audio
- USB
- Storage controllers
- Expansion devices

---

# 7. RAM

RAM thường tiêu thụ ít điện hơn CPU/GPU.

Tổng RAM power phụ thuộc:

- Number of modules
- DDR generation
- Voltage
- Capacity
- Frequency
- Load

---

# 8. Storage

### SSD

Thông thường tiêu thụ ít điện.

### HDD

Có thể có mức tiêu thụ cao hơn trong quá trình spin-up.

Khi có nhiều HDD, cần xem xét cả startup behavior.

---

# 9. Fans

Mỗi fan có công suất tương đối nhỏ nhưng hệ thống nhiều fan có thể cộng lại.

Ví dụ:

```text
6 Fans × 3W
=
18W
```

---

# 10. USB Devices

USB devices cũng tiêu thụ điện.

Ví dụ:

- Keyboard
- Mouse
- USB HDD
- USB SSD
- RGB controller
- USB hub
- External devices

---

# 11. Headroom

Không nên chọn PSU vừa đúng mức estimated load.

Ví dụ:

```text
Estimated Load = 500W
```

Có thể cân nhắc PSU có capacity cao hơn để có khoảng dự phòng.

Headroom giúp hệ thống có thêm margin cho:

- Load changes
- GPU transient behavior
- Future upgrades
- Aging
- Additional devices

---

# 12. Ví dụ tính PSU

Giả sử:

```text
CPU       = 120W
GPU       = 250W
Motherboard = 60W
RAM       = 20W
SSD       = 10W
HDD       = 15W
Fans      = 20W
USB       = 15W
```

Tổng:

```text
120 + 250 + 60 + 20 + 10 + 15 + 20 + 15
= 510W
```

Estimated system load:

```text
≈ 510W
```

Không nên chọn PSU chỉ vì:

```text
PSU = 510W
```

Cần xem thêm PSU quality, +12V capacity, connector requirements và transient behavior.

---

# 13. +12V Capacity

Đây là thông số rất quan trọng.

Ví dụ PSU:

```text
Total Power = 650W

+12V = 54A
```

Công suất lý thuyết của +12V:

```text
12 × 54 = 648W
```

Điều này cho thấy phần lớn công suất của PSU tập trung vào +12V.

---

# 14. PSU Sizing Workflow

```text
Identify Components
        ↓
Estimate CPU Power
        ↓
Estimate GPU Power
        ↓
Estimate Other Components
        ↓
Calculate System Load
        ↓
Check +12V Capacity
        ↓
Check Connectors
        ↓
Add Headroom
        ↓
Select PSU
```

---

# 15. PSU Wattage Examples

### Office PC

Ví dụ:

```text
CPU = 65W
iGPU
RAM = 16W
SSD = 5W
Motherboard = 50W
Fans = 10W
```

Estimated:

```text
≈ 146W
```

Một PSU phù hợp sẽ cần xem thêm platform, efficiency, connectors và quality chứ không chỉ dựa vào watt.

---

### Gaming PC

Ví dụ:

```text
CPU = 120W
GPU = 300W
Motherboard = 60W
RAM = 30W
SSD = 10W
Fans = 30W
Other = 20W
```

Total:

```text
570W
```

Cần xem thêm peak/transient behavior và khuyến nghị của GPU/PSU manufacturer.

---

# 16. Too Little Wattage

PSU thiếu capacity có thể gây:

- Shutdown
- Restart
- GPU crash
- System instability
- Failure under heavy load

---

# 17. Too Much Wattage

PSU công suất lớn hơn nhu cầu không tự động làm PC tiêu thụ toàn bộ số Watt đó.

Ví dụ:

```text
PC Load = 350W

PSU = 850W
```

PC không mặc định tiêu thụ 850W.

---

## 🇬🇧 English

# PSU Wattage

## 1. What Is Wattage?

Wattage is the amount of electrical power a PSU can provide under specified conditions.

A 650W PSU does not mean the computer constantly consumes 650W.

Example:

```text
PSU Capacity = 650W
System Load = 400W
```

The PC consumes power according to its actual load.

---

## 2. Basic Formula

```text
Power (W) = Voltage (V) × Current (A)
```

Example:

```text
12V × 20A = 240W
```

---

## 3. Estimating System Power

```text
System Power
=
CPU
+
GPU
+
Motherboard
+
RAM
+
Storage
+
Fans
+
USB
+
Other Devices
```

---

## 4. CPU Power

CPU power consumption depends on:

- CPU model
- Workload
- Power limits
- Turbo behavior
- BIOS configuration
- Temperature

TDP should not be treated as an exact PSU requirement.

---

## 5. GPU Power

GPU power requirements depend on:

- GPU model
- Board power
- Power limit
- Transient behavior
- Manufacturer recommendation
- Required connectors

---

## 6. Motherboard Power

Motherboard power is used by:

- Chipset
- RAM
- Network
- Audio
- USB
- Storage controllers
- Expansion devices

---

## 7. RAM Power

RAM consumption depends on:

- Number of modules
- DDR generation
- Voltage
- Capacity
- Frequency
- Workload

---

## 8. Storage Power

### SSD

Usually has relatively low power consumption.

### HDD

May require higher power during spin-up.

Multiple HDD systems should consider startup behavior.

---

## 9. Fans

Fans individually consume relatively little power.

Example:

```text
6 × 3W fans
=
18W
```

---

## 10. USB Devices

USB devices also consume power.

Examples:

- Keyboard
- Mouse
- USB drives
- USB SSD
- RGB controllers
- USB hubs
- External devices

---

## 11. Headroom

Avoid selecting a PSU based solely on the exact estimated load.

Example:

```text
Estimated Load = 500W
```

A PSU with additional capacity provides margin for:

- Load changes
- GPU transient behavior
- Future upgrades
- Component aging
- Additional devices

---

## 12. Example Calculation

```text
CPU          = 120W
GPU          = 250W
Motherboard  = 60W
RAM          = 20W
SSD          = 10W
HDD          = 15W
Fans         = 20W
USB          = 15W
```

Total:

```text
510W
```

This does not mean that a 510W PSU is automatically the correct choice.

Also evaluate:

- +12V capacity
- PSU quality
- Connector requirements
- Transient behavior
- Manufacturer recommendations

---

## 13. +12V Capacity

Example:

```text
Total PSU Power = 650W
+12V = 54A
```

Theoretical +12V power:

```text
12 × 54 = 648W
```

This indicates that most of the PSU's capacity is available through the +12V output.

---

## 14. PSU Sizing Workflow

```text
Identify Components
        ↓
Estimate CPU Power
        ↓
Estimate GPU Power
        ↓
Estimate Other Loads
        ↓
Calculate System Load
        ↓
Check +12V Capacity
        ↓
Check Connectors
        ↓
Add Headroom
        ↓
Select PSU
```

---

## 15. Insufficient Capacity

An undersized PSU may result in:

- Shutdowns
- Reboots
- GPU crashes
- System instability
- Problems under heavy load

---

## 16. Excess Capacity

A higher-wattage PSU does not force the computer to consume its full rated capacity.

Example:

```text
System Load = 350W
PSU Capacity = 850W
```

The system does not automatically consume 850W.
