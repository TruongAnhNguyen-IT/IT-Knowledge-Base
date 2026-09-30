# Mainboard Troubleshooting

> A systematic troubleshooting process helps isolate motherboard, CPU, RAM, GPU, power and peripheral failures.

> Troubleshooting có hệ thống giúp xác định lỗi nằm ở mainboard, CPU, RAM, GPU, nguồn hoặc thiết bị ngoại vi.

---

# 1. Troubleshooting Principle

## 🇻🇳 Tiếng Việt

Không thay linh kiện ngẫu nhiên.

Áp dụng:

```text
Observe
   ↓
Reproduce
   ↓
Isolate
   ↓
Test
   ↓
Verify
   ↓
Document
```

Nguyên tắc:

> Thay đổi một yếu tố tại một thời điểm.

## 🇬🇧 English

Do not replace components randomly.

Use:

```text
Observe
   ↓
Reproduce
   ↓
Isolate
   ↓
Test
   ↓
Verify
   ↓
Document
```

Change one variable at a time whenever possible.

---

# 2. PC Không Lên Nguồn

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
AC power
PSU switch
Power cable
24-pin ATX
CPU EPS
Power button
Front panel connector
PSU
Motherboard
```

Quy trình:

```text
Wall power
↓
PSU
↓
24-pin
↓
CPU EPS
↓
Power switch
↓
Motherboard
```

## 🇬🇧 English

Check:

- AC power.
- PSU switch.
- Power cable.
- 24-pin ATX.
- CPU EPS.
- Power switch.
- Front panel header.
- PSU.
- Motherboard.

---

# 3. Có Nguồn Nhưng Không POST

## 🇻🇳 Tiếng Việt

Kiểm tra theo thứ tự:

```text
CPU
↓
CPU power
↓
RAM
↓
GPU / display
↓
BIOS
↓
Motherboard
```

Tháo bớt thiết bị:

```text
Storage
USB devices
Additional PCIe cards
Extra RAM
```

Chỉ giữ cấu hình tối thiểu.

## 🇬🇧 English

If the system powers on but does not POST:

1. Check CPU.
2. Check CPU power.
3. Test one RAM module.
4. Check display/GPU.
5. Check BIOS.
6. Check motherboard.

Remove unnecessary peripherals.

---

# 4. No Display

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
Monitor
Display cable
Input source
GPU
GPU power
Motherboard display output
CPU integrated graphics
RAM
POST
```

Lưu ý:

Cổng HDMI/DP trên motherboard chỉ hoạt động nếu CPU/platform hỗ trợ integrated graphics.

## 🇬🇧 English

Check:

- Monitor.
- Cable.
- Input source.
- GPU.
- GPU power.
- Motherboard display output.
- CPU integrated graphics.
- RAM.
- POST.

Motherboard video outputs require appropriate CPU/platform graphics support.

---

# 5. RAM Not Detected

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
RAM seating
DIMM slot
Memory module
CPU socket
CPU memory controller
BIOS
Memory compatibility
```

Quy trình:

```text
Power OFF
↓
Remove RAM
↓
Inspect contacts/slot
↓
Install one module
↓
Use recommended slot
↓
Clear CMOS if needed
↓
POST
```

## 🇬🇧 English

Check:

- RAM seating.
- DIMM slot.
- Memory module.
- CPU socket.
- Memory controller.
- BIOS.
- Compatibility.

Test one module at a time.

---

# 6. CPU Not Detected

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
CPU installation
CPU socket
Bent pins
CPU EPS power
BIOS version
CPU support
Cooling installation
```

Một số lỗi CPU detection có thể liên quan đến socket pin hoặc BIOS.

## 🇬🇧 English

Check:

- CPU installation.
- Socket condition.
- Bent pins.
- CPU EPS power.
- BIOS version.
- CPU support.
- Cooler installation.

---

# 7. SSD Not Detected

## 🇻🇳 Tiếng Việt

### SATA

Kiểm tra:

```text
SATA cable
SATA power
SATA port
BIOS
Drive health
```

### M.2

Kiểm tra:

```text
M.2 slot
M.2 protocol
NVMe/SATA compatibility
BIOS
PCIe lane sharing
```

## 🇬🇧 English

For SATA:

- Cable.
- Power.
- Port.
- BIOS.
- Drive health.

For M.2:

- Slot.
- Protocol.
- Compatibility.
- BIOS.
- Lane sharing.

---

# 8. USB Not Working

## 🇻🇳 Tiếng Việt

Xác định:

```text
One port?
One group?
All USB?
Front only?
Rear only?
```

Kiểm tra:

- USB device.
- Port.
- Driver.
- BIOS.
- Internal header.
- Power.
- Windows Device Manager.

## 🇬🇧 English

Determine whether the problem affects:

- One port.
- One USB group.
- All USB ports.
- Front USB.
- Rear USB.

Then test:

- Device.
- Port.
- Driver.
- BIOS.
- Internal header.
- Power.

---

# 9. Ethernet Not Working

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
RJ-45 cable
Switch/router
Link LED
NIC
Driver
IP
DHCP
DNS
```

Commands:

```cmd
ipconfig /all
ping 127.0.0.1
ping <gateway>
nslookup google.com
```

## 🇬🇧 English

Check:

- Ethernet cable.
- Switch/router.
- Link LED.
- NIC.
- Driver.
- IP configuration.
- DHCP.
- DNS.

---

# 10. Audio Not Working

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
Audio device
Driver
Default output
Volume
Rear audio
Front audio
HD Audio header
```

## 🇬🇧 English

Check:

- Audio device.
- Driver.
- Default output.
- Volume.
- Rear audio.
- Front audio.
- Front-panel audio header.

---

# 11. Random Restart

## 🇻🇳 Tiếng Việt

Có thể liên quan đến:

```text
PSU
CPU temperature
VRM
RAM
BIOS
XMP/EXPO
GPU
Motherboard
```

Kiểm tra:

```text
Temperature
Event Viewer
Memory errors
BIOS settings
Power delivery
```

## 🇬🇧 English

Possible causes include:

- PSU.
- CPU temperature.
- VRM.
- RAM instability.
- BIOS settings.
- XMP/EXPO.
- GPU.
- Motherboard.

---

# 12. Overheating

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
CPU cooler
Thermal paste
CPU fan
Case airflow
VRM temperature
Chipset temperature
Fan curve
Ambient temperature
```

## 🇬🇧 English

Check:

- CPU cooler.
- Thermal paste.
- CPU fan.
- Case airflow.
- VRM temperature.
- Chipset temperature.
- Fan curve.
- Ambient temperature.

---

# 13. BIOS Boot Loop

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
Boot drive
Boot priority
UEFI/Legacy
Windows Boot Manager
Storage detection
Secure Boot
CMOS settings
```

Có thể thử:

```text
Load Optimized Defaults
Save & Exit
```

Nếu cần:

```text
Clear CMOS
```

## 🇬🇧 English

Check:

- Boot drive.
- Boot priority.
- UEFI/Legacy mode.
- Windows Boot Manager.
- Storage detection.
- Secure Boot.
- CMOS configuration.

---

# 14. Debug LED

## 🇻🇳 Tiếng Việt

Một số mainboard có:

```text
CPU
DRAM
VGA
BOOT
```

Ví dụ:

```text
CPU LED ON
→ Check CPU / EPS / BIOS / socket

DRAM LED ON
→ Check RAM / slots / compatibility

VGA LED ON
→ Check GPU / display / power

BOOT LED ON
→ Check storage / boot configuration
```

## 🇬🇧 English

Debug LEDs may indicate:

```text
CPU
DRAM
VGA
BOOT
```

Use the motherboard manual to interpret the exact LED behavior.

---

# 15. Clear CMOS Troubleshooting

## 🇻🇳 Tiếng Việt

Có thể dùng khi:

- Sai BIOS configuration.
- RAM profile không ổn định.
- Overclock thất bại.
- Không POST sau khi thay đổi BIOS.

Sau Clear CMOS cần kiểm tra lại:

```text
Date/Time
Boot Mode
Boot Priority
XMP/EXPO
Fan settings
Secure Boot
TPM
Virtualization
```

## 🇬🇧 English

Clear CMOS may help with:

- Incorrect firmware configuration.
- Memory profile instability.
- Failed overclocking.
- POST failure after firmware changes.

After reset, verify important settings again.

---

# 16. Troubleshooting Decision Tree

```text
POWER ON?
│
├── NO
│   ├── AC Power
│   ├── PSU
│   ├── 24-pin
│   ├── CPU EPS
│   └── Power Switch
│
└── YES
    │
    ├── POST?
    │   │
    │   ├── NO
    │   │   ├── CPU
    │   │   ├── RAM
    │   │   ├── GPU
    │   │   ├── BIOS
    │   │   └── Mainboard
    │   │
    │   └── YES
    │
    └── OS Boot?
        │
        ├── NO
        │   ├── Storage
        │   ├── Boot Mode
        │   └── Bootloader
        │
        └── YES
            │
            ├── USB
            ├── Ethernet
            ├── Audio
            ├── Storage
            └── Stability
```

---

# 17. Troubleshooting Record

```markdown
# Mainboard Troubleshooting Record

## Problem

- Date:
- Device:
- Motherboard:
- Symptoms:

## Environment

- CPU:
- RAM:
- GPU:
- Storage:
- PSU:
- BIOS:

## Initial Observation

-

## Tests

### Test 1

- Action:
- Result:

### Test 2

- Action:
- Result:

### Test 3

- Action:
- Result:

## Root Cause

-

## Solution

-

## Verification

-

## Final Result

- PASS / FAIL

## Notes

-
```

---

# Troubleshooting Principles

```text
Do not guess.
Do not replace everything.
Test systematically.
Record results.
Change one variable at a time.
Verify the final result.
Document the solution.
```
