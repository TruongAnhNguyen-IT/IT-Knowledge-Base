# Mainboard Overview
# Tổng quan Mainboard / Motherboard Overview

---

## 1. Mainboard là gì? / What is a Mainboard?

### 🇻🇳 Tiếng Việt

**Mainboard (Bo mạch chủ / Motherboard)** là bảng mạch chính của máy tính. Mainboard có nhiệm vụ kết nối, cung cấp đường truyền dữ liệu và phân phối nguồn điện giữa các thành phần phần cứng như CPU, RAM, GPU, Storage và các thiết bị ngoại vi.

Mainboard là nền tảng quyết định nhiều yếu tố của hệ thống, bao gồm:

- CPU nào có thể sử dụng.
- Loại RAM nào được hỗ trợ.
- Số lượng khe PCIe.
- Số lượng và loại thiết bị lưu trữ.
- Các cổng kết nối.
- Khả năng mở rộng hệ thống.
- Các tính năng BIOS/UEFI.
- Khả năng nâng cấp phần cứng.

### 🇬🇧 English

A **mainboard (motherboard)** is the primary circuit board of a computer. It provides physical connections, data communication paths, and power distribution between hardware components such as the CPU, RAM, GPU, storage devices, and peripherals.

The motherboard determines many aspects of a computer system, including:

- Which CPUs are supported.
- Which memory type is supported.
- The number of PCIe slots.
- The number and type of storage devices.
- Available I/O interfaces.
- System expansion capabilities.
- BIOS/UEFI features.
- Hardware upgrade options.

---

# 2. Mainboard Architecture
# Kiến trúc Mainboard

### 🇻🇳 Tiếng Việt

Kiến trúc tổng quát của một mainboard có thể được mô tả như sau:

```text
                         ┌───────────────┐
                         │      CPU      │
                         └───────┬───────┘
                                 │
                           CPU Socket
                                 │
              ┌──────────────────┼──────────────────┐
              │                  │                  │
             RAM                PCIe              Chipset
              │                  │                  │
        DIMM Slots              GPU          ┌──────┼──────┐
                                             │      │      │
                                            USB   SATA    LAN
```

CPU, RAM, PCIe và chipset giao tiếp với nhau thông qua các đường truyền được thiết kế theo từng nền tảng.

Kiến trúc thực tế sẽ khác nhau tùy theo:

- CPU generation.
- Platform.
- Chipset.
- Mainboard design.

### 🇬🇧 English

A simplified motherboard architecture can be represented as:

```text
                         ┌───────────────┐
                         │      CPU      │
                         └───────┬───────┘
                                 │
                           CPU Socket
                                 │
              ┌──────────────────┼──────────────────┐
              │                  │                  │
             RAM                PCIe              Chipset
              │                  │                  │
        DIMM Slots              GPU          ┌──────┼──────┐
                                             │      │      │
                                            USB   SATA    LAN
```

The CPU, memory, PCIe devices, and chipset communicate through platform-specific interfaces and data paths.

The actual architecture varies depending on:

- CPU generation.
- Platform.
- Chipset.
- Motherboard design.

---

# 3. Mainboard Components
# Các thành phần trên Mainboard

### 🇻🇳 Tiếng Việt

| Thành phần | Chức năng |
|---|---|
| CPU Socket | Kết nối CPU với mainboard |
| Chipset | Cung cấp và quản lý nhiều chức năng I/O |
| DIMM Slots | Khe lắp RAM |
| PCIe Slots | Khe lắp GPU và card mở rộng |
| M.2 Slots | Kết nối SSD M.2 và thiết bị tương thích |
| SATA Ports | Kết nối SATA SSD, HDD và thiết bị SATA |
| VRM | Điều chỉnh và cung cấp điện áp cho CPU |
| BIOS/UEFI | Firmware khởi tạo phần cứng và quá trình boot |
| CMOS/RTC Battery | Duy trì thời gian và một số cấu hình firmware |
| 24-pin ATX | Cấp nguồn chính cho mainboard |
| CPU EPS | Cấp nguồn cho CPU |
| Audio Controller | Xử lý âm thanh |
| LAN Controller | Kết nối mạng Ethernet |
| Fan Headers | Kết nối và điều khiển quạt |
| Internal Headers | Kết nối USB, Audio, Front Panel và các thiết bị khác |

### 🇬🇧 English

| Component | Function |
|---|---|
| CPU Socket | Connects the CPU to the motherboard |
| Chipset | Provides and manages many I/O functions |
| DIMM Slots | Used to install RAM |
| PCIe Slots | Used for GPUs and expansion cards |
| M.2 Slots | Used for M.2 SSDs and supported devices |
| SATA Ports | Connect SATA SSDs, HDDs, and other SATA devices |
| VRM | Regulates and supplies power to the CPU |
| BIOS/UEFI | Firmware responsible for hardware initialization and boot |
| CMOS/RTC Battery | Maintains time and certain firmware settings |
| 24-pin ATX | Main motherboard power connection |
| CPU EPS | Provides power to the CPU |
| Audio Controller | Handles audio processing |
| LAN Controller | Provides Ethernet networking |
| Fan Headers | Connect and control cooling fans |
| Internal Headers | Connect USB, audio, front-panel, and other internal devices |

---

# 4. CPU Socket
# Socket CPU

### 🇻🇳 Tiếng Việt

CPU Socket là vị trí trên mainboard dùng để lắp CPU.

Socket phải tương thích với CPU.

Ví dụ:

```text
CPU:
Intel Core i5-10400

Socket:
LGA1200
```

Tuy nhiên, **cùng socket không có nghĩa là chắc chắn tương thích**.

Cần kiểm tra thêm:

- Chipset.
- BIOS version.
- CPU Support List.
- CPU power requirements.
- VRM capability.
- RAM compatibility.
- Manufacturer support.

### 🇬🇧 English

The CPU socket is the physical interface used to install the CPU on the motherboard.

The socket must be compatible with the processor.

Example:

```text
CPU:
Intel Core i5-10400

Socket:
LGA1200
```

However, **the same socket does not automatically guarantee compatibility**.

The following should also be checked:

- Chipset.
- BIOS version.
- CPU support list.
- CPU power requirements.
- VRM capability.
- RAM compatibility.
- Manufacturer support.

---

# 5. Chipset
# Chipset

### 🇻🇳 Tiếng Việt

Chipset cung cấp và quản lý nhiều chức năng I/O của nền tảng.

Chipset có thể ảnh hưởng đến:

- Số lượng USB.
- SATA.
- PCIe expansion.
- Storage.
- Networking.
- Các tính năng mở rộng.
- Một số tính năng CPU/platform.

Các chipset khác nhau có thể hỗ trợ các tính năng khác nhau.

### 🇬🇧 English

The chipset provides and manages many platform I/O functions.

It may affect:

- USB connectivity.
- SATA.
- PCIe expansion.
- Storage.
- Networking.
- Expansion features.
- Certain CPU/platform features.

Different chipsets can provide different features and capabilities.

---

# 6. DIMM Slots
# Khe RAM

### 🇻🇳 Tiếng Việt

DIMM slots là các khe trên mainboard dùng để lắp RAM.

Các thông tin cần kiểm tra:

```text
Memory Generation
Memory Type
Number of Slots
Maximum Capacity
Supported Speed
ECC / Non-ECC
Memory Channels
```

Ví dụ:

```text
Memory:
DDR4

Slots:
4 × DIMM
```

Không nên xác định RAM tối đa chỉ dựa trên số lượng khe. Cần kiểm tra specification của mainboard.

### 🇬🇧 English

DIMM slots are motherboard slots used to install system memory.

Important specifications include:

```text
Memory Generation
Memory Type
Number of Slots
Maximum Capacity
Supported Speed
ECC / Non-ECC
Memory Channels
```

Example:

```text
Memory:
DDR4

Slots:
4 × DIMM
```

The maximum supported memory capacity should not be determined only by the number of slots. Always check the motherboard specifications.

---

# 7. PCIe Slots
# Khe PCIe

### 🇻🇳 Tiếng Việt

PCIe là giao diện mở rộng tốc độ cao được sử dụng để kết nối nhiều loại thiết bị.

Các kích thước phổ biến:

```text
PCIe x1
PCIe x4
PCIe x8
PCIe x16
```

Thiết bị PCIe có thể bao gồm:

- GPU.
- Network Card.
- Sound Card.
- Capture Card.
- Storage Expansion Card.
- Các card mở rộng khác.

Cần phân biệt:

```text
Physical Slot Size
```

và:

```text
Electrical Lane Configuration
```

Một khe vật lý x16 không nhất thiết luôn hoạt động ở x16 lanes.

### 🇬🇧 English

PCIe is a high-speed expansion interface used to connect various devices.

Common physical slot sizes include:

```text
PCIe x1
PCIe x4
PCIe x8
PCIe x16
```

PCIe devices may include:

- Graphics cards.
- Network cards.
- Sound cards.
- Capture cards.
- Storage expansion cards.
- Other expansion devices.

It is important to distinguish between:

```text
Physical Slot Size
```

and:

```text
Electrical Lane Configuration
```

A physical x16 slot does not necessarily operate with x16 electrical lanes.

---

# 8. M.2 Slots
# Khe M.2

### 🇻🇳 Tiếng Việt

M.2 là một dạng connector/form factor được sử dụng cho nhiều thiết bị.

Trên desktop motherboard, M.2 thường được sử dụng cho:

- NVMe SSD.
- SATA M.2 SSD.
- Một số thiết bị khác tùy thiết kế.

Cần kiểm tra:

```text
M.2 Key
M.2 Size
Interface
SATA / NVMe
PCIe Generation
Supported Devices
Lane Sharing
```

Không phải mọi khe M.2 đều hỗ trợ mọi loại SSD M.2.

### 🇬🇧 English

M.2 is a connector and form factor used for various devices.

On desktop motherboards, M.2 slots are commonly used for:

- NVMe SSDs.
- SATA M.2 SSDs.
- Other supported devices.

The following should be checked:

```text
M.2 Key
M.2 Size
Interface
SATA / NVMe
PCIe Generation
Supported Devices
Lane Sharing
```

Not every M.2 slot supports every type of M.2 SSD.

---

# 9. SATA Ports
# Cổng SATA

### 🇻🇳 Tiếng Việt

SATA ports được sử dụng để kết nối:

- SATA SSD.
- HDD.
- Optical Drive.
- Các thiết bị SATA khác.

Một số motherboard có thể chia sẻ tài nguyên giữa SATA ports và M.2 slots.

Cần kiểm tra motherboard manual để biết chính xác các cổng nào bị ảnh hưởng khi sử dụng một khe M.2 cụ thể.

### 🇬🇧 English

SATA ports are used to connect:

- SATA SSDs.
- HDDs.
- Optical drives.
- Other SATA devices.

Some motherboards may share resources between SATA ports and M.2 slots.

The motherboard manual should be checked to determine which ports are affected when a specific M.2 slot is used.

---

# 10. VRM
# Mạch cấp nguồn

### 🇻🇳 Tiếng Việt

**VRM – Voltage Regulator Module** là hệ thống mạch điều chỉnh điện áp trên mainboard.

VRM có nhiệm vụ chuyển đổi và điều chỉnh nguồn điện phù hợp cho CPU và một số thành phần khác.

VRM có thể bao gồm:

- PWM Controller.
- MOSFET/Power Stage.
- Chokes.
- Capacitors.
- VRM Heatsinks.

VRM có vai trò quan trọng khi CPU hoạt động ở mức tải cao trong thời gian dài.

### 🇬🇧 English

**VRM – Voltage Regulator Module** is the voltage regulation circuitry on the motherboard.

It converts and regulates electrical power for the CPU and certain other components.

A VRM system may include:

- PWM controllers.
- MOSFETs/power stages.
- Chokes.
- Capacitors.
- VRM heatsinks.

VRM design and cooling can be important during sustained high-load operation.

---

# 11. BIOS/UEFI
# Firmware

### 🇻🇳 Tiếng Việt

BIOS/UEFI là firmware của mainboard.

Nó thực hiện:

- Hardware initialization.
- POST.
- Hardware configuration.
- Boot device selection.
- Khởi động bootloader của hệ điều hành.

Các thiết lập phổ biến:

```text
Boot Order
CPU Configuration
Memory Configuration
XMP / EXPO
Secure Boot
TPM
Virtualization
Fan Control
Storage Configuration
Integrated Graphics
```

### 🇬🇧 English

BIOS/UEFI is the motherboard firmware.

It performs:

- Hardware initialization.
- POST.
- Hardware configuration.
- Boot device selection.
- Bootloader initialization.

Common settings include:

```text
Boot Order
CPU Configuration
Memory Configuration
XMP / EXPO
Secure Boot
TPM
Virtualization
Fan Control
Storage Configuration
Integrated Graphics
```

---

# 12. Form Factor
# Kích thước Mainboard

### 🇻🇳 Tiếng Việt

Các form factor phổ biến:

- ATX.
- Micro-ATX.
- Mini-ITX.
- E-ATX và các biến thể khác.

Form factor ảnh hưởng đến:

- Case compatibility.
- Số lượng expansion slots.
- Số lượng DIMM slots.
- Storage configuration.
- Cooling layout.

### 🇬🇧 English

Common motherboard form factors include:

- ATX.
- Micro-ATX.
- Mini-ITX.
- E-ATX and other variants.

The form factor affects:

- Case compatibility.
- Expansion slot availability.
- DIMM slot availability.
- Storage configuration.
- Cooling layout.

---

# 13. Mainboard Specification
# Thông số Mainboard

### 🇻🇳 Tiếng Việt

Khi ghi thông tin một mainboard, nên lưu:

```text
Manufacturer:
Model:
Revision:
Form Factor:

CPU Socket:
Chipset:
Supported CPU:

Memory Type:
Maximum Memory:
DIMM Slots:

PCIe Slots:
M.2 Slots:
SATA Ports:

LAN:
Wi-Fi:
Bluetooth:
Audio:

BIOS/UEFI:

Power Connectors:

Rear I/O:
Internal Headers:
```

### 🇬🇧 English

When documenting a motherboard, record:

```text
Manufacturer:
Model:
Revision:
Form Factor:

CPU Socket:
Chipset:
Supported CPU:

Memory Type:
Maximum Memory:
DIMM Slots:

PCIe Slots:
M.2 Slots:
SATA Ports:

LAN:
Wi-Fi:
Bluetooth:
Audio:

BIOS/UEFI:

Power Connectors:

Rear I/O:
Internal Headers:
```

---

# 14. Safety
# An toàn khi làm việc với Mainboard

### 🇻🇳 Tiếng Việt

Khi làm việc với mainboard:

- Tắt máy hoàn toàn.
- Rút nguồn AC.
- Ngắt PSU.
- Sử dụng biện pháp chống tĩnh điện.
- Không chạm trực tiếp vào chân socket CPU.
- Không làm cong chân socket.
- Không ép linh kiện vào khe.
- Kiểm tra đúng chiều trước khi lắp.
- Không thao tác với connector khi chưa xác định đúng loại.
- Tham khảo manual trước khi thay đổi phần cứng.

### 🇬🇧 English

When working with a motherboard:

- Shut down the computer completely.
- Disconnect AC power.
- Turn off/disconnect the PSU.
- Use appropriate ESD protection.
- Do not touch CPU socket contacts directly.
- Do not bend socket pins.
- Do not force components into slots.
- Verify component orientation before installation.
- Do not connect an unknown connector without identifying it first.
- Consult the motherboard manual before hardware modifications.

---

# 15. Documentation Template
# Mẫu ghi chép Mainboard

### 🇻🇳 Tiếng Việt

```text
Nhà sản xuất:
Model:
Revision:
Serial Number:

Form Factor:
CPU Socket:
Chipset:

CPU hỗ trợ:
BIOS Version:

Loại RAM:
Dung lượng RAM tối đa:
Số khe RAM:

PCIe:
M.2:
SATA:

LAN:
Wi-Fi:
Bluetooth:
Audio:

Power Connectors:

Rear I/O:

Internal Headers:

Tình trạng vật lý:

Ghi chú:
```

### 🇬🇧 English

```text
Manufacturer:
Model:
Revision:
Serial Number:

Form Factor:
CPU Socket:
Chipset:

Supported CPU:
BIOS Version:

Memory Type:
Maximum Memory:
Memory Slots:

PCIe:
M.2:
SATA:

LAN:
Wi-Fi:
Bluetooth:
Audio:

Power Connectors:

Rear I/O:

Internal Headers:

Physical Condition:

Notes:
```
