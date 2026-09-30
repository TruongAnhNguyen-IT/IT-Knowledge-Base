# CPU Troubleshooting / Xử lý sự cố CPU

## 1. Troubleshooting Overview / Tổng quan xử lý sự cố

**Tiếng Việt**

CPU troubleshooting là quá trình xác định nguyên nhân gây ra lỗi liên quan đến CPU hoặc hệ thống xử lý.

**English**

CPU troubleshooting is the process of identifying and resolving problems related to the processor or CPU-related system components.

---

# 2. Common CPU Problems / Các lỗi thường gặp

Các lỗi phổ biến:

1. PC không khởi động.
2. Không có hình ảnh.
3. CPU không được nhận diện.
4. CPU quá nóng.
5. CPU usage cao.
6. Máy tự restart.
7. Máy bị crash/BSOD.
8. CPU chạy không đúng xung nhịp.
9. Hiệu năng CPU thấp.
10. Hệ thống không ổn định sau khi nâng cấp CPU.

---

# 3. PC Does Not Boot / Máy không khởi động

## Symptoms / Triệu chứng

- Press power button but no POST.
- No display.
- Motherboard CPU debug LED.
- System repeatedly restarts.
- System powers on then shuts down.

## Possible Causes / Nguyên nhân

- CPU installed incorrectly.
- CPU power connector not connected.
- BIOS incompatibility.
- RAM problem.
- Motherboard problem.
- PSU problem.
- CPU failure.

## Troubleshooting / Cách kiểm tra

### Step 1

Power off the computer.

### Step 2

Disconnect AC power.

### Step 3

Check CPU installation.

### Step 4

Check CPU power connector.

Common connectors:

```text
4-pin ATX12V
8-pin EPS12V
4+4 EPS
```

### Step 5

Check RAM.

Try:

- Reseat RAM.
- Test one RAM module.
- Try another memory slot.

### Step 6

Clear CMOS.

### Step 7

Check motherboard debug LEDs.

### Step 8

Check CPU compatibility and BIOS.

---

# 4. No Display After CPU Upgrade / Không có hình sau khi nâng cấp CPU

## Possible Causes

- BIOS does not support CPU.
- CPU not installed correctly.
- RAM problem.
- GPU problem.
- CPU has no integrated graphics.
- Display cable connected to wrong output.

## Troubleshooting

Check:

```text
CPU
↓
Motherboard
↓
BIOS
↓
RAM
↓
GPU / iGPU
↓
Display cable
```

---

# 5. CPU Not Detected / Không nhận CPU

## Check

- CPU socket
- CPU installation
- Motherboard BIOS
- CPU Support List
- CPU power connector
- Socket pins
- Motherboard condition

### Important

For LGA sockets, inspect motherboard socket pins carefully.

Bent socket pins can cause:

- No POST
- Memory channel problems
- PCIe problems
- CPU detection issues

---

# 6. High CPU Temperature / CPU quá nóng

## Possible Causes

- Dust
- Poor airflow
- Fan failure
- Thermal paste
- Cooler mounting
- High workload
- High ambient temperature
- Incorrect power settings

## Troubleshooting

1. Check CPU usage.
2. Check fan speed.
3. Clean cooler.
4. Check thermal paste.
5. Reinstall cooler if necessary.
6. Check airflow.
7. Monitor temperature again.

---

# 7. High CPU Usage / CPU Usage cao

## Possible Causes

- Application
- Windows service
- Background process
- Browser
- Windows Update
- Malware
- Virtual machine
- Software bug

## Troubleshooting

Open:

```text
Task Manager
→ Processes
→ CPU
```

Sort by CPU usage.

Identify the process causing high CPU usage.

Then check:

- Application name
- Startup behavior
- Background service
- Windows service
- Scheduled tasks

---

# 8. Random Restart / Máy tự khởi động lại

## Possible Causes

- CPU overheating
- PSU problem
- RAM problem
- Motherboard problem
- BIOS instability
- Driver problem
- Hardware failure

## Troubleshooting

Check:

1. CPU temperature
2. RAM
3. PSU
4. Motherboard
5. BIOS
6. Windows Event Viewer

---

# 9. Blue Screen / BSOD

Possible causes include:

- Driver
- RAM
- CPU instability
- Motherboard
- Storage
- Windows corruption
- Overclocking

Useful tools:

```text
Event Viewer
Reliability Monitor
Windows Memory Diagnostic
CPU stress test
Hardware monitoring software
```

---

# 10. CPU Clock Lower Than Expected / Xung CPU thấp

## Possible Causes

- Thermal throttling
- Power limit
- Power-saving mode
- BIOS configuration
- CPU workload
- Laptop power mode
- Cooling limitation

Check:

- CPU temperature
- CPU utilization
- CPU power
- CPU clock
- BIOS settings
- Windows power settings

---

# 11. Performance Problems / Hiệu năng thấp

Không nên kết luận CPU bị lỗi chỉ vì hiệu năng thấp.

Kiểm tra:

```text
CPU
├── Temperature
├── Usage
├── Clock
├── Power
└── Throttling

RAM
├── Capacity
└── Usage

Storage
├── Health
└── Performance

GPU
├── Usage
└── Temperature

Software
└── Background processes
```

---

# 12. CPU Upgrade Troubleshooting / Xử lý sau khi nâng cấp CPU

Sau khi thay CPU:

### Check 1

System POST.

### Check 2

BIOS detects CPU.

### Check 3

CPU model is correct.

### Check 4

RAM is detected.

### Check 5

Storage boots normally.

### Check 6

CPU temperature is normal.

### Check 7

Run stability test.

### Check 8

Check Windows Device Manager.

---

# 13. Basic Troubleshooting Workflow / Quy trình xử lý cơ bản

```text
Identify Symptoms
       ↓
Check Physical Connections
       ↓
Check CPU Installation
       ↓
Check RAM
       ↓
Check BIOS
       ↓
Check CPU Compatibility
       ↓
Check Temperature
       ↓
Check PSU
       ↓
Run Diagnostic Tests
       ↓
Identify Root Cause
       ↓
Apply Fix
       ↓
Verify System Stability
       ↓
Document Result
```

---

# 14. Troubleshooting Checklist / Checklist

| Item | Status |
|---|---|
| Power | ☐ |
| CPU Installation | ☐ |
| CPU Power Connector | ☐ |
| RAM | ☐ |
| Motherboard | ☐ |
| BIOS | ☐ |
| CPU Compatibility | ☐ |
| GPU / iGPU | ☐ |
| CPU Temperature | ☐ |
| PSU | ☐ |
| Storage | ☐ |
| Drivers | ☐ |
| Windows | ☐ |
| Stability Test | ☐ |

---

# 15. Documentation / Ghi nhận lỗi

Khi xử lý một lỗi thực tế, nên ghi lại:

```text
Date:
Device:
CPU:
Motherboard:
RAM:
PSU:
Operating System:

Problem:
Symptoms:

Initial Diagnosis:

Troubleshooting Steps:

Root Cause:

Solution:

Verification:

Result:
```

**English:**

```text
Date:
Device:
CPU:
Motherboard:
RAM:
PSU:
Operating System:

Problem:
Symptoms:

Initial Diagnosis:

Troubleshooting Steps:

Root Cause:

Solution:

Verification:

Result:
```

---

# 16. Important Note / Lưu ý

Không nên thay CPU ngay khi hệ thống có lỗi.

CPU failure thường cần được xác minh bằng quá trình loại trừ các nguyên nhân khác như:

- RAM
- PSU
- Motherboard
- BIOS
- Cooling
- GPU
- Storage
- Operating System

> **Always diagnose systematically before replacing hardware.**

> **Luôn chẩn đoán có hệ thống trước khi thay thế phần cứng.**
