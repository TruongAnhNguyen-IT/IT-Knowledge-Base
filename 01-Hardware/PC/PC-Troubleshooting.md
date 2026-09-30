# PC Troubleshooting

> **Tiếng Việt:** Quy trình chẩn đoán và xử lý sự cố máy tính để bàn.  
> **English:** Desktop PC troubleshooting and diagnostic procedures.

---

# 1. Troubleshooting Principles

### 🇻🇳

Không nên thay linh kiện ngay khi phát hiện lỗi.

Quy trình:

```text
Problem
   ↓
Collect Information
   ↓
Reproduce Problem
   ↓
Identify Possible Causes
   ↓
Test One Variable
   ↓
Confirm Cause
   ↓
Apply Fix
   ↓
Retest
   ↓
Document
```

### 🇬🇧

Do not immediately replace components when a problem occurs.

Recommended process:

```text
Problem
   ↓
Collect Information
   ↓
Reproduce Problem
   ↓
Identify Possible Causes
   ↓
Test One Variable
   ↓
Confirm Cause
   ↓
Apply Fix
   ↓
Retest
   ↓
Document
```

---

# 2. PC Does Not Power On

## Symptoms

- No fan.
- No LED.
- No display.
- No response.

## Possible Causes

- Power cable.
- Power switch.
- PSU.
- 24-pin connector.
- CPU EPS connector.
- Motherboard.
- Short circuit.

## Diagnostic Steps

1. Verify wall power.
2. Verify power cable.
3. Check PSU switch.
4. Check front-panel Power SW.
5. Reseat 24-pin ATX.
6. Reseat CPU EPS.
7. Disconnect unnecessary devices.
8. Test PSU if appropriate.
9. Test motherboard outside case if necessary.

---

# 3. PC Powers On but No Display

## Possible Causes

- RAM.
- GPU.
- Display cable.
- Monitor.
- CPU.
- BIOS.
- Motherboard.

## Steps

```text
Check Monitor
      ↓
Check Cable
      ↓
Check Correct Display Output
      ↓
Reseat RAM
      ↓
Test One RAM Module
      ↓
Check GPU
      ↓
Check Debug LED
      ↓
Clear CMOS if appropriate
```

Nếu CPU có integrated graphics, có thể thử output từ motherboard khi cấu hình hỗ trợ.

---

# 4. No POST

### Symptoms

- System powers on.
- No successful POST.
- No normal boot.

Kiểm tra:

- CPU.
- RAM.
- GPU.
- BIOS compatibility.
- Motherboard.
- PSU.

Debug tools:

- Debug LED.
- POST code display.
- Beep code.

---

# 5. RAM Problems

## Symptoms

- Random restart.
- BSOD.
- No display.
- Memory errors.
- System instability.

## Diagnostic Steps

1. Power off.
2. Reseat RAM.
3. Test one module.
4. Test different DIMM slot.
5. Test another known-good module.
6. Run memory diagnostic.

Tools:

- Windows Memory Diagnostic.
- MemTest86.

---

# 6. Storage Problems

## Symptoms

- Slow boot.
- Disk disappears.
- File corruption.
- Windows cannot boot.
- SMART warning.

## Steps

1. Check BIOS detection.
2. Check cables.
3. Check SATA power.
4. Check SATA data cable.
5. Check M.2 installation.
6. Check drive health.
7. Check Windows Disk Management.
8. Back up important data.
9. Replace drive if confirmed faulty.

---

# 7. Windows Does Not Boot

Possible causes:

- Corrupted boot files.
- Storage failure.
- Incorrect boot order.
- Windows corruption.
- Hardware failure.

Basic workflow:

```text
BIOS Detects Drive?
       ↓
      YES
       ↓
Correct Boot Device?
       ↓
      YES
       ↓
Windows Recovery
       ↓
Startup Repair
       ↓
Advanced Troubleshooting
```

---

# 8. Windows Blue Screen

BSOD can be caused by:

- Driver problems.
- RAM problems.
- Storage problems.
- Hardware instability.
- System corruption.
- Software conflicts.

Collect:

- Stop code.
- Recent changes.
- Driver changes.
- Hardware changes.
- Event logs.
- Minidump when available.

---

# 9. Overheating

## Symptoms

- High temperature.
- Fan running loudly.
- Performance throttling.
- Random shutdown.
- System instability.

Possible causes:

- Dust.
- Poor thermal paste.
- Poor cooler mounting.
- Failed fan.
- Poor airflow.
- High ambient temperature.

Steps:

1. Inspect cooler.
2. Check fan.
3. Clean dust.
4. Check thermal paste.
5. Check case airflow.
6. Monitor temperature under load.
7. Retest.

---

# 10. PC Randomly Restarts

Possible causes:

- PSU.
- RAM.
- CPU overheating.
- GPU.
- Driver.
- Windows.
- Motherboard.

Diagnostic approach:

```text
Check Event Viewer
        ↓
Check Temperature
        ↓
Check RAM
        ↓
Check PSU
        ↓
Check GPU
        ↓
Stress Test
        ↓
Identify Trigger
```

---

# 11. PC Shuts Down During Load

Possible causes:

- PSU protection.
- CPU overheating.
- GPU overheating.
- Power delivery issue.
- Motherboard issue.

Check:

- CPU temperature.
- GPU temperature.
- PSU capacity.
- PSU connectors.
- Fan operation.

---

# 12. Slow PC

Possible causes:

- Insufficient RAM.
- HDD instead of SSD.
- High startup applications.
- Malware.
- Background processes.
- Storage health problems.
- Thermal throttling.

Check:

```text
Task Manager
├── CPU
├── Memory
├── Disk
└── Startup Apps
```

---

# 13. High CPU Usage

Steps:

1. Open Task Manager.
2. Sort by CPU.
3. Identify process.
4. Check whether it is expected.
5. Investigate application.
6. Check Windows services.
7. Check malware if suspicious.
8. Monitor after remediation.

---

# 14. High Disk Usage

Possible causes:

- Windows Update.
- Antivirus scan.
- Background application.
- Low free space.
- Storage problems.

Check:

- Task Manager.
- Resource Monitor.
- Event Viewer.
- Storage health.

---

# 15. Network Problems

## No Internet

Check:

```cmd
ipconfig /all
```

Then:

```cmd
ping <default-gateway>
ping 8.8.8.8
ping google.com
```

Interpretation:

```text
Gateway fails
→ Local network problem

Gateway works
+
8.8.8.8 fails
→ Internet routing problem

8.8.8.8 works
+
Domain fails
→ DNS problem
```

---

# 16. Ethernet Link Problem

Check:

- Cable.
- Switch port.
- NIC status.
- Driver.
- Link speed.
- IP configuration.

PowerShell:

```powershell
Get-NetAdapter
```

---

# 17. USB Problems

Possible causes:

- Damaged USB port.
- Driver issue.
- USB power problem.
- Device failure.

Steps:

1. Test another port.
2. Test another device.
3. Check Device Manager.
4. Reinstall driver if necessary.
5. Test device on another computer.

---

# 18. Audio Problems

Check:

- Output device.
- Volume.
- Driver.
- Audio service.
- Cable.
- Speaker/headphone.

Windows:

```text
Settings
→ System
→ Sound
```

---

# 19. GPU Problems

Symptoms:

- No display.
- Artifacts.
- Driver crash.
- Black screen.
- GPU overheating.

Steps:

1. Check power connectors.
2. Reseat GPU.
3. Check display cable.
4. Test another output.
5. Check driver.
6. Monitor temperature.
7. Test known-good GPU when available.

---

# 20. Troubleshooting Matrix

| Problem | Possible Cause | First Checks |
|---|---|---|
| No Power | PSU / Power | Cable, PSU, Power SW |
| No Display | RAM / GPU | RAM, GPU, cable |
| No POST | CPU / RAM / BIOS | Debug LED, RAM |
| Random Restart | PSU / RAM / Heat | Temperature, RAM |
| Slow PC | Storage / RAM / Software | Task Manager |
| Disk Missing | Cable / Drive | BIOS, cable |
| BSOD | Driver / RAM / Storage | Stop code, logs |
| Overheating | Cooler / Dust | Fan, temperature |
| No Internet | NIC / DNS / Router | `ipconfig`, `ping` |
| USB Failure | Port / Driver / Device | Another port/device |

---

# 21. Troubleshooting Documentation

Mỗi lỗi nên ghi:

```text
Issue ID:

Date:

Device:

User/Customer:

Problem Description:

Symptoms:

Environment:

Recent Changes:

Initial Hypothesis:

Diagnostic Steps:

Test Result:

Root Cause:

Solution:

Retest Result:

Preventive Action:

Technician:
```

---

# 22. Example Troubleshooting Case

## Case: PC không lên hình

### Problem

PC bật nguồn, quạt quay nhưng màn hình không hiển thị.

### Initial Checks

- Monitor working.
- HDMI cable working.
- GPU installed.
- No display.

### Diagnostic

1. Reseat RAM.
2. Test one RAM module.
3. Test another slot.
4. Check debug LED.
5. Reseat GPU.
6. Test integrated graphics if supported.

### Result

RAM was not properly seated.

### Solution

Reseat RAM and perform POST test again.

### Final Result

System successfully booted.

### Lesson Learned

Always start with simple physical checks before replacing hardware.
