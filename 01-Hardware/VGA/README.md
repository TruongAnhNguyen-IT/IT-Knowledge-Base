# VGA – Graphics Card Knowledge Base

> Tài liệu kiến thức về VGA / GPU, bao gồm tổng quan, khả năng tương thích, driver, kiểm tra và xử lý sự cố.
>
> A technical knowledge base covering VGA / GPU fundamentals, compatibility, drivers, testing, and troubleshooting.

---

## 🇻🇳 Tiếng Việt

### 1. Giới thiệu

**VGA (Video Graphics Adapter)** hay **Graphics Card / GPU** là thành phần chịu trách nhiệm xử lý và xuất hình ảnh từ máy tính đến màn hình.

VGA có thể là:

- **Integrated Graphics (iGPU)** – GPU tích hợp trong CPU hoặc SoC.
- **Dedicated Graphics Card (dGPU)** – card đồ họa rời.
- **Discrete GPU** – GPU độc lập được sử dụng trên card đồ họa.

VGA được sử dụng trong:

- Hiển thị hình ảnh.
- Chơi game.
- Đồ họa 2D/3D.
- Thiết kế CAD.
- Video editing.
- Rendering.
- AI / Machine Learning.
- GPGPU / Compute.
- Multi-monitor.
- Một số hệ thống workstation và server.

---

### 2. Mục đích của thư mục

Thư mục này dùng để lưu trữ kiến thức về:

- VGA architecture.
- GPU specifications.
- VRAM.
- GPU interfaces.
- Video outputs.
- VGA compatibility.
- VGA drivers.
- VGA testing.
- VGA troubleshooting.
- GPU temperature.
- GPU stability.
- Display problems.

---

### 3. Cấu trúc tài liệu

```text
VGA/
│
├── README.md
├── VGA-Compatibility.md
├── VGA-Driver.md
├── VGA-Overview.md
├── VGA-Testing.md
└── VGA-Troubleshooting.md
```

---

### 4. Nội dung từng file

| File | Nội dung |
|---|---|
| `VGA-Overview.md` | Kiến thức tổng quan về VGA/GPU |
| `VGA-Compatibility.md` | Kiểm tra VGA có tương thích với hệ thống hay không |
| `VGA-Driver.md` | Driver, cài đặt, cập nhật và xử lý lỗi driver |
| `VGA-Testing.md` | Quy trình kiểm tra VGA |
| `VGA-Troubleshooting.md` | Chẩn đoán và xử lý lỗi VGA |
| `README.md` | Tổng quan thư mục VGA |

---

### 5. Các thành phần cần kiểm tra khi lắp VGA

Khi lắp VGA rời, cần kiểm tra:

- Mainboard.
- PCIe slot.
- CPU.
- PSU.
- PCIe power connector.
- Case clearance.
- Display cable.
- Monitor.
- Driver.
- BIOS/UEFI.
- Operating System.
- Airflow.
- GPU temperature.

---

### 6. Quy trình kiểm tra VGA cơ bản

```text
Physical Inspection
        ↓
Check PCIe Slot
        ↓
Check PSU
        ↓
Check PCIe Power
        ↓
Install VGA
        ↓
Connect Display
        ↓
Boot System
        ↓
Install Driver
        ↓
Check Device Manager
        ↓
Monitor Temperature
        ↓
Run Stability Test
        ↓
Check Performance
```

---

### 7. Checklist nhanh

#### Hardware

- [ ] VGA được lắp đúng PCIe slot.
- [ ] VGA được cố định chắc chắn.
- [ ] PCIe power được cắm đầy đủ.
- [ ] PSU đủ công suất.
- [ ] PSU có đầu cấp nguồn phù hợp.
- [ ] GPU không bị hư hỏng vật lý.
- [ ] Fan GPU hoạt động bình thường.
- [ ] Không có dấu hiệu cháy hoặc oxy hóa.

#### Software

- [ ] Windows nhận VGA.
- [ ] Driver đã được cài.
- [ ] Không có lỗi trong Device Manager.
- [ ] GPU được nhận đúng model.
- [ ] Driver đúng phiên bản.
- [ ] Không xảy ra crash khi tải GPU.

#### Testing

- [ ] Display output OK.
- [ ] VRAM test OK.
- [ ] GPU stress test OK.
- [ ] Temperature OK.
- [ ] Fan OK.
- [ ] Performance ổn định.

---

## 🇬🇧 English

### 1. Introduction

A **VGA (Video Graphics Adapter)** or **Graphics Card / GPU** is a component responsible for processing and outputting visual information from a computer to a display.

Graphics processing can be provided by:

- Integrated Graphics (iGPU).
- Dedicated Graphics Card (dGPU).
- Discrete GPU.

Common use cases include:

- Display output.
- Gaming.
- 2D/3D graphics.
- CAD.
- Video editing.
- Rendering.
- AI / Machine Learning.
- GPGPU / Compute.
- Multi-monitor setups.
- Workstations.

---

### 2. Purpose

This directory documents:

- GPU fundamentals.
- VGA specifications.
- VRAM.
- PCIe interface.
- Video outputs.
- Compatibility.
- Drivers.
- Testing.
- Troubleshooting.
- Temperature monitoring.
- Stability testing.

---

### 3. Basic VGA Validation Workflow

```text
Physical Inspection
        ↓
PCIe Slot Check
        ↓
PSU Check
        ↓
