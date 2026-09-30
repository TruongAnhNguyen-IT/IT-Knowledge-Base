# Laptop Inspection / Kiểm tra Laptop

## 1. Overview / Tổng quan

**Tiếng Việt**

Laptop Inspection là quá trình kiểm tra toàn diện tình trạng vật lý, phần cứng, phần mềm và chức năng của laptop.

Mục tiêu:

- Xác định tình trạng thiết bị.
- Phát hiện lỗi.
- Đánh giá khả năng sử dụng.
- Ghi nhận linh kiện.
- Kiểm tra trước khi bàn giao.
- Kiểm tra trước khi mua hoặc thu mua.

**English**

Laptop inspection is the process of checking the physical condition, hardware, software, and functionality of a laptop.

Objectives:

- Determine device condition.
- Identify problems.
- Evaluate usability.
- Record hardware components.
- Inspect before delivery.
- Inspect before purchase or procurement.

---

# 2. Inspection Workflow / Quy trình kiểm tra

```text
Receive Device
      ↓
Record Device Information
      ↓
Physical Inspection
      ↓
Power Test
      ↓
Hardware Inspection
      ↓
Display Test
      ↓
Keyboard / Touchpad Test
      ↓
Port Test
      ↓
Network Test
      ↓
Battery Test
      ↓
Storage Test
      ↓
Performance Test
      ↓
Software Test
      ↓
Document Results
      ↓
Final Assessment
```

---

# 3. Device Information / Thông tin thiết bị

Ghi:

```text
Brand:
Model:
Serial Number:
Service Tag:
Asset Tag:
CPU:
RAM:
Storage:
GPU:
Display:
Battery:
OS:
```

**English:**

Record:

```text
Brand
Model
Serial Number
Service Tag
Asset Tag
CPU
RAM
Storage
GPU
Display
Battery
Operating System
```

---

# 4. Physical Inspection / Kiểm tra ngoại quan

Kiểm tra:

- Laptop body
- Screen bezel
- Screen panel
- Keyboard
- Touchpad
- Hinges
- Bottom cover
- Screws
- Rubber feet
- Ports
- Charger

Tìm:

- Scratches
- Cracks
- Dents
- Broken parts
- Missing screws
- Loose hinges
- Bent chassis
- Liquid damage indicators nếu có

---

# 5. Power Test / Kiểm tra nguồn

Kiểm tra:

- Power button
- AC adapter
- Charging
- Battery
- Power LED
- Boot process

Ghi nhận:

```text
Power On: PASS / FAIL
Charging: PASS / FAIL
Battery: PASS / FAIL
Boot: PASS / FAIL
```

---

# 6. Display Inspection / Kiểm tra màn hình

Kiểm tra:

- Power-on display
- Brightness
- Backlight
- Dead pixels
- Stuck pixels
- Flickering
- Lines
- Color issues
- Backlight bleeding
- External display

Test các mức brightness:

- 0%
- 25%
- 50%
- 75%
- 100%

---

# 7. Keyboard Test / Kiểm tra bàn phím

Kiểm tra từng phím.

Bao gồm:

- Letters
- Numbers
- Function keys
- Arrow keys
- Enter
- Space
- Backspace
- Shift
- Ctrl
- Alt
- Windows key
- Touchpad buttons nếu có

Có thể sử dụng keyboard testing website hoặc text editor để kiểm tra.

---

# 8. Touchpad Test / Kiểm tra Touchpad

Kiểm tra:

- Cursor movement
- Left click
- Right click
- Scrolling
- Multi-touch gestures
- Palm rejection nếu hỗ trợ

---

# 9. Webcam Test / Kiểm tra Webcam

Kiểm tra:

- Camera detection
- Image quality
- Focus
- Microphone
- Privacy shutter nếu có

Windows:

```text
Settings
→ Bluetooth & devices
→ Cameras
```

---

# 10. Audio Test / Kiểm tra âm thanh

Kiểm tra:

### Speaker

- Left channel
- Right channel
- Volume
- Distortion

### Microphone

- Input detection
- Recording
- Audio quality

---

# 11. USB Port Test / Kiểm tra USB

Kiểm tra từng cổng:

- USB-A
- USB-C

Test bằng:

- USB flash drive
- Keyboard
- Mouse
- External storage

USB-C cần kiểm tra thêm nếu thiết bị hỗ trợ:

- Data
- Charging
- Display output
- Power Delivery

---

# 12. Network Test / Kiểm tra mạng

## Wi-Fi

Kiểm tra:

- Wi-Fi detection
- Connection
- Signal
- Internet access
- Stability

## Ethernet

Nếu có RJ45:

- Link detection
- DHCP
- Internet
- Speed

## Bluetooth

Kiểm tra:

- Bluetooth detection
- Pairing
- Connection stability

---

# 13. Storage Inspection / Kiểm tra ổ lưu trữ

Kiểm tra:

- Drive detection
- Capacity
- Health
- Temperature
- Read/write performance

Công cụ:

- Windows Disk Management
- CrystalDiskInfo
- CrystalDiskMark

---

# 14. RAM Inspection / Kiểm tra RAM

Kiểm tra:

- Capacity
- Type
- Speed
- Number of modules
- Available memory

Windows:

```text
Task Manager
→ Performance
→ Memory
```

---

# 15. CPU Inspection / Kiểm tra CPU

Kiểm tra:

- Model
- Cores
- Threads
- Clock
- Temperature
- Usage

Tools:

- Task Manager
- HWiNFO
- CPU-Z

---

# 16. GPU Inspection / Kiểm tra GPU

Kiểm tra:

- GPU model
- Driver
- VRAM
- Temperature
- Usage

Windows:

```text
Task Manager
→ Performance
→ GPU
```

---

# 17. Battery Inspection / Kiểm tra pin

Kiểm tra:

- Battery percentage
- Charging
- Battery health
- Battery capacity
- Cycle count nếu có
- Charging/discharging behavior

Windows Battery Report:

```text
powercfg /batteryreport
```

Sau đó mở file battery report được Windows tạo ra.

---

# 18. Operating System Inspection / Kiểm tra hệ điều hành

Kiểm tra:

- Windows edition
- Activation
- Windows Update
- Device Manager
- Drivers
- System uptime
- User accounts
- Disk space

---

# 19. Device Manager Inspection / Kiểm tra Device Manager

Kiểm tra các thiết bị có:

- Yellow warning
- Unknown device
- Missing driver
- Disabled device

Đường dẫn:

```text
Device Manager
```

---

# 20. Performance Test / Kiểm tra hiệu năng

Có thể kiểm tra:

- CPU load
- RAM usage
- Storage performance
- GPU performance
- Temperature
- Fan behavior

Không nên chạy stress test kéo dài trên thiết bị có dấu hiệu phần cứng không ổn định trước khi xác định nguyên nhân.

---

# 21. Inspection Checklist / Checklist

| Category | Test | Result |
|---|---|---|
| Exterior | Body | PASS / FAIL |
| Display | Screen | PASS / FAIL |
| Keyboard | All keys | PASS / FAIL |
| Touchpad | Touch / Click | PASS / FAIL |
| Webcam | Camera | PASS / FAIL |
| Audio | Speaker | PASS / FAIL |
| Audio | Microphone | PASS / FAIL |
| USB | Ports | PASS / FAIL |
| Network | Wi-Fi | PASS / FAIL |
| Network | Bluetooth | PASS / FAIL |
| Storage | Health | PASS / FAIL |
| RAM | Detection | PASS / FAIL |
| CPU | Test | PASS / FAIL |
| GPU | Test | PASS / FAIL |
| Battery | Health | PASS / FAIL |
| Charger | Charging | PASS / FAIL |
| OS | Windows | PASS / FAIL |

---

# 22. Inspection Report / Biên bản kiểm tra

```text
Date:
Technician:
Device:
Brand:
Model:
Serial Number:

CPU:
RAM:
Storage:
GPU:
Display:
Battery:

Physical Condition:

Functional Test:

Problems Found:

Actions Taken:

Final Result:

Technician:
```

**English:**

```text
Date:
Technician:
Device:
Brand:
Model:
Serial Number:

CPU:
RAM:
Storage:
GPU:
Display:
Battery:

Physical Condition:

Functional Test:

Problems Found:

Actions Taken:

Final Result:

Technician:
```
