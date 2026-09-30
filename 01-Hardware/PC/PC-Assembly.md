# PC Assembly

> **Tiếng Việt:** Quy trình lắp ráp máy tính để bàn.  
> **English:** Desktop PC assembly procedure.

---

# 1. Mục tiêu | Objective

### 🇻🇳

Mục tiêu của việc lắp ráp PC:

- Lắp đúng linh kiện.
- Đảm bảo compatibility.
- Đảm bảo nguồn điện chính xác.
- Đảm bảo tản nhiệt.
- Đảm bảo airflow.
- Hạn chế lỗi POST.
- Đảm bảo hệ thống hoạt động ổn định.

### 🇬🇧

The objectives of PC assembly are:

- Install components correctly.
- Verify compatibility.
- Ensure proper power connections.
- Ensure adequate cooling.
- Ensure proper airflow.
- Minimize POST failures.
- Ensure system stability.

---

# 2. Required Components | Linh kiện cần chuẩn bị

Một bộ PC cơ bản:

```text
CPU
Motherboard
RAM
CPU Cooler
Storage
PSU
Case
GPU (if required)
Case Fans
Keyboard
Mouse
Monitor
```

---

# 3. Tools | Dụng cụ

- Phillips screwdriver.
- Flat screwdriver when required.
- Anti-static wrist strap.
- Thermal paste.
- Cable ties.
- Cleaning brush.
- Flashlight.

---

# 4. Pre-Assembly Checklist

Trước khi lắp:

- [ ] CPU compatible with motherboard.
- [ ] Motherboard BIOS supports CPU.
- [ ] RAM compatible.
- [ ] Storage compatible.
- [ ] Case supports motherboard size.
- [ ] GPU fits inside case.
- [ ] CPU cooler fits case.
- [ ] PSU provides enough power.
- [ ] Required PSU connectors are available.
- [ ] All components are physically undamaged.

---

# 5. CPU Installation

### 🇻🇳

1. Đặt motherboard trên bề mặt chống tĩnh điện.
2. Mở socket CPU.
3. Kiểm tra dấu tam giác trên CPU.
4. Căn đúng hướng.
5. Đặt CPU nhẹ nhàng vào socket.
6. Khóa retention mechanism.

**Không được:**

- Ấn mạnh CPU.
- Chạm vào chân socket.
- Lắp ngược CPU.

### 🇬🇧

1. Place the motherboard on an ESD-safe surface.
2. Open the CPU socket.
3. Locate the CPU alignment marker.
4. Align the CPU correctly.
5. Place the CPU gently into the socket.
6. Lock the retention mechanism.

**Do not:**

- Force the CPU.
- Touch socket contacts.
- Install the CPU in the wrong orientation.

---

# 6. CPU Cooler Installation

Các bước:

1. Kiểm tra mounting system.
2. Làm sạch CPU nếu cần.
3. Apply thermal paste.
4. Install cooler.
5. Tighten screws evenly.
6. Connect CPU_FAN/AIO_PUMP as required.

Kiểm tra:

- Cooler chắc chắn.
- Không nghiêng.
- Fan quay.
- Cable không chạm fan.

---

# 7. RAM Installation

### 🇻🇳

1. Mở RAM slot.
2. Căn notch.
3. Đặt RAM đúng chiều.
4. Nhấn đều hai đầu.
5. Kiểm tra locking clips.

Nếu sử dụng 2 thanh RAM, cần tham khảo motherboard manual để chọn đúng slot cho dual-channel.

### 🇬🇧

1. Open the DIMM slot.
2. Align the notch.
3. Insert the RAM in the correct orientation.
4. Press evenly until locked.
5. Verify the retention clips.

For two RAM modules, check the motherboard manual for the recommended dual-channel slots.

---

# 8. M.2 SSD Installation

1. Locate M.2 slot.
2. Check supported interface.
3. Insert SSD at an angle.
4. Press SSD down.
5. Secure with screw/latch.
6. Install heatsink if available.

---

# 9. Motherboard Installation

1. Install correct I/O shield if required.
2. Verify motherboard standoffs.
3. Place motherboard inside case.
4. Align rear I/O.
5. Align mounting holes.
6. Secure screws.

**Important:**

Không được để thừa standoff chạm vào mặt dưới motherboard.

---

# 10. PSU Installation

Install PSU according to case design.

Connect:

```text
PSU
│
├── 24-pin ATX → Motherboard
├── 4/8-pin EPS → CPU
├── PCIe / 12VHPWR / required GPU power
├── SATA Power → Storage
└── Other required devices
```

Không ép đầu connector nếu không đúng loại.

---

# 11. GPU Installation

1. Locate primary PCIe x16 slot.
2. Remove required expansion slot covers.
3. Insert GPU vertically.
4. Lock PCIe retention mechanism.
5. Secure GPU to case.
6. Connect GPU power cable if required.

---

# 12. Case Front Panel

Các connector thường gặp:

- Power SW.
- Reset SW.
- Power LED.
- HDD LED.
- HD Audio.
- USB 2.0.
- USB 3.x.
- USB Type-C.

Front-panel pinout phải tham khảo motherboard manual.

---

# 13. Case Fans

Airflow cơ bản:

```text
Front
  ↓
Cool Air
  ↓
Components
  ↓
Hot Air
  ↓
Rear / Top
```

Có thể sử dụng:

- Front intake.
- Bottom intake.
- Rear exhaust.
- Top exhaust.

Mục tiêu là tạo airflow hợp lý và hạn chế cable cản gió.

---

# 14. Cable Management

Nguyên tắc:

- Route cables phía sau motherboard tray.
- Không để dây chạm fan.
- Không bẻ dây quá mạnh.
- Không kéo căng connector.
- Tách dây nguồn và dây data khi cần.
- Sử dụng cable ties.

---

# 15. First Power-On

Trước khi bật:

- [ ] CPU installed.
- [ ] CPU cooler installed.
- [ ] CPU_FAN connected.
- [ ] RAM installed.
- [ ] GPU installed if required.
- [ ] 24-pin connected.
- [ ] CPU EPS connected.
- [ ] GPU power connected.
- [ ] Storage connected.
- [ ] Monitor connected.
- [ ] Keyboard connected.

Sau đó:

```text
Power On
   ↓
Observe POST
   ↓
Check Display
   ↓
Enter BIOS/UEFI
   ↓
Verify Hardware
```

---

# 16. BIOS/UEFI Verification

Kiểm tra:

- CPU model.
- CPU temperature.
- RAM capacity.
- RAM speed.
- Storage device.
- Fan speed.
- Boot device.
- BIOS version.

---

# 17. Operating System Installation

Quy trình:

```text
Create Installation Media
        ↓
Boot from USB
        ↓
Partition Disk
        ↓
Install Windows
        ↓
Install Drivers
        ↓
Windows Update
        ↓
Activate
        ↓
Configure System
```

---

# 18. Post-Assembly Testing

Kiểm tra:

### Hardware

- CPU.
- RAM.
- Storage.
- GPU.
- Network.
- Audio.
- USB.
- Display.

### Software

- Device Manager.
- Windows Update.
- Driver status.
- Activation.

### Stability

- CPU temperature.
- GPU temperature.
- RAM stability.
- Storage health.
- System restart/shutdown.

---

# 19. Assembly Record

Mỗi PC nên ghi lại:

```text
PC ID:
Date:
CPU:
Motherboard:
RAM:
Storage:
GPU:
PSU:
Case:
Cooler:
Operating System:
BIOS Version:
Test Result:
Issues:
Technician:
```

---

# 20. Assembly Completion Checklist

- [ ] Hardware installed.
- [ ] Cable connections verified.
- [ ] POST successful.
- [ ] BIOS detects all components.
- [ ] Windows installed.
- [ ] Drivers installed.
- [ ] No unknown devices.
- [ ] Temperature checked.
- [ ] Storage health checked.
- [ ] Stability test completed.
- [ ] Final inspection completed.
- [ ] Documentation completed.
