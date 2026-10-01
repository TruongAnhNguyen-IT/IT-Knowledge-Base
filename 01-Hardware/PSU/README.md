# Power Supply Unit (PSU)

## 🇻🇳 Tiếng Việt

### 1. Giới thiệu

**PSU (Power Supply Unit)** là bộ nguồn của máy tính, có nhiệm vụ chuyển đổi điện năng từ nguồn điện AC thành các mức điện áp DC phù hợp để cung cấp cho các linh kiện như:

- Mainboard
- CPU
- RAM
- GPU / VGA
- SSD
- HDD
- Optical Drive
- Fan
- USB devices
- Các thiết bị ngoại vi khác

PSU là một trong những linh kiện quan trọng nhất của hệ thống vì mọi linh kiện đều phụ thuộc vào nguồn điện ổn định.

---

### 2. Mục tiêu của thư mục

Thư mục `PSU/` dùng để lưu trữ kiến thức về:

- Tổng quan PSU
- Các chuẩn PSU
- Công suất PSU
- Điện áp PSU
- Các đầu connector
- Cách tính công suất
- Cách kiểm tra PSU
- Chẩn đoán lỗi PSU
- Troubleshooting
- Các lỗi thường gặp
- An toàn khi làm việc với PSU

---

### 3. Cấu trúc tài liệu

```text
PSU/
├── PSU-Connectors.md
├── PSU-Overview.md
├── PSU-Testing.md
├── PSU-Troubleshooting.md
├── PSU-Wattage.md
└── README.md
```

---

### 4. Các nội dung chính

| File | Nội dung |
|---|---|
| `PSU-Overview.md` | Tổng quan về PSU |
| `PSU-Connectors.md` | Các loại connector |
| `PSU-Wattage.md` | Công suất và cách tính |
| `PSU-Testing.md` | Kiểm tra và đo PSU |
| `PSU-Troubleshooting.md` | Chẩn đoán và xử lý lỗi |
| `README.md` | Tổng quan thư mục |

---

### 5. PSU thực hiện những nhiệm vụ gì?

PSU thực hiện các nhiệm vụ chính:

1. Nhận điện AC từ nguồn điện.
2. Chuyển đổi AC thành DC.
3. Tạo ra các mức điện áp cần thiết.
4. Cung cấp điện cho mainboard.
5. Cung cấp điện cho CPU.
6. Cung cấp điện cho GPU.
7. Cung cấp điện cho storage.
8. Bảo vệ hệ thống khi xảy ra sự cố điện.

---

### 6. Các mức điện áp phổ biến

Các rail điện áp thường gặp trong hệ thống ATX:

- +12V
- +5V
- +3.3V
- +5VSB
- -12V trên các thiết kế ATX phù hợp

Theo tài liệu ATX 3.0 của Intel, mức +12V danh định là 12V, +5V là 5V và +3.3V là 3.3V; các mức cho phép phụ thuộc từng rail và tiêu chuẩn.

---

### 7. Các connector phổ biến

Các connector PSU thường gặp:

- 24-pin ATX
- 4-pin ATX12V
- 8-pin EPS12V
- 4+4-pin EPS
- 6-pin PCIe
- 8-pin PCIe / 6+2-pin PCIe
- 12V-2x6
- SATA Power
- 4-pin Peripheral / Molex
- Berg / Floppy

Các connector PCIe hiện đại có thể sử dụng 12V-2x6; tài liệu Intel mô tả connector này trong nhóm PCIe auxiliary power connectors.

---

### 8. Các dạng PSU

#### ATX

PSU desktop phổ biến nhất.

#### SFX

PSU kích thước nhỏ dành cho Small Form Factor PC.

#### SFX-L

Phiên bản dài hơn SFX, thường cung cấp không gian lớn hơn cho linh kiện PSU.

#### TFX

Thường xuất hiện trong một số máy tính nhỏ hoặc OEM.

#### Flex ATX

Dùng trong các hệ thống rất nhỏ.

---

### 9. Modular PSU

#### Non-Modular

Tất cả dây cáp được gắn cố định vào PSU.

#### Semi-Modular

Một số dây chính cố định, các dây phụ có thể tháo rời.

#### Fully Modular

Hầu hết hoặc toàn bộ dây DC có thể tháo rời.

---

### 10. Các thông số quan trọng

Khi đánh giá PSU cần quan tâm:

- Total Wattage
- +12V Wattage
- +12V Current
- Efficiency
- PSU Form Factor
- Connector configuration
- Protection features
- ATX specification
- Warranty
- Build quality
- Operating temperature
- Noise level

---

### 11. Các lỗi PSU thường gặp

Một PSU lỗi có thể gây:

- PC không bật
- PC bật rồi tắt
- Random shutdown
- Random restart
- BSOD
- GPU mất nguồn
- Storage mất kết nối
- Quạt PSU không hoạt động
- Coil noise
- Burning smell
- Voltage instability

Không phải mọi lỗi trên đều do PSU. Cần kiểm tra từng thành phần trước khi kết luận.

---

### 12. Quy trình kiểm tra cơ bản

```text
Power Source
     ↓
AC Cable
     ↓
PSU
     ↓
24-pin ATX
     ↓
CPU EPS
     ↓
GPU PCIe
     ↓
SATA / Peripheral
     ↓
System Components
```

---

### 13. Nguyên tắc an toàn

- Không mở PSU nếu không có chuyên môn về điện tử công suất.
- Không chạm vào linh kiện bên trong PSU.
- Rút nguồn AC trước khi tháo PSU.
- Kiểm tra công tắc PSU.
- Kiểm tra điện áp bằng thiết bị đo phù hợp.
- Không dùng dây modular của PSU khác nếu không xác nhận tương thích.
- Không cố cắm connector sai loại.
- Không short các chân một cách tùy tiện.

---

## 🇬🇧 English

# Power Supply Unit (PSU)

### 1. Introduction

A **Power Supply Unit (PSU)** converts AC electrical power from the wall outlet into DC voltages required by computer components.

A PSU supplies power to:

- Motherboard
- CPU
- RAM
- GPU
- SSD
- HDD
- Fans
- USB devices
- Other peripherals

The PSU is a critical component because system stability depends on stable and properly regulated power.

---

### 2. Folder Objectives

The `PSU/` directory documents:

- PSU fundamentals
- PSU standards
- PSU wattage
- Voltage rails
- Power connectors
- Power calculations
- PSU testing
- Troubleshooting
- Common failures
- Safety procedures

---

### 3. Documentation Structure

```text
PSU/
├── PSU-Connectors.md
├── PSU-Overview.md
├── PSU-Testing.md
├── PSU-Troubleshooting.md
├── PSU-Wattage.md
└── README.md
```

---

### 4. Main Topics

| File | Description |
|---|---|
| `PSU-Overview.md` | PSU fundamentals |
| `PSU-Connectors.md` | Power connectors |
| `PSU-Wattage.md` | Power requirements |
| `PSU-Testing.md` | PSU testing procedures |
| `PSU-Troubleshooting.md` | PSU troubleshooting |
| `README.md` | Directory overview |

---

### 5. PSU Responsibilities

A PSU:

1. Receives AC input.
2. Converts AC into DC.
3. Provides required DC voltage rails.
4. Powers the motherboard.
5. Powers the CPU.
6. Powers the GPU.
7. Powers storage devices.
8. Provides protection against electrical faults.

---

### 6. Common Voltage Rails

Common ATX voltage rails include:

- +12V
- +5V
- +3.3V
- +5VSB
- -12V on applicable ATX designs

Intel's ATX design documentation specifies nominal +12V, +5V and +3.3V rails with defined regulation limits.

---

### 7. Common Connectors

Common PSU connectors include:

- 24-pin ATX
- 4-pin ATX12V
- 8-pin EPS12V
- 4+4-pin EPS
- 6-pin PCIe
- 6+2-pin PCIe
- 12V-2x6
- SATA Power
- 4-pin Peripheral / Molex
- Berg / Floppy

Modern PCIe power systems may use the 12V-2x6 connector.

---

### 8. PSU Form Factors

Common form factors:

- ATX
- SFX
- SFX-L
- TFX
- Flex ATX

---

### 9. Modular Types

#### Non-Modular

All cables are permanently attached.

#### Semi-Modular

Some cables are fixed while additional cables are removable.

#### Fully Modular

Most or all DC cables can be detached.

---

### 10. Important PSU Specifications

Important specifications include:

- Total wattage
- +12V output
- +12V current
- Efficiency
- Form factor
- Connector configuration
- Protection features
- ATX specification
- Warranty
- Operating temperature
- Acoustic performance

---

### 11. Common PSU Symptoms

A faulty PSU may cause:

- No power
- Power-on then shutdown
- Random shutdown
- Random reboot
- BSOD
- GPU power loss
- Storage instability
- PSU fan problems
- Electrical noise
- Burning smell
- Voltage instability

These symptoms do not automatically prove that the PSU is defective.

---

### 12. Basic Power Path

```text
Wall Outlet
    ↓
AC Cable
    ↓
PSU
    ↓
24-pin ATX
    ↓
CPU EPS
    ↓
GPU PCIe
    ↓
SATA / Peripheral
    ↓
Computer Components
```

---

### 13. Safety

- Do not open a PSU unless properly trained.
- Do not touch internal PSU components.
- Disconnect AC power before removing the PSU.
- Check the PSU power switch.
- Use appropriate measurement equipment.
- Never mix modular cables from different PSU models unless compatibility is confirmed.
- Never force an incompatible connector.
- Do not randomly short pins.
