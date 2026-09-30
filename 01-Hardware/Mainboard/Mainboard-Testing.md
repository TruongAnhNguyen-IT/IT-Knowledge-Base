# Mainboard Testing

> Mainboard testing is the process of verifying motherboard functionality, hardware detection, stability and I/O operation.

> Kiểm tra mainboard là quá trình xác minh khả năng hoạt động, nhận diện phần cứng, độ ổn định và các cổng kết nối của mainboard.

---

# 1. Testing Objectives

## 🇻🇳 Tiếng Việt

Mục tiêu:

- Kiểm tra mainboard có POST hay không.
- Kiểm tra CPU.
- Kiểm tra RAM.
- Kiểm tra GPU/display.
- Kiểm tra storage.
- Kiểm tra USB.
- Kiểm tra Ethernet.
- Kiểm tra audio.
- Kiểm tra PCIe.
- Kiểm tra M.2.
- Kiểm tra SATA.
- Kiểm tra BIOS/UEFI.
- Kiểm tra stability.

## 🇬🇧 English

Testing objectives include:

- POST verification.
- CPU detection.
- RAM detection.
- Display output.
- Storage detection.
- USB testing.
- Ethernet testing.
- Audio testing.
- PCIe testing.
- M.2 testing.
- SATA testing.
- BIOS verification.
- Stability testing.

---

# 2. Basic Test Setup

## 🇻🇳 Tiếng Việt

Một cấu hình test tối thiểu:

```text
Motherboard
CPU
CPU Cooler
One RAM module
PSU
GPU if required
Keyboard
Monitor
Storage if OS testing is required
```

Không nên lắp quá nhiều linh kiện ngay từ đầu.

## 🇬🇧 English

A minimal test setup should contain:

```text
Motherboard
CPU
CPU Cooler
One RAM module
PSU
GPU if required
Keyboard
Monitor
```

Use the minimum hardware required for initial POST testing.

---

# 3. Visual Inspection

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
[ ] Burn marks
[ ] Broken components
[ ] Bent pins
[ ] Corrosion
[ ] Damaged socket
[ ] Damaged PCIe slot
[ ] Damaged RAM slot
[ ] Missing components
[ ] Swollen/damaged capacitors
[ ] Liquid damage
```

## 🇬🇧 English

Inspect for:

- Burn marks.
- Broken components.
- Bent pins.
- Corrosion.
- Damaged CPU socket.
- Damaged PCIe slots.
- Damaged DIMM slots.
- Missing components.
- Capacitor damage.
- Liquid damage.

---

# 4. POST Test

## 🇻🇳 Tiếng Việt

Quy trình:

```text
1. Install CPU
2. Install CPU cooler
3. Install one RAM module
4. Connect PSU
5. Connect display
6. Power on
7. Observe POST
```

Theo dõi:

```text
Debug LED
POST Code
Beep
Display
Automatic reboot
Shutdown
```

## 🇬🇧 English

POST test procedure:

```text
1. Install CPU
2. Install CPU cooler
3. Install one RAM module
4. Connect PSU
5. Connect display
6. Power on
7. Observe POST
```

Observe:

- Debug LEDs.
- POST codes.
- Beep codes.
- Display output.
- Reboot behavior.
- Shutdown behavior.

---

# 5. RAM Testing

## 🇻🇳 Tiếng Việt

Kiểm tra từng module:

```text
DIMM A1
DIMM A2
DIMM B1
DIMM B2
```

Không áp dụng thứ tự này cho mọi mainboard; luôn kiểm tra manual.

Test:

```text
1 RAM
→ POST

2 RAM
→ POST

Enable XMP/EXPO
→ Stability test
```

## 🇬🇧 English

Test memory modules individually and according to the motherboard manual.

Check:

- Detection.
- Capacity.
- Frequency.
- Dual-channel operation.
- XMP/EXPO behavior.
- Stability.

---

# 6. CPU Testing

## 🇻🇳 Tiếng Việt

Kiểm tra:

- CPU được BIOS nhận.
- Model CPU chính xác.
- Core count.
- Thread count.
- Frequency.
- Temperature.
- CPU voltage.
- Stability.

Có thể sử dụng:

```text
CPU-Z
HWiNFO
Task Manager
BIOS Hardware Monitor
Stress-testing software
```

## 🇬🇧 English

Verify:

- CPU model.
- Core count.
- Thread count.
- Frequency.
- Temperature.
- Voltage.
- Stability.

---

# 7. Storage Testing

## 🇻🇳 Tiếng Việt

### SATA

Kiểm tra:

```text
SATA data cable
SATA power
BIOS detection
Windows detection
Read/write operation
```

### M.2

Kiểm tra:

```text
M.2 installation
M.2 key
NVMe/SATA protocol
BIOS detection
PCIe link
Temperature
```

## 🇬🇧 English

For SATA:

- Data cable.
- Power.
- BIOS detection.
- OS detection.
- Read/write operation.

For M.2:

- Installation.
- Protocol.
- PCIe link.
- BIOS detection.
- Temperature.

---

# 8. USB Testing

## 🇻🇳 Tiếng Việt

Test từng nhóm:

```text
Rear USB
Front USB
USB 2.0
USB 3.x
USB-C
```

Thiết bị test:

```text
Keyboard
Mouse
USB Flash Drive
External SSD
USB-C device
```

## 🇬🇧 English

Test:

- Rear USB.
- Front USB.
- USB 2.0.
- USB 3.x.
- USB-C.

Use:

- Keyboard.
- Mouse.
- Flash drive.
- External SSD.
- USB-C devices.

---

# 9. Ethernet Testing

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
RJ-45
Link LED
NIC detection
Driver
IP address
DHCP
Ping
Internet
```

Ví dụ:

```cmd
ipconfig
ping 127.0.0.1
ping <gateway>
ping 8.8.8.8
```

## 🇬🇧 English

Verify:

- Physical link.
- NIC detection.
- Driver.
- IP configuration.
- DHCP.
- Gateway connectivity.
- Internet connectivity.

---

# 10. Audio Testing

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
Audio driver
Speaker output
Headphone output
Microphone input
Front audio
Rear audio
```

## 🇬🇧 English

Test:

- Audio driver.
- Speaker output.
- Headphone output.
- Microphone input.
- Front audio.
- Rear audio.

---

# 11. PCIe Testing

## 🇻🇳 Tiếng Việt

Kiểm tra:

- GPU.
- Network card.
- Sound card.
- Capture card.
- PCIe storage.

Kiểm tra:

```text
Device detection
PCIe generation
Link width
Driver
Stability
```

## 🇬🇧 English

Test:

- GPU.
- Network adapter.
- Sound card.
- Capture card.
- PCIe storage.

Verify:

- Device detection.
- Link generation.
- Link width.
- Driver.
- Stability.

---

# 12. BIOS Testing

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
CPU detected
RAM detected
Storage detected
Fan detected
Temperature
Boot device
BIOS version
UEFI mode
```

## 🇬🇧 English

Verify:

- CPU detection.
- Memory detection.
- Storage detection.
- Fan detection.
- Temperature.
- Boot device.
- Firmware version.
- UEFI mode.

---

# 13. Stability Testing

## 🇻🇳 Tiếng Việt

Sau khi POST thành công:

```text
Idle Test
CPU Test
Memory Test
Storage Test
GPU Test
Network Test
Full System Test
```

Theo dõi:

```text
Temperature
Voltage
Clock
Errors
Crash
Freeze
Restart
BSOD
```

## 🇬🇧 English

After successful POST, perform:

- Idle testing.
- CPU testing.
- Memory testing.
- Storage testing.
- GPU testing.
- Network testing.
- Full-system testing.

Monitor:

- Temperature.
- Voltage.
- Clock speed.
- Errors.
- Crashes.
- Freezes.
- Restarts.
- BSOD.

---

# 14. Mainboard Testing Checklist

```text
[ ] Visual Inspection
[ ] CPU Detection
[ ] RAM Detection
[ ] POST
[ ] BIOS
[ ] Display
[ ] USB
[ ] SATA
[ ] M.2
[ ] PCIe
[ ] Ethernet
[ ] Audio
[ ] Fan Headers
[ ] Front Panel
[ ] Temperature
[ ] Stability
```

---

# 15. Test Record

```markdown
# Mainboard Test Record

## Hardware

- Manufacturer:
- Model:
- Revision:
- BIOS:

## CPU

- Model:
- Result:

## RAM

- Module:
- Capacity:
- Result:

## GPU

- Model:
- Result:

## Storage

- SATA:
- M.2:
- Result:

## I/O

- USB:
- Ethernet:
- Audio:
- Display:

## Stability

- CPU:
- RAM:
- GPU:
- Storage:

## Result

- PASS / FAIL

## Notes

-
```
