# PC Overview

> **Tiếng Việt:** Tổng quan về máy tính để bàn và các thành phần chính.  
> **English:** Overview of desktop computers and their main components.

---

# 1. PC là gì? | What is a PC?

### 🇻🇳 Tiếng Việt

PC (Personal Computer) là máy tính cá nhân được sử dụng cho các mục đích như:

- Làm việc văn phòng.
- Học tập.
- Lập trình.
- Thiết kế đồ họa.
- Chơi game.
- Xử lý dữ liệu.
- Chạy máy chủ nhỏ.
- Sử dụng các phần mềm chuyên dụng.

Desktop PC thường có các linh kiện riêng biệt và có khả năng nâng cấp hoặc thay thế từng thành phần.

### 🇬🇧 English

A Personal Computer (PC) is a computer designed for individual use.

Common applications include:

- Office work.
- Education.
- Programming.
- Graphic design.
- Gaming.
- Data processing.
- Small server workloads.
- Specialized applications.

A desktop PC usually consists of separate components that can be upgraded or replaced individually.

---

# 2. PC Architecture | Kiến trúc PC

```text
                ┌───────────────┐
                │      PSU      │
                │ Power Supply  │
                └───────┬───────┘
                        │
                        ▼
┌─────────┐       ┌───────────────┐
│ Storage │──────►│  Motherboard  │
└─────────┘       └───────┬───────┘
                          │
             ┌────────────┼────────────┐
             ▼            ▼            ▼
           CPU           RAM          GPU
             │
             ▼
          Cooler

Motherboard
    │
    ├── USB
    ├── LAN
    ├── Audio
    ├── SATA
    ├── M.2
    ├── PCIe
    └── Display Output
```

---

# 3. Main Components | Thành phần chính

## 3.1 Motherboard

### 🇻🇳

Mainboard là bo mạch chủ kết nối các thành phần của PC.

Nhiệm vụ:

- Kết nối CPU.
- Kết nối RAM.
- Kết nối Storage.
- Kết nối GPU.
- Cung cấp USB.
- Cung cấp Audio.
- Cung cấp LAN.
- Điều khiển nhiều thiết bị ngoại vi.

### 🇬🇧

The motherboard is the main circuit board that connects PC components.

Functions include:

- CPU connection.
- RAM connection.
- Storage connection.
- GPU connection.
- USB connectivity.
- Audio connectivity.
- Network connectivity.
- Peripheral connectivity.

---

## 3.2 CPU

### 🇻🇳

CPU (Central Processing Unit) là bộ xử lý trung tâm.

CPU thực hiện:

- Tính toán.
- Xử lý instruction.
- Điều khiển hoạt động của hệ thống.
- Chạy ứng dụng.
- Xử lý các tác vụ hệ điều hành.

Các thông số thường gặp:

- Model.
- Generation.
- Socket.
- Core.
- Thread.
- Base Clock.
- Boost Clock.
- Cache.
- TDP / Processor Base Power.
- Integrated Graphics.

### 🇬🇧

The CPU (Central Processing Unit) is the main processor of the computer.

Common specifications include:

- Model.
- Generation.
- Socket.
- Cores.
- Threads.
- Base clock.
- Boost clock.
- Cache.
- Power characteristics.
- Integrated graphics.

---

## 3.3 RAM

### 🇻🇳

RAM là bộ nhớ tạm thời được hệ thống sử dụng để lưu dữ liệu đang được xử lý.

Thông số:

- DDR generation.
- Capacity.
- Frequency.
- Timing.
- Voltage.
- Number of modules.
- Channel configuration.

### 🇬🇧

RAM is temporary system memory used to store data currently being processed.

Specifications include:

- DDR generation.
- Capacity.
- Frequency.
- Timings.
- Voltage.
- Number of modules.
- Channel configuration.

---

## 3.4 Storage

Các loại storage phổ biến:

- HDD.
- SATA SSD.
- NVMe SSD.

Thông số:

- Capacity.
- Interface.
- Read speed.
- Write speed.
- Health.
- Power-on hours.
- Temperature.

---

## 3.5 GPU

GPU xử lý đồ họa và các tác vụ tính toán song song.

Có hai loại chính:

- Integrated GPU.
- Dedicated GPU.

Thông số:

- GPU model.
- VRAM.
- Memory type.
- Interface.
- Power consumption.
- Clock speed.
- Cooling system.

---

## 3.6 PSU

PSU cung cấp điện cho các linh kiện.

Các thông số:

- Wattage.
- Efficiency rating.
- ATX standard.
- 12V output.
- Connectors.
- Protection features.

Các đầu nguồn phổ biến:

- 24-pin ATX.
- 8-pin CPU EPS.
- 6/8-pin PCIe.
- SATA Power.
- Molex.

---

## 3.7 CPU Cooler

CPU Cooler giúp tản nhiệt cho CPU.

Các loại:

- Stock cooler.
- Air cooler.
- AIO liquid cooler.
- Custom liquid cooling.

---

## 3.8 Case

Case bảo vệ và bố trí linh kiện.

Cần kiểm tra:

- Form factor.
- Motherboard compatibility.
- GPU clearance.
- CPU cooler clearance.
- PSU support.
- Fan support.
- Airflow.
- Cable management.

---

# 4. PC Form Factors | Kích thước PC

Các form factor phổ biến:

- Full Tower.
- Mid Tower.
- Mini Tower.
- Small Form Factor (SFF).
- Mini-ITX systems.

Compatibility cần xem xét:

```text
Motherboard Size
        ↓
Case Support
        ↓
PSU Size
        ↓
GPU Length
        ↓
CPU Cooler Height
        ↓
Storage / Fan Mounting
```

---

# 5. Hardware Compatibility | Tương thích phần cứng

Trước khi lắp PC cần kiểm tra:

### CPU ↔ Motherboard

- Socket.
- Chipset.
- BIOS support.
- CPU power requirements.

### RAM ↔ Motherboard

- DDR generation.
- Maximum capacity.
- Supported speed.
- DIMM type.

### GPU ↔ Motherboard

- PCIe slot.
- Physical clearance.
- PSU requirements.

### Storage ↔ Motherboard

- SATA ports.
- M.2 slot.
- NVMe support.
- SATA/NVMe compatibility.

### PSU ↔ System

- Total power requirement.
- Required connectors.
- PSU form factor.

---

# 6. BIOS/UEFI

BIOS/UEFI có nhiệm vụ:

- Khởi tạo phần cứng.
- POST.
- Detect hardware.
- Boot operating system.
- Configure hardware settings.

Các thông tin có thể kiểm tra:

- CPU.
- RAM.
- Storage.
- Fan speed.
- Boot device.
- BIOS version.

---

# 7. POST | Power-On Self-Test

Khi bật PC, hệ thống thực hiện POST.

Quá trình cơ bản:

```text
Power On
   ↓
PSU Power
   ↓
Motherboard Initialization
   ↓
CPU Initialization
   ↓
RAM Detection
   ↓
GPU / Display Initialization
   ↓
Storage Detection
   ↓
Boot Device
   ↓
Operating System
```

Nếu POST thất bại, có thể xuất hiện:

- No display.
- Beep code.
- Debug LED.
- System restart.
- System shutdown.

---

# 8. Operating System

Desktop PC thường sử dụng:

- Windows.
- Linux.

Windows cần kiểm tra:

- Activation.
- Drivers.
- Device Manager.
- Windows Update.
- Storage.
- Network.
- Audio.
- Display.

---

# 9. Performance Factors | Yếu tố ảnh hưởng hiệu năng

Hiệu năng PC phụ thuộc vào:

- CPU.
- RAM.
- Storage.
- GPU.
- Cooling.
- Power supply.
- Software.
- Operating system configuration.

Không nên đánh giá hiệu năng chỉ dựa vào một linh kiện.

---

# 10. Basic PC Workflow

```text
Inspect
  ↓
Identify Components
  ↓
Check Compatibility
  ↓
Assemble
  ↓
POST
  ↓
BIOS/UEFI
  ↓
Install OS
  ↓
Install Drivers
  ↓
Test
  ↓
Document
```
