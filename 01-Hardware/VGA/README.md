# VGA — Graphics Card

> **Tiếng Việt:** Tài liệu kiến thức và thực hành về VGA / Graphics Card.  
> **English:** A practical knowledge base for VGA / Graphics Cards.

---

# 1. Giới thiệu | Introduction

## 🇻🇳 Tiếng Việt

Thư mục này chứa tài liệu về **VGA (Graphics Card)**, bao gồm kiến thức nền tảng, khả năng tương thích, driver, kiểm tra và xử lý sự cố.

Mục tiêu là xây dựng một tài liệu có thể sử dụng cho:

- Học tập.
- IT Support.
- Hardware Troubleshooting.
- PC Assembly.
- PC Maintenance.
- GPU Testing.
- Hardware Documentation.

## 🇬🇧 English

This directory contains documentation about **VGA / Graphics Cards**, including fundamentals, compatibility, drivers, testing, and troubleshooting.

The purpose is to provide practical documentation for:

- Learning.
- IT Support.
- Hardware Troubleshooting.
- PC Assembly.
- PC Maintenance.
- GPU Testing.
- Hardware Documentation.

---

# 2. Documentation Structure

```text
VGA/
├── VGA-Compatibility.md
├── VGA-Driver.md
├── VGA-Overview.md
├── VGA-Testing.md
├── VGA-Troubleshooting.md
└── README.md
```

---

# 3. Documentation Map

| File | Tiếng Việt | English |
|---|---|---|
| `VGA-Overview.md` | Tổng quan VGA/GPU | VGA/GPU Overview |
| `VGA-Compatibility.md` | Tương thích VGA | VGA Compatibility |
| `VGA-Driver.md` | Driver VGA | VGA Driver |
| `VGA-Testing.md` | Kiểm tra VGA | VGA Testing |
| `VGA-Troubleshooting.md` | Xử lý sự cố VGA | VGA Troubleshooting |

---

# 4. VGA Overview

File:

```text
VGA-Overview.md
```

### 🇻🇳

Tập trung vào kiến thức nền tảng:

- VGA.
- GPU.
- iGPU.
- dGPU.
- VRAM.
- GPU Clock.
- Memory Bus.
- Memory Bandwidth.
- PCIe.
- Display Outputs.
- Power Connectors.
- VRM.
- Cooling.
- Temperature.
- VBIOS.
- Ray Tracing.
- AI acceleration.
- GPU artifacts.

### 🇬🇧

Covers fundamental concepts:

- VGA.
- GPU.
- iGPU.
- dGPU.
- VRAM.
- GPU Clock.
- Memory Bus.
- Memory Bandwidth.
- PCIe.
- Display Outputs.
- Power Connectors.
- VRM.
- Cooling.
- Temperature.
- VBIOS.
- Ray Tracing.
- AI acceleration.
- GPU artifacts.

---

# 5. VGA Compatibility

File:

```text
VGA-Compatibility.md
```

### 🇻🇳

Dùng để xác định VGA có phù hợp với hệ thống hay không.

Kiểm tra:

```text
Motherboard
CPU
PCIe
PSU
Power Connectors
Case
Monitor
Operating System
Driver
```

### 🇬🇧

Used to determine whether a GPU is compatible with a computer system.

Check:

```text
Motherboard
CPU
PCIe
PSU
Power Connectors
Case
Monitor
Operating System
Driver
```

---

# 6. VGA Driver

File:

```text
VGA-Driver.md
```

### 🇻🇳

Bao gồm:

- Driver concept.
- NVIDIA.
- AMD.
- Intel.
- Driver installation.
- Driver update.
- Clean installation.
- DDU.
- Rollback.
- Device Manager.
- Error codes.
- Driver verification.

### 🇬🇧

Includes:

- Driver concepts.
- NVIDIA.
- AMD.
- Intel.
- Driver installation.
- Driver updates.
- Clean installation.
- DDU.
- Rollback.
- Device Manager.
- Error codes.
- Driver verification.

---

# 7. VGA Testing

File:

```text
VGA-Testing.md
```

### 🇻🇳

Quy trình:

```text
Visual Inspection
↓
Installation Check
↓
BIOS/POST
↓
Windows Detection
↓
Driver Verification
↓
GPU-Z
↓
HWiNFO
↓
Idle Test
↓
Load Test
↓
Stress Test
↓
Benchmark
↓
Artifact Test
↓
Display Test
↓
Final Report
```

### 🇬🇧

Testing workflow:

```text
Visual Inspection
↓
Installation Check
↓
BIOS/POST
↓
Windows Detection
↓
Driver Verification
↓
GPU-Z
↓
HWiNFO
↓
Idle Test
↓
Load Test
↓
Stress Test
↓
Benchmark
↓
Artifact Test
↓
Display Test
↓
Final Report
```

---

# 8. VGA Troubleshooting

File:

```text
VGA-Troubleshooting.md
```

### 🇻🇳

Các vấn đề:

- VGA không nhận.
- Không có hình.
- Màn hình đen.
- Driver crash.
- Code 43.
- Artifact.
- Overheating.
- Fan không quay.
- GPU crash.
- Hiệu năng thấp.
- PCIe link bất thường.
- Flickering.
- Random restart.

### 🇬🇧

Common issues:

- GPU not detected.
- No display.
- Black screen.
- Driver crashes.
- Code 43.
- Artifacts.
- Overheating.
- GPU fan not spinning.
- GPU crashes.
- Low performance.
- Abnormal PCIe link.
- Flickering.
- Random restarts.

---

# 9. Recommended Learning Order

## 🇻🇳

Nên học theo thứ tự:

```text
01. VGA-Overview.md
        ↓
02. VGA-Compatibility.md
        ↓
03. VGA-Driver.md
        ↓
04. VGA-Testing.md
        ↓
05. VGA-Troubleshooting.md
```

### 🇬🇧

Recommended learning order:

```text
01. VGA-Overview.md
        ↓
02. VGA-Compatibility.md
        ↓
03. VGA-Driver.md
        ↓
04. VGA-Testing.md
        ↓
05. VGA-Troubleshooting.md
```

---

# 10. Practical Workflow

## 🇻🇳

Khi tiếp nhận một VGA cần kiểm tra:

```text
Receive GPU
↓
Record Model / Serial
↓
Visual Inspection
↓
Check Compatibility
↓
Install GPU
↓
Connect Power
↓
Connect Display
↓
Boot
↓
Install Driver
↓
Verify GPU
↓
Monitor Temperature
↓
Stress Test
↓
Benchmark
↓
Check Display Outputs
↓
Document Result
```

## 🇬🇧

When receiving a GPU for testing:

```text
Receive GPU
↓
Record Model / Serial
↓
Visual Inspection
↓
Check Compatibility
↓
Install GPU
↓
Connect Power
↓
Connect Display
↓
Boot
↓
Install Driver
↓
Verify GPU
↓
Monitor Temperature
↓
Stress Test
↓
Benchmark
↓
Check Display Outputs
↓
Document Result
```

---

# 11. Recommended Tools

| Tool | Purpose |
|---|---|
| Device Manager | GPU detection |
| DirectX Diagnostic Tool | GPU/driver information |
| GPU-Z | GPU specifications |
| HWiNFO | Hardware monitoring |
| MSI Afterburner | GPU monitoring/control |
| FurMark | GPU stress testing |
| OCCT | Stability testing |
| 3DMark | Benchmarking |
| Unigine Heaven | GPU benchmarking |
| Event Viewer | Windows error investigation |

---

# 12. VGA Test Record

```text
GPU:
Brand:
Model:
Serial Number:

GPU Architecture:
VRAM:
Memory Type:
Memory Bus:
PCIe Interface:

Motherboard:
CPU:
RAM:
PSU:
Case:

Operating System:
Driver:

Physical Condition:

BIOS Detection:

Windows Detection:

Temperature:
Idle:
Load:

Fan:

Stress Test:

Benchmark:

Display Outputs:

Artifacts:

Final Result:

[ ] PASS
[ ] FAIL
[ ] NEED FURTHER TESTING

Notes:
```

---

# 13. Knowledge Base Scope

### 🇻🇳

Tài liệu này tập trung vào **VGA/Graphics Card**, không thay thế tài liệu chuyên sâu về:

- CPU.
- RAM.
- PSU.
- Mainboard.
- SSD/HDD.
- Monitor.
- Windows.

Các thành phần trên nên có tài liệu riêng và được liên kết với VGA khi cần.

### 🇬🇧

This documentation focuses on **VGA/Graphics Cards** and does not replace dedicated documentation for:

- CPU.
- RAM.
- PSU.
- Motherboard.
- SSD/HDD.
- Monitor.
- Windows.

These components should have their own documentation and be referenced when relevant.

---

# 14. Related Hardware

```text
01-Hardware/
├── PC/
├── Laptop/
├── CPU/
├── RAM/
├── SSD-HDD/
├── VGA/
├── PSU/
└── Mainboard/
```

VGA có quan hệ trực tiếp với:

```text
CPU
RAM
Mainboard
PSU
Storage
Monitor
Operating System
Driver
```

---

# 15. Documentation Standard

### 🇻🇳

Khi bổ sung tài liệu VGA mới, nên sử dụng cấu trúc:

```text
# Title

> Description

# 1. Introduction

# 2. Concepts

# 3. Specifications

# 4. Procedures

# 5. Troubleshooting

# 6. Checklist

# 7. Documentation / Report
```

### 🇬🇧

When adding new VGA documentation, use a consistent structure:

```text
# Title

> Description

# 1. Introduction

# 2. Concepts

# 3. Specifications

# 4. Procedures

# 5. Troubleshooting

# 6. Checklist

# 7. Documentation / Report
```

---

# 16. Final Objective

## 🇻🇳

Mục tiêu cuối cùng của thư mục VGA là xây dựng khả năng:

> **Hiểu → Nhận diện → Kiểm tra tương thích → Lắp đặt → Cài driver → Test → Chẩn đoán → Xử lý → Ghi nhận kết quả.**

## 🇬🇧

The final objective of this VGA documentation is to develop the ability to:

> **Understand → Identify → Check Compatibility → Install → Install Drivers → Test → Diagnose → Troubleshoot → Document.**
