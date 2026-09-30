# CPU Temperature / Nhiệt độ CPU

## 1. Overview / Tổng quan

**Tiếng Việt**

CPU temperature là nhiệt độ của bộ xử lý trong quá trình hoạt động.

Nhiệt độ CPU phụ thuộc vào:

- CPU model
- CPU workload
- CPU cooler
- Thermal paste
- Case airflow
- Fan speed
- Ambient temperature
- Power limits

**English**

CPU temperature is the temperature of the processor while it is operating.

It depends on:

- CPU model
- CPU workload
- CPU cooler
- Thermal paste
- Case airflow
- Fan speed
- Ambient temperature
- Power limits

---

# 2. CPU Temperature States / Các trạng thái nhiệt độ

## Idle

CPU đang tải thấp.

Examples:

- Desktop
- Basic background tasks
- Light applications

## Normal Workload

CPU thực hiện các tác vụ thông thường:

- Web browsing
- Microsoft Office
- Software
- Multitasking

## Heavy Workload

CPU hoạt động với tải cao:

- Rendering
- Compilation
- Virtual machines
- CPU stress testing
- Heavy applications

---

# 3. Factors Affecting CPU Temperature / Yếu tố ảnh hưởng

### CPU Workload

CPU usage càng cao thường tạo ra nhiều nhiệt hơn.

### CPU Cooler

Tản nhiệt tốt giúp truyền nhiệt từ CPU ra môi trường.

### Thermal Paste

Keo tản nhiệt giúp cải thiện tiếp xúc nhiệt giữa CPU và cooler.

### Case Airflow

Luồng khí trong case ảnh hưởng trực tiếp đến khả năng thoát nhiệt.

### Ambient Temperature

Nhiệt độ môi trường càng cao thì nhiệt độ CPU thường cũng cao hơn.

### Dust

Bụi có thể làm giảm hiệu quả của heatsink và fan.

---

# 4. CPU Temperature Monitoring / Theo dõi nhiệt độ

Các công cụ thường dùng:

- BIOS/UEFI Hardware Monitor
- Windows Task Manager
- HWiNFO
- HWMonitor
- Core Temp

---

# 5. How to Check CPU Temperature / Cách kiểm tra

### Method 1: BIOS/UEFI

1. Restart computer.
2. Enter BIOS/UEFI.
3. Open Hardware Monitor.
4. Check CPU temperature.

### Method 2: Monitoring Software

Install a trusted hardware monitoring tool.

Check:

- CPU temperature
- CPU usage
- CPU clock
- CPU power
- Fan speed

---

# 6. High CPU Temperature / CPU quá nóng

Possible causes:

- Dust
- Poor airflow
- Fan failure
- Thermal paste problem
- Cooler installation problem
- High CPU workload
- High ambient temperature
- Incorrect BIOS configuration
- Overclocking

---

# 7. Troubleshooting High Temperature / Xử lý nhiệt độ cao

### Step 1 — Check CPU Usage

Open:

```text
Task Manager
→ Processes
→ CPU
```

Find applications using excessive CPU resources.

### Step 2 — Check CPU Fan

Verify:

- Fan spinning
- Fan speed
- Fan connector
- Fan noise

### Step 3 — Clean Dust

Clean:

- CPU heatsink
- CPU fan
- Case fans
- Air filters

### Step 4 — Check Cooler Installation

Ensure the cooler is properly mounted.

### Step 5 — Check Thermal Paste

If necessary, clean and reapply thermal paste.

### Step 6 — Check Case Airflow

Recommended airflow concept:

```text
Cool Air
   ↓
[Front Intake]
       ↓
    CPU / GPU
       ↓
[Rear / Top Exhaust]
   ↓
Hot Air Out
```

---

# 8. Temperature Interpretation / Đánh giá nhiệt độ

Không nên sử dụng một con số cố định cho mọi CPU.

Cần xem:

- CPU model
- Manufacturer specifications
- TjMax / maximum junction temperature
- Workload
- Ambient temperature
- Cooling system

**English**

Do not use one fixed temperature threshold for every CPU.

Always consider:

- CPU model
- Manufacturer specifications
- TjMax / maximum junction temperature
- Workload
- Ambient temperature
- Cooling system

---

# 9. Thermal Throttling / Giảm xung do nhiệt

**Tiếng Việt**

Thermal throttling xảy ra khi CPU giảm xung nhịp để kiểm soát nhiệt độ khi đạt giới hạn nhiệt được thiết kế.

**English**

Thermal throttling occurs when the CPU reduces its operating frequency to control temperature after reaching a thermal limit.

Symptoms may include:

- Lower CPU clock
- Reduced performance
- High temperature
- Performance fluctuation

---

# 10. Prevention / Phòng tránh

- Clean the PC regularly.
- Maintain good airflow.
- Check CPU cooler.
- Monitor CPU temperature.
- Replace thermal paste when necessary.
- Avoid blocking air intake/exhaust.
- Use an appropriate CPU cooler.
