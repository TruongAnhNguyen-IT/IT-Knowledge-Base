# PC Inspection

> **Tiếng Việt:** Quy trình kiểm tra máy tính để bàn.  
> **English:** Desktop PC inspection procedure.

---

# 1. Mục đích | Purpose

### 🇻🇳

PC Inspection được sử dụng để xác định:

- Tình trạng ngoại quan.
- Cấu hình thực tế.
- Tình trạng phần cứng.
- Tình trạng Windows.
- Tình trạng storage.
- Nhiệt độ.
- Hiệu năng.
- Độ ổn định.
- Các lỗi hiện tại.

### 🇬🇧

PC inspection is used to determine:

- Physical condition.
- Actual hardware configuration.
- Hardware condition.
- Windows condition.
- Storage health.
- Temperatures.
- Performance.
- Stability.
- Existing issues.

---

# 2. Inspection Workflow

```text
Receive PC
   ↓
Physical Inspection
   ↓
Power-On Test
   ↓
BIOS Inspection
   ↓
Hardware Identification
   ↓
Windows Inspection
   ↓
Driver Inspection
   ↓
Storage Inspection
   ↓
Temperature Test
   ↓
Stability Test
   ↓
Performance Test
   ↓
Final Report
```

---

# 3. Physical Inspection

Kiểm tra:

- Case.
- Side panel.
- Front panel.
- USB ports.
- Audio ports.
- Power button.
- Reset button.
- Expansion slots.
- Screws.
- Fans.
- Dust.
- Rust.
- Physical damage.

Ghi nhận:

```text
Condition:
Good / Fair / Damaged

Damage:
Yes / No

Notes:
...
```

---

# 4. Internal Inspection

Mở case và kiểm tra:

- Motherboard.
- CPU cooler.
- RAM.
- GPU.
- PSU.
- Storage.
- SATA cables.
- Power cables.
- Case fans.
- Dust accumulation.
- Loose components.
- Burn marks.
- Corrosion.

---

# 5. Power-On Inspection

Quan sát:

- Power LED.
- Fan operation.
- POST.
- Display output.
- Beep codes.
- Debug LEDs.
- Unexpected restart.
- Shutdown.
- Abnormal noise.

---

# 6. BIOS/UEFI Inspection

Kiểm tra:

```text
CPU:
Model:
Cores:
Threads:

RAM:
Capacity:
Speed:

Storage:
Drive:
Capacity:

GPU:
Model:

Temperature:
CPU:
System:

BIOS:
Version:
Date:
```

---

# 7. Windows Inspection

Kiểm tra:

- Windows version.
- Windows edition.
- Activation.
- Update status.
- Computer name.
- User accounts.
- Storage capacity.
- Installed applications.

Commands:

```cmd
winver
systeminfo
hostname
```

PowerShell:

```powershell
Get-ComputerInfo
```

---

# 8. Device Manager

Kiểm tra:

```text
Device Manager
│
├── Display adapters
├── Network adapters
├── Sound controllers
├── Disk drives
├── Processors
├── Memory technology devices
└── Universal Serial Bus controllers
```

Đặc biệt chú ý:

- Yellow warning icon.
- Unknown device.
- Disabled device.
- Driver error.

---

# 9. Storage Inspection

Kiểm tra:

- Capacity.
- Partition.
- File system.
- Health.
- Temperature.
- Power-on hours.
- Bad sectors when applicable.
- Read/write performance.

Tools:

- Disk Management.
- CrystalDiskInfo.
- Manufacturer diagnostic tools.

---

# 10. RAM Inspection

Kiểm tra:

- Total capacity.
- Number of modules.
- DDR generation.
- Speed.
- Dual-channel configuration.

Windows:

```cmd
msinfo32
```

PowerShell:

```powershell
Get-CimInstance Win32_PhysicalMemory
```

Memory testing có thể sử dụng:

- Windows Memory Diagnostic.
- MemTest86.

---

# 11. CPU Inspection

Kiểm tra:

- Model.
- Core count.
- Thread count.
- Clock speed.
- Temperature.
- Utilization.
- Throttling.

Tools:

- Task Manager.
- CPU-Z.
- HWiNFO.

---

# 12. GPU Inspection

Kiểm tra:

- GPU model.
- VRAM.
- Driver.
- Temperature.
- Fan.
- Display output.

Windows:

```text
Device Manager
→ Display adapters
```

---

# 13. Network Inspection

Kiểm tra:

- Ethernet.
- Wi-Fi.
- Link speed.
- IP address.
- DNS.
- Gateway.
- Internet connectivity.

Commands:

```cmd
ipconfig /all
ping 8.8.8.8
ping google.com
```

PowerShell:

```powershell
Get-NetAdapter
Get-NetIPConfiguration
```

---

# 14. USB Inspection

Kiểm tra từng port:

- USB-A.
- USB-C.
- Front USB.
- Rear USB.

Test với:

- USB flash drive.
- Keyboard.
- Mouse.
- External HDD/SSD.

---

# 15. Audio Inspection

Kiểm tra:

- Speaker.
- Headphone.
- Microphone.
- Front audio.
- Rear audio.
- Audio driver.

---

# 16. Temperature Inspection

Theo dõi:

- CPU temperature.
- GPU temperature.
- SSD temperature.
- Motherboard temperature.

Quan trọng là đánh giá theo **model phần cứng, tải và môi trường**, không dùng một con số cố định cho mọi PC.

---

# 17. Stability Testing

Kiểm tra:

- Idle stability.
- CPU load.
- GPU load.
- RAM stability.
- Storage stability.

Tools có thể sử dụng:

- OCCT.
- MemTest86.
- HWiNFO.
- CrystalDiskMark.

Không nên stress test quá mức đối với thiết bị đang có dấu hiệu lỗi hoặc nhiệt độ bất thường.

---

# 18. Performance Inspection

Các nhóm kiểm tra:

### CPU

- Multi-core performance.
- Single-core performance.

### RAM

- Memory bandwidth.
- Latency.

### Storage

- Sequential read.
- Sequential write.
- Random performance.

### GPU

- Graphics performance.
- VRAM behavior.

---

# 19. Inspection Report

Mẫu:

```text
PC Inspection Report

PC ID:
Date:
Technician:

CPU:
Motherboard:
RAM:
Storage:
GPU:
PSU:

Windows:
BIOS:

Physical Condition:
Hardware Condition:
Software Condition:

Temperature:
CPU:
GPU:
Storage:

Network:
Audio:
USB:

Problems Found:
1.
2.
3.

Recommended Action:
1.
2.
3.

Final Result:
PASS / NEED REPAIR / RECHECK
```

---

# 20. Final Inspection Checklist

- [ ] Physical inspection completed.
- [ ] Configuration verified.
- [ ] BIOS inspected.
- [ ] Windows inspected.
- [ ] Drivers checked.
- [ ] Storage health checked.
- [ ] RAM checked.
- [ ] CPU checked.
- [ ] GPU checked.
- [ ] Network checked.
- [ ] USB checked.
- [ ] Audio checked.
- [ ] Temperature checked.
- [ ] Stability checked.
- [ ] Report completed.
