# Mainboard Ports

# Cổng kết nối Mainboard / Motherboard Ports

---

## 1. Tổng quan / Overview

### 🇻🇳 Tiếng Việt

Mainboard có nhiều loại cổng và connector dùng để kết nối CPU, RAM, Storage, GPU, thiết bị ngoại vi, quạt, case và các thiết bị mở rộng.

Các kết nối của mainboard có thể chia thành hai nhóm chính:

```text
Mainboard Ports
│
├── External I/O
│   ├── USB
│   ├── HDMI
│   ├── DisplayPort
│   ├── DVI
│   ├── VGA
│   ├── RJ-45 Ethernet
│   ├── Audio
│   ├── PS/2
│   └── Wi-Fi Antenna
│
└── Internal Connectors
    ├── ATX Power
    ├── CPU Power
    ├── SATA
    ├── M.2
    ├── PCIe
    ├── Front Panel
    ├── USB Headers
    ├── Audio Header
    ├── Fan Headers
    ├── RGB/ARGB
    └── Other Headers
```

Chức năng chính của các cổng là cung cấp:

- Kết nối dữ liệu.
- Kết nối nguồn điện.
- Kết nối thiết bị ngoại vi.
- Kết nối thiết bị lưu trữ.
- Kết nối thiết bị mở rộng.
- Kết nối các thành phần trong case.

### 🇬🇧 English

A motherboard contains many ports, connectors, and headers used to connect the CPU, RAM, storage, GPU, peripherals, cooling fans, case components, and expansion devices.

Motherboard connections can generally be divided into two main groups:

```text
Mainboard Ports
│
├── External I/O
│   ├── USB
│   ├── HDMI
│   ├── DisplayPort
│   ├── DVI
│   ├── VGA
│   ├── RJ-45 Ethernet
│   ├── Audio
│   ├── PS/2
│   └── Wi-Fi Antenna
│
└── Internal Connectors
    ├── ATX Power
    ├── CPU Power
    ├── SATA
    ├── M.2
    ├── PCIe
    ├── Front Panel
    ├── USB Headers
    ├── Audio Header
    ├── Fan Headers
    ├── RGB/ARGB
    └── Other Headers
```

The main purposes of motherboard connections are:

- Data connectivity.
- Power connectivity.
- Peripheral connectivity.
- Storage connectivity.
- Expansion device connectivity.
- Internal component connectivity.

---

# 2. Rear I/O Panel
# Cụm cổng I/O phía sau

### 🇻🇳 Tiếng Việt

**Rear I/O Panel** là khu vực các cổng kết nối nằm ở phía sau mainboard.

Một mainboard có thể có:

```text
USB
USB-C
HDMI
DisplayPort
DVI
VGA
RJ-45 Ethernet
Audio
PS/2
Wi-Fi Antenna
```

Không phải mainboard nào cũng có tất cả các cổng trên.

Số lượng và loại cổng phụ thuộc vào:

- Model mainboard.
- Chipset.
- CPU platform.
- Thiết kế của nhà sản xuất.

### 🇬🇧 English

The **Rear I/O Panel** is the area containing the external connectors on the back of the motherboard.

A motherboard may include:

```text
USB
USB-C
HDMI
DisplayPort
DVI
VGA
RJ-45 Ethernet
Audio
PS/2
Wi-Fi Antenna
```

Not every motherboard provides all of these ports.

The number and type of ports depend on:

- Motherboard model.
- Chipset.
- CPU platform.
- Manufacturer design.

---

# 3. USB Type-A
# Cổng USB Type-A

### 🇻🇳 Tiếng Việt

USB Type-A là một trong những loại connector phổ biến nhất trên mainboard desktop.

Có thể dùng để kết nối:

- Keyboard.
- Mouse.
- USB Flash Drive.
- External HDD/SSD.
- Printer.
- Barcode Scanner.
- USB Wi-Fi Adapter.
- USB Bluetooth Adapter.
- Các thiết bị ngoại vi khác.

Các cổng USB có thể khác nhau về:

- Chuẩn USB.
- Tốc độ truyền dữ liệu.
- Khả năng cấp nguồn.
- Chức năng bổ sung.

**Không nên xác định chuẩn USB chỉ dựa vào màu sắc của cổng.**

Cần kiểm tra thông số của nhà sản xuất.

### 🇬🇧 English

USB Type-A is one of the most common connector types found on desktop motherboards.

It can be used to connect:

- Keyboard.
- Mouse.
- USB flash drive.
- External HDD/SSD.
- Printer.
- Barcode scanner.
- USB Wi-Fi adapter.
- USB Bluetooth adapter.
- Other peripherals.

USB ports can differ in:

- USB standard.
- Data transfer speed.
- Power capability.
- Additional functionality.

**USB capability should not be determined only by the port color.**

Always check the manufacturer's specifications.

---

# 4. USB Type-C
# Cổng USB Type-C

### 🇻🇳 Tiếng Việt

USB Type-C là một loại connector có thiết kế nhỏ và có thể cắm đảo chiều.

Tuy nhiên:

> USB-C không đồng nghĩa với một tốc độ hoặc tính năng cụ thể.

Một cổng USB-C có thể hỗ trợ một hoặc nhiều chức năng tùy thiết kế:

- USB data.
- High-speed data.
- Display output.
- Power Delivery.
- Các giao thức khác.

Cần kiểm tra motherboard specification để biết chính xác cổng USB-C hỗ trợ gì.

### 🇬🇧 English

USB Type-C is a compact, reversible connector.

However:

> USB-C does not automatically define a specific speed or feature set.

Depending on the motherboard design, a USB-C port may support:

- USB data.
- High-speed data.
- Display output.
- Power Delivery.
- Other protocols.

The motherboard specifications should be checked to determine the exact capabilities.

---

# 5. HDMI
# Cổng HDMI

### 🇻🇳 Tiếng Việt

HDMI là giao diện kỹ thuật số dùng để truyền:

- Video.
- Audio.

Cổng HDMI trên mainboard thường liên quan đến khả năng xuất hình của CPU/APU.

Ví dụ:

```text
CPU có iGPU
      ↓
Mainboard HDMI
      ↓
Monitor
```

Nếu CPU không có integrated graphics, cổng HDMI trên mainboard có thể không xuất hình.

Khi troubleshooting cần kiểm tra:

- CPU có iGPU không.
- BIOS configuration.
- Cable.
- Monitor input.
- Mainboard specification.

### 🇬🇧 English

HDMI is a digital interface used to transmit:

- Video.
- Audio.

The HDMI port on a motherboard generally depends on the graphics capabilities of the CPU/APU.

Example:

```text
CPU with integrated graphics
          ↓
Motherboard HDMI
          ↓
Monitor
```

If the CPU does not provide integrated graphics, the motherboard HDMI output may not produce an image.

When troubleshooting, check:

- Whether the CPU has integrated graphics.
- BIOS configuration.
- Cable.
- Monitor input.
- Motherboard specifications.

---

# 6. DisplayPort
# Cổng DisplayPort

### 🇻🇳 Tiếng Việt

DisplayPort là giao diện hiển thị kỹ thuật số dùng để kết nối máy tính với màn hình.

Có thể truyền:

- Digital video.
- Digital audio.

Khả năng thực tế phụ thuộc vào:

- CPU/iGPU.
- Mainboard.
- DisplayPort implementation.
- Monitor.

### 🇬🇧 English

DisplayPort is a digital display interface used to connect computers to monitors.

It can carry:

- Digital video.
- Digital audio.

Actual capabilities depend on:

- CPU/iGPU.
- Motherboard.
- DisplayPort implementation.
- Monitor.

---

# 7. DVI
# Cổng DVI

### 🇻🇳 Tiếng Việt

DVI là một giao diện hiển thị được sử dụng trên nhiều hệ thống máy tính trước đây.

Một số loại DVI phổ biến:

```text
DVI-D
DVI-I
DVI-A
```

DVI-D truyền tín hiệu digital.

DVI-I có thể hỗ trợ digital và analog tùy thiết kế.

DVI hiện ít xuất hiện trên các mainboard hiện đại.

### 🇬🇧 English

DVI is a display interface commonly found on older computer systems.

Common DVI types include:

```text
DVI-D
DVI-I
DVI-A
```

DVI-D carries digital signals.

DVI-I can support digital and analog signals depending on the implementation.

DVI is less common on modern motherboards.

---

# 8. VGA
# Cổng VGA

### 🇻🇳 Tiếng Việt

VGA là giao diện video analog.

Có thể được sử dụng để kết nối:

- Monitor.
- Projector.
- Legacy display devices.

VGA thường gặp trên:

- Mainboard cũ.
- Máy tính văn phòng.
- Hệ thống doanh nghiệp.
- Hệ thống cần hỗ trợ thiết bị legacy.

### 🇬🇧 English

VGA is an analog video interface.

It can be used to connect:

- Monitors.
- Projectors.
- Legacy display devices.

VGA is more commonly found on:

- Older motherboards.
- Office computers.
- Business systems.
- Systems requiring legacy display support.

---

# 9. RJ-45 Ethernet
# Cổng mạng RJ-45

### 🇻🇳 Tiếng Việt

RJ-45 Ethernet là cổng mạng có dây.

Dùng để kết nối máy tính với:

- Switch.
- Router.
- Network infrastructure.
- Internet gateway.

Tốc độ có thể khác nhau tùy mainboard và network controller:

```text
100 Mbps
1 Gbps
2.5 Gbps
5 Gbps
10 Gbps
```

Cần kiểm tra:

- Network controller.
- Motherboard specification.
- Cable.
- Switch/router.
- Negotiated link speed.

### 🇬🇧 English

RJ-45 Ethernet is used for wired network connectivity.

It can connect a computer to:

- Switches.
- Routers.
- Network infrastructure.
- Internet gateways.

Supported speeds vary depending on the motherboard and network controller:

```text
100 Mbps
1 Gbps
2.5 Gbps
5 Gbps
10 Gbps
```

Check:

- Network controller.
- Motherboard specifications.
- Ethernet cable.
- Switch/router.
- Negotiated link speed.

---

# 10. Ethernet LEDs
# Đèn LED trên cổng mạng

### 🇻🇳 Tiếng Việt

Một số cổng Ethernet có LED để hiển thị trạng thái:

- Link.
- Activity.
- Speed.

Ý nghĩa màu sắc và trạng thái LED phụ thuộc vào nhà sản xuất.

Khi troubleshooting:

```text
Không có LED
    ↓
Kiểm tra dây mạng
    ↓
Kiểm tra switch/router
    ↓
Kiểm tra NIC
    ↓
Kiểm tra driver
```

### 🇬🇧 English

Some Ethernet ports include LEDs that indicate:

- Link status.
- Network activity.
- Link speed.

LED colors and meanings vary by manufacturer.

During troubleshooting:

```text
No LED
   ↓
Check Ethernet cable
   ↓
Check switch/router
   ↓
Check NIC
   ↓
Check driver
```

---

# 11. Audio Ports
# Cổng Audio

### 🇻🇳 Tiếng Việt

Audio ports thường sử dụng jack 3.5 mm.

Có thể bao gồm:

```text
Line Out
Mic In
Line In
Rear Speaker
Center/Subwoofer
Side Speaker
```

Một số mainboard có hệ thống audio nhiều kênh.

Chức năng từng jack phụ thuộc vào cấu hình của mainboard và driver.

### 🇬🇧 English

Audio ports commonly use 3.5 mm connectors.

They may include:

```text
Line Out
Mic In
Line In
Rear Speaker
Center/Subwoofer
Side Speaker
```

Some motherboards support multi-channel audio.

The function of each jack depends on the motherboard design and audio driver configuration.

---

# 12. PS/2
# Cổng PS/2

### 🇻🇳 Tiếng Việt

PS/2 là giao diện cũ dành cho:

- Keyboard.
- Mouse.

Một số mainboard có:

```text
PS/2 Keyboard
PS/2 Mouse
```

hoặc:

```text
PS/2 Combo
```

PS/2 vẫn có thể hữu ích trong một số trường hợp troubleshooting hoặc hệ thống legacy.

### 🇬🇧 English

PS/2 is an older interface used for:

- Keyboards.
- Mice.

A motherboard may provide:

```text
PS/2 Keyboard
PS/2 Mouse
```

or:

```text
PS/2 Combo
```

PS/2 can still be useful for certain troubleshooting scenarios and legacy systems.

---

# 13. Wi-Fi Antenna Connectors
# Cổng anten Wi-Fi

### 🇻🇳 Tiếng Việt

Mainboard có Wi-Fi tích hợp thường có các connector để gắn anten.

Anten giúp cải thiện khả năng thu phát tín hiệu Wi-Fi.

Khi kiểm tra Wi-Fi:

```text
Antenna
   ↓
Wi-Fi Module
   ↓
Driver
   ↓
Windows
   ↓
Network
```

Cần kiểm tra:

- Antenna đã được gắn chưa.
- Wi-Fi adapter có được nhận không.
- Driver.
- Device Manager.
- Wireless settings.

### 🇬🇧 English

Motherboards with integrated Wi-Fi commonly provide antenna connectors.

The antennas help the wireless adapter transmit and receive radio signals.

A simplified troubleshooting path is:

```text
Antenna
   ↓
Wi-Fi Module
   ↓
Driver
   ↓
Windows
   ↓
Network
```

Check:

- Whether the antennas are connected.
- Whether the Wi-Fi adapter is detected.
- Driver status.
- Device Manager.
- Wireless settings.

---

# 14. SATA Ports
# Cổng SATA

### 🇻🇳 Tiếng Việt

SATA ports nằm trên PCB của mainboard và dùng để kết nối thiết bị lưu trữ SATA.

Có thể kết nối:

- SATA SSD.
- HDD.
- Optical Drive.

Ví dụ:

```text
SATA1
SATA2
SATA3
SATA4
```

Một số SATA ports có thể chia sẻ tài nguyên với M.2.

Cần kiểm tra motherboard manual.

### 🇬🇧 English

SATA ports are located on the motherboard PCB and are used to connect SATA storage devices.

They may connect:

- SATA SSDs.
- HDDs.
- Optical drives.

Example:

```text
SATA1
SATA2
SATA3
SATA4
```

Some SATA ports may share resources with M.2 slots.

Always check the motherboard manual.

---

# 15. M.2 Slots
# Khe M.2

### 🇻🇳 Tiếng Việt

M.2 slots thường được sử dụng cho SSD.

Có thể hỗ trợ:

```text
M.2 SATA
M.2 NVMe
```

tùy theo thiết kế mainboard.

Cần kiểm tra:

- M.2 Key.
- M.2 Size.
- Interface.
- PCIe generation.
- SATA/NVMe support.
- Lane sharing.

Ví dụ kích thước:

```text
2242
2260
2280
```

### 🇬🇧 English

M.2 slots are commonly used for SSDs.

Depending on the motherboard, they may support:

```text
M.2 SATA
M.2 NVMe
```

Check:

- M.2 key.
- M.2 size.
- Interface.
- PCIe generation.
- SATA/NVMe support.
- Lane sharing.

Common M.2 sizes include:

```text
2242
2260
2280
```

---

# 16. PCIe Slots
# Khe PCIe

### 🇻🇳 Tiếng Việt

PCIe slots dùng để kết nối các card mở rộng.

Các thiết bị phổ biến:

- GPU.
- Network Card.
- Sound Card.
- Capture Card.
- Storage Controller.
- Wi-Fi Card.
- Other Expansion Cards.

Các kích thước phổ biến:

```text
PCIe x1
PCIe x4
PCIe x8
PCIe x16
```

### 🇬🇧 English

PCIe slots are used to connect expansion cards.

Common devices include:

- Graphics cards.
- Network cards.
- Sound cards.
- Capture cards.
- Storage controllers.
- Wi-Fi cards.
- Other expansion cards.

Common slot sizes include:

```text
PCIe x1
PCIe x4
PCIe x8
PCIe x16
```

---

# 17. 24-pin ATX Power Connector
# Đầu nguồn 24-pin ATX

### 🇻🇳 Tiếng Việt

24-pin ATX là đầu cấp nguồn chính cho motherboard desktop.

Kết nối:

```text
PSU
 ↓
24-pin ATX
 ↓
Motherboard
```

Khi máy không có nguồn, cần kiểm tra:

- PSU.
- AC power.
- PSU switch.
- 24-pin connector.
- Motherboard socket.
- Short circuit.

### 🇬🇧 English

The 24-pin ATX connector is the primary power connector for a desktop motherboard.

Connection:

```text
PSU
 ↓
24-pin ATX
 ↓
Motherboard
```

When troubleshooting a no-power condition, check:

- PSU.
- AC power.
- PSU switch.
- 24-pin connector.
- Motherboard socket.
- Possible short circuits.

---

# 18. CPU EPS Power Connector
# Đầu nguồn CPU EPS

### 🇻🇳 Tiếng Việt

CPU EPS connector cung cấp nguồn cho CPU power circuitry.

Các dạng có thể gặp:

```text
4-pin
8-pin
4+4-pin
```

Không được nhầm:

```text
CPU EPS
```

với:

```text
PCIe GPU Power
```

Hai connector có thể có hình dạng gần giống nhưng được thiết kế cho mục đích khác nhau.

### 🇬🇧 English

The CPU EPS connector supplies power to the CPU power circuitry.

Common configurations include:

```text
4-pin
8-pin
4+4-pin
```

Do not confuse:

```text
CPU EPS
```

with:

```text
PCIe GPU Power
```

They may look similar but are designed for different purposes.

---

# 19. Front Panel Header
# Header Front Panel

### 🇻🇳 Tiếng Việt

Front Panel Header kết nối các nút và đèn LED trên case với motherboard.

Có thể bao gồm:

```text
Power Switch
Reset Switch
Power LED
HDD LED
```

Ví dụ:

```text
PWR SW
RESET SW
PLED
HDD LED
```

Pin layout thay đổi tùy mainboard.

Cần xem motherboard manual trước khi kết nối.

### 🇬🇧 English

The Front Panel Header connects the computer case switches and LEDs to the motherboard.

It may include:

```text
Power Switch
Reset Switch
Power LED
HDD LED
```

Examples:

```text
PWR SW
RESET SW
PLED
HDD LED
```

Pin layouts vary by motherboard.

Always check the motherboard manual before connecting the cables.

---

# 20. USB 2.0 Internal Header
# Header USB 2.0 bên trong

### 🇻🇳 Tiếng Việt

USB 2.0 internal header dùng để kết nối các thiết bị USB nằm bên trong case hoặc USB front panel.

Có thể sử dụng cho:

- Front USB.
- Internal USB devices.
- Một số thiết bị phụ trợ.

### 🇬🇧 English

The USB 2.0 internal header is used to connect internal USB devices or front-panel USB ports.

It may be used for:

- Front USB ports.
- Internal USB devices.
- Certain auxiliary devices.

---

# 21. USB 3.x Internal Header
# Header USB 3.x bên trong

### 🇻🇳 Tiếng Việt

USB 3.x internal headers thường dùng để kết nối USB phía trước case.

Ví dụ:

```text
Motherboard
     ↓
USB 3.x Header
     ↓
Front USB-A
```

Connector cụ thể phụ thuộc vào chuẩn và thiết kế mainboard.

### 🇬🇧 English

USB 3.x internal headers are commonly used to connect front-panel USB ports.

Example:

```text
Motherboard
     ↓
USB 3.x Header
     ↓
Front USB-A
```

The exact connector depends on the USB standard and motherboard design.

---

# 22. Front USB-C Header
# Header USB-C Front Panel

### 🇻🇳 Tiếng Việt

Một số mainboard có internal header dành cho USB-C phía trước case.

Kết nối:

```text
Case Front USB-C
        ↓
Motherboard USB-C Header
```

Không nên nhầm với USB 2.0 header hoặc USB 3.x header thông thường.

### 🇬🇧 English

Some motherboards provide an internal header for a case's front USB-C port.

Connection:

```text
Case Front USB-C
        ↓
Motherboard USB-C Header
```

It should not be confused with a USB 2.0 header or a standard USB 3.x header.

---

# 23. Front Audio Header
# Header Audio phía trước

### 🇻🇳 Tiếng Việt

Front Audio Header dùng để kết nối jack tai nghe và microphone phía trước case.

Thông thường:

```text
Case
 ↓
HD AUDIO Cable
 ↓
Front Audio Header
 ↓
Motherboard
```

Cần kiểm tra connector đúng vị trí.

### 🇬🇧 English

The Front Audio Header connects the case's front headphone and microphone ports to the motherboard.

Typical connection:

```text
Case
 ↓
HD AUDIO Cable
 ↓
Front Audio Header
 ↓
Motherboard
```

The correct header location should be verified using the motherboard manual.

---

# 24. Fan Headers
# Header quạt

### 🇻🇳 Tiếng Việt

Fan headers được sử dụng để kết nối quạt với mainboard.

Có thể gặp:

```text
CPU_FAN
SYS_FAN
CHA_FAN
AIO_PUMP
```

Chức năng có thể bao gồm:

- Cấp nguồn cho fan.
- Đọc RPM.
- Điều khiển tốc độ fan.

### 🇬🇧 English

Fan headers are used to connect cooling fans to the motherboard.

Common labels include:

```text
CPU_FAN
SYS_FAN
CHA_FAN
AIO_PUMP
```

They may provide:

- Fan power.
- RPM monitoring.
- Fan speed control.

---

# 25. RGB Header
# Header RGB

### 🇻🇳 Tiếng Việt

RGB headers dùng để kết nối các thiết bị chiếu sáng RGB.

Có thể gặp:

```text
RGB
ARGB
```

Hai loại này không nên xem là giống nhau.

Cần xác định chính xác:

- Header type.
- Pin layout.
- Voltage.
- Manufacturer specification.

**Không cắm thiết bị vào header khi chưa xác định đúng loại.**

### 🇬🇧 English

RGB headers are used to connect RGB lighting devices.

Common types include:

```text
RGB
ARGB
```

These should not be treated as interchangeable.

Check:

- Header type.
- Pin layout.
- Voltage.
- Manufacturer specifications.

**Do not connect a device until the correct header type has been identified.**

---

# 26. TPM Header
# Header TPM

### 🇻🇳 Tiếng Việt

TPM header là connector dành cho một số module TPM rời.

Tuy nhiên, nhiều nền tảng hiện đại có thể cung cấp TPM thông qua firmware.

Cần kiểm tra motherboard documentation để biết hệ thống sử dụng:

- Firmware TPM.
- Discrete TPM.
- TPM header.

### 🇬🇧 English

A TPM header is used for certain discrete TPM modules.

However, many modern platforms can provide TPM functionality through firmware.

Check the motherboard documentation to determine whether the system uses:

- Firmware TPM.
- Discrete TPM.
- TPM header.

---

# 27. Clear CMOS Header
# Header Clear CMOS

### 🇻🇳 Tiếng Việt

Clear CMOS header được sử dụng để reset một số thiết lập BIOS/UEFI.

Có thể được sử dụng khi:

- BIOS configuration không ổn định.
- Hệ thống không POST sau khi thay đổi setting.
- Cần khôi phục cấu hình firmware mặc định.

Phương pháp reset phụ thuộc từng motherboard.

**Không được tự ý short các chân khi chưa biết chính xác vị trí và quy trình.**

### 🇬🇧 English

The Clear CMOS header is used to reset certain BIOS/UEFI settings.

It may be useful when:

- BIOS configuration becomes unstable.
- The system fails to POST after changing settings.
- Firmware settings need to be restored to defaults.

The reset procedure varies by motherboard.

**Do not short the pins unless the correct location and procedure are known.**

---

# 28. Diagnostic Features
# Tính năng chẩn đoán

### 🇻🇳 Tiếng Việt

Một số motherboard có các tính năng hỗ trợ troubleshooting:

```text
Debug LED
POST Code
Q-Code
Diagnostic Button
Speaker Header
BIOS Flashback
```

Ví dụ Debug LED có thể hiển thị:

```text
CPU
DRAM
VGA
BOOT
```

Ý nghĩa chính xác phải được kiểm tra trong motherboard manual.

### 🇬🇧 English

Some motherboards provide diagnostic features such as:

```text
Debug LED
POST Code
Q-Code
Diagnostic Button
Speaker Header
BIOS Flashback
```

For example, Debug LEDs may indicate:

```text
CPU
DRAM
VGA
BOOT
```

The exact meaning should always be verified in the motherboard manual.

---

# 29. Port Testing
# Kiểm tra các cổng

### 🇻🇳 Tiếng Việt

Khi kiểm tra một port, nên thực hiện theo quy trình:

```text
Identify Port
     ↓
Check Specification
     ↓
Connect Known-Good Device
     ↓
Check Detection
     ↓
Check Driver
     ↓
Test Function
     ↓
Record Result
```

### 🇬🇧 English

When testing a port, follow a systematic procedure:

```text
Identify Port
     ↓
Check Specification
     ↓
Connect Known-Good Device
     ↓
Check Detection
     ↓
Check Driver
     ↓
Test Function
     ↓
Record Result
```

---

# 30. Port Testing Checklist
# Checklist kiểm tra cổng

| Port / Connector | Kiểm tra / Test | Kết quả / Result |
|---|---|---|
| USB-A | USB device | PASS / FAIL |
| USB-C | Data/device | PASS / FAIL |
| HDMI | Monitor | PASS / FAIL |
| DisplayPort | Monitor | PASS / FAIL |
| DVI | Monitor | PASS / FAIL |
| VGA | Monitor | PASS / FAIL |
| RJ-45 | Ethernet | PASS / FAIL |
| Audio Out | Headphone/Speaker | PASS / FAIL |
| Mic | Microphone | PASS / FAIL |
| PS/2 | Keyboard/Mouse | PASS / FAIL |
| Wi-Fi | Wireless connection | PASS / FAIL |
| SATA | Storage detection | PASS / FAIL |
| M.2 | SSD detection | PASS / FAIL |
| PCIe | Expansion device | PASS / FAIL |
| Front USB | USB device | PASS / FAIL |
| Front Audio | Headset | PASS / FAIL |
| Fan Header | Fan/RPM | PASS / FAIL |
| RGB/ARGB | Lighting | PASS / FAIL |

---

# 31. Port Documentation Template
# Mẫu ghi nhận thông tin cổng

### 🇻🇳 Tiếng Việt

```text
Mainboard:
Model:
Revision:

Tên cổng / Connector:
Vị trí:
Loại connector:
Interface:
Chuẩn hỗ trợ:

Thiết bị kiểm tra:

Driver cần thiết:

BIOS Setting:

Quy trình kiểm tra:

Kết quả:
PASS / FAIL

Hiện tượng:

Nguyên nhân:

Cách xử lý:

Kết quả cuối cùng:

Ghi chú:
```

### 🇬🇧 English

```text
Motherboard:
Model:
Revision:

Port / Connector:
Location:
Connector Type:
Interface:
Supported Standard:

Test Device:

Required Driver:

BIOS Setting:

Test Procedure:

Result:
PASS / FAIL

Observed Symptom:

Possible Cause:

Corrective Action:

Final Result:

Notes:
```

---

# 32. Common Port Troubleshooting
# Xử lý lỗi cổng thường gặp

## USB

### 🇻🇳 Tiếng Việt

```text
Kiểm tra thiết bị
↓
Kiểm tra cable
↓
Thử port khác
↓
Kiểm tra Device Manager
↓
Kiểm tra driver
↓
Kiểm tra BIOS
```

### 🇬🇧 English

```text
Check device
↓
Check cable
↓
Test another port
↓
Check Device Manager
↓
Check driver
↓
Check BIOS
```

---

## Ethernet

### 🇻🇳 Tiếng Việt

```text
Kiểm tra cable
↓
Kiểm tra Link LED
↓
Kiểm tra NIC
↓
Kiểm tra driver
↓
Kiểm tra IP
↓
Ping Gateway
```

### 🇬🇧 English

```text
Check cable
↓
Check Link LED
↓
Check NIC
↓
Check driver
↓
Check IP configuration
↓
Ping gateway
```

---

## Display

### 🇻🇳 Tiếng Việt

```text
Kiểm tra Monitor
↓
Kiểm tra Cable
↓
Kiểm tra Input
↓
Kiểm tra GPU/iGPU
↓
Kiểm tra BIOS
```

### 🇬🇧 English

```text
Check monitor
↓
Check cable
↓
Check input
↓
Check GPU/iGPU
↓
Check BIOS
```

---

## Audio

### 🇻🇳 Tiếng Việt

```text
Kiểm tra Output Device
↓
Kiểm tra Volume
↓
Kiểm tra Driver
↓
Kiểm tra Jack
↓
Thử thiết bị khác
```

### 🇬🇧 English

```text
Check output device
↓
Check volume
↓
Check driver
↓
Check audio jack
↓
Test another device
```

---

# 33. Important Notes
# Lưu ý quan trọng

### 🇻🇳 Tiếng Việt

Không nên xác định chức năng của một cổng chỉ dựa vào:

- Hình dạng.
- Màu sắc.
- Vị trí trên mainboard.

Cần kiểm tra:

1. Motherboard manual.
2. Motherboard specification.
3. Manufacturer documentation.
4. BIOS/UEFI settings nếu cần.
5. Driver và hệ điều hành.

Các model mainboard khác nhau có thể sử dụng cùng một connector nhưng hỗ trợ tính năng khác nhau.

### 🇬🇧 English

Do not determine a port's functionality based only on:

- Physical appearance.
- Color.
- Location on the motherboard.

Always check:

1. Motherboard manual.
2. Motherboard specifications.
3. Manufacturer documentation.
4. BIOS/UEFI settings when applicable.
5. Drivers and operating system configuration.

Different motherboard models may use the same connector while providing different capabilities.

---

# 34. Quick Reference
# Bảng tham khảo nhanh

| Connector / Port | 🇻🇳 Chức năng | 🇬🇧 Function |
|---|---|---|
| USB-A | Thiết bị USB | USB devices |
| USB-C | Data/Display/Power tùy thiết kế | Data/Display/Power depending on design |
| HDMI | Hình ảnh + âm thanh số | Digital video + audio |
| DisplayPort | Hình ảnh + âm thanh số | Digital video + audio |
| DVI | Tín hiệu hình ảnh | Display signal |
| VGA | Hình ảnh analog | Analog video |
| RJ-45 | Mạng Ethernet | Ethernet networking |
| Audio Jack | Âm thanh | Audio |
| PS/2 | Keyboard/Mouse | Keyboard/Mouse |
| Wi-Fi Antenna | Kết nối anten Wi-Fi | Wi-Fi antenna |
| SATA | Storage SATA | SATA storage |
| M.2 | SSD/thiết bị M.2 | M.2 devices |
| PCIe | Card mở rộng | Expansion cards |
| 24-pin ATX | Nguồn mainboard | Main motherboard power |
| CPU EPS | Nguồn CPU | CPU power |
| Front Panel | Nút/LED case | Case switches/LEDs |
| USB Header | USB front/internal | Front/internal USB |
| Audio Header | Audio phía trước | Front audio |
| Fan Header | Quạt | Cooling fans |
| RGB/ARGB | Đèn RGB | RGB lighting |
| TPM Header | Module TPM | TPM module |
| Clear CMOS | Reset cấu hình BIOS | Reset firmware settings |

---

# 35. Final Principle
# Nguyên tắc cuối cùng

### 🇻🇳 Tiếng Việt

Khi làm việc với các cổng trên mainboard:

> **Không chỉ nhận biết hình dạng của cổng; cần hiểu chức năng, chuẩn giao tiếp, giới hạn và khả năng tương thích của nó.**

Đối với công việc IT Support, kỹ thuật viên nên biết:

- Cổng này dùng để làm gì?
- Thiết bị nào có thể kết nối?
- Có cần driver không?
- Có cần BIOS setting không?
- Tốc độ hỗ trợ là bao nhiêu?
- Có giới hạn nào không?
- Nếu không hoạt động thì kiểm tra từ đâu?

### 🇬🇧 English

When working with motherboard ports:

> **Do not only identify the physical connector; understand its function, interface standard, limitations, and compatibility.**

For IT Support and technical work, a technician should understand:

- What is this port used for?
- What devices can be connected?
- Is a driver required?
- Is a BIOS setting required?
- What speed is supported?
- Are there any limitations?
- Where should troubleshooting begin if the port does not work?
