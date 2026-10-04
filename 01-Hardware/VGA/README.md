# VGA — Graphics Card / GPU

> **Tiếng Việt:** Tài liệu kiến thức về VGA, GPU, khả năng tương thích, driver, kiểm tra và xử lý sự cố.  
> **English:** A knowledge base covering graphics cards, GPUs, compatibility, drivers, testing, and troubleshooting.

---

## 1. Giới thiệu | Introduction

### 🇻🇳 Tiếng Việt

**VGA (Video Graphics Adapter/Card)** là thiết bị phần cứng chịu trách nhiệm xử lý và xuất hình ảnh ra màn hình.

Trong máy tính hiện đại, VGA thường được gọi là **Graphics Card**, **Graphics Processing Unit (GPU)** hoặc **Discrete GPU (dGPU)** khi nói đến card đồ họa rời.

VGA có thể được sử dụng cho:

- Xuất hình ảnh ra màn hình.
- Chơi game.
- Thiết kế đồ họa.
- Chỉnh sửa video.
- Render 3D.
- CAD/3D modeling.
- AI/Machine Learning.
- Tăng tốc các ứng dụng sử dụng GPU.
- Multi-monitor.
- Giải mã và mã hóa video.

### 🇬🇧 English

A **VGA (Video Graphics Adapter/Card)** is a hardware component responsible for processing and outputting visual information to a display.

Modern computers commonly use the terms **Graphics Card**, **Graphics Processing Unit (GPU)**, and **Discrete GPU (dGPU)**.

A graphics card can be used for:

- Display output.
- Gaming.
- Graphic design.
- Video editing.
- 3D rendering.
- CAD/3D modeling.
- AI/Machine Learning.
- GPU-accelerated applications.
- Multi-monitor configurations.
- Video decoding and encoding.

---

# 2. Cấu trúc thư mục | Directory Structure

```text
VGA/
├── README.md
├── VGA-Compatibility.md
├── VGA-Driver.md
├── VGA-Overview.md
├── VGA-Testing.md
└── VGA-Troubleshooting.md
```

---

# 3. Nội dung tài liệu | Documentation

| File | Tiếng Việt | English |
|---|---|---|
| `VGA-Overview.md` | Tổng quan VGA/GPU | VGA/GPU Overview |
| `VGA-Compatibility.md` | Kiểm tra tương thích | VGA Compatibility |
| `VGA-Driver.md` | Driver VGA | VGA Drivers |
| `VGA-Testing.md` | Kiểm tra VGA | VGA Testing |
| `VGA-Troubleshooting.md` | Xử lý sự cố | VGA Troubleshooting |

---

# 4. Kiến thức cần nắm | Key Knowledge

### 🇻🇳 Tiếng Việt

Khi làm việc với VGA cần hiểu:

1. GPU
2. VRAM
3. GPU architecture
4. GPU clock
5. VRAM clock
6. Memory bus
7. Memory bandwidth
8. CUDA / Stream Processors
9. Ray Tracing
10. Tensor Cores
11. Video encoder/decoder
12. PCIe
13. DisplayPort
14. HDMI
15. DVI
16. VGA connector
17. Power connectors
18. PSU requirements
19. Driver
20. Temperature
21. GPU utilization
22. VRAM utilization
23. Benchmark
24. Stress test
25. Artifact
26. Thermal throttling

### 🇬🇧 English

When working with graphics cards, you should understand:

1. GPU
2. VRAM
3. GPU architecture
4. GPU clock
5. VRAM clock
6. Memory bus
7. Memory bandwidth
8. CUDA / Stream Processors
9. Ray Tracing
10. Tensor Cores
11. Video encoder/decoder
12. PCIe
13. DisplayPort
14. HDMI
15. DVI
16. VGA connector
17. Power connectors
18. PSU requirements
19. Drivers
20. Temperature
21. GPU utilization
22. VRAM utilization
23. Benchmarking
24. Stress testing
25. Artifacts
26. Thermal throttling

---

# 5. Quy trình làm việc với VGA | VGA Workflow

```text
Identify GPU
     ↓
Check Compatibility
     ↓
Install Hardware
     ↓
Connect Power / Display
     ↓
Install Driver
     ↓
Verify Device
     ↓
Test Temperature
     ↓
Test Stability
     ↓
Benchmark
     ↓
Document Results
```

### 🇻🇳 Tiếng Việt

Quy trình đề xuất:

1. Xác định model VGA.
2. Kiểm tra khả năng tương thích.
3. Lắp VGA.
4. Kết nối nguồn phụ nếu cần.
5. Kết nối màn hình.
6. Cài driver.
7. Kiểm tra Device Manager.
8. Kiểm tra GPU-Z/HWiNFO.
9. Kiểm tra nhiệt độ.
10. Stress test.
11. Benchmark.
12. Ghi nhận kết quả.

### 🇬🇧 English

Recommended workflow:

1. Identify the GPU model.
2. Check compatibility.
3. Install the graphics card.
4. Connect auxiliary power if required.
5. Connect the display.
6. Install the driver.
7. Verify the device in Device Manager.
8. Check the GPU using GPU-Z/HWiNFO.
9. Check temperatures.
10. Perform a stress test.
11. Run benchmarks.
12. Document the results.

---

# 6. Công cụ thường dùng | Common Tools

| Tool | Purpose |
|---|---|
| Device Manager | Kiểm tra thiết bị / Device detection |
| GPU-Z | GPU information |
| HWiNFO | Hardware monitoring |
| MSI Afterburner | Monitoring / GPU control |
| NVIDIA App | NVIDIA driver management |
| AMD Software: Adrenalin Edition | AMD driver management |
| Intel Graphics Software | Intel graphics management |
| FurMark | GPU stress testing |
| 3DMark | Benchmark |
| Unigine Heaven | GPU benchmark |
| OCCT | Stability testing |
| Windows Event Viewer | Error investigation |

---

# 7. Mục tiêu học tập | Learning Objectives

### 🇻🇳

Sau khi hoàn thành tài liệu này, người học có thể:

- Nhận diện VGA.
- Đọc thông số VGA.
- Kiểm tra VGA có tương thích với mainboard/PSU/case không.
- Cài đặt driver.
- Kiểm tra tình trạng VGA.
- Benchmark VGA.
- Stress test VGA.
- Nhận biết artifact.
- Kiểm tra nhiệt độ.
- Xử lý lỗi không nhận VGA.
- Xử lý lỗi màn hình đen.
- Xử lý lỗi driver.
- Ghi log quá trình kiểm tra.

### 🇬🇧

After completing this documentation, you should be able to:

- Identify graphics cards.
- Read GPU specifications.
- Check GPU compatibility with the motherboard, PSU, and case.
- Install GPU drivers.
- Verify GPU health.
- Benchmark a GPU.
- Stress-test a GPU.
- Identify graphical artifacts.
- Monitor GPU temperature.
- Troubleshoot GPU detection problems.
- Troubleshoot black-screen problems.
- Troubleshoot driver issues.
- Document testing results.

---

# 8. Related Documentation

```text
Hardware
├── PC
├── Laptop
├── CPU
├── RAM
├── SSD-HDD
├── VGA
├── PSU
└── Mainboard
```

VGA có liên quan trực tiếp đến:

- CPU
- Mainboard
- RAM
- PSU
- SSD/HDD
- Monitor
- Windows
- Drivers
```

---

# 2. `VGA-Overview.md`
