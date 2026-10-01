# PSU Overview

## 🇻🇳 Tiếng Việt

## 1. PSU là gì?

**PSU (Power Supply Unit)** là bộ nguồn cung cấp điện cho máy tính.

Nguồn điện từ ổ điện là **AC (Alternating Current)**, trong khi phần lớn linh kiện máy tính sử dụng **DC (Direct Current)**.

PSU có nhiệm vụ:

```text
AC Input
   ↓
Power Conversion
   ↓
DC Output
   ↓
Computer Components
```

---

## 2. Chức năng chính của PSU

### 2.1 AC to DC Conversion

Chuyển đổi điện AC thành DC.

### 2.2 Voltage Regulation

Duy trì điện áp đầu ra trong phạm vi cho phép.

### 2.3 Power Distribution

Phân phối điện đến:

- Motherboard
- CPU
- GPU
- Storage
- Fans
- Accessories

### 2.4 Protection

PSU hiện đại thường tích hợp nhiều cơ chế bảo vệ.

Các cơ chế thường gặp:

- OVP – Over Voltage Protection
- UVP – Under Voltage Protection
- OCP – Over Current Protection
- OPP – Over Power Protection
- SCP – Short Circuit Protection
- OTP – Over Temperature Protection

Tên và cách triển khai cụ thể phụ thuộc từng PSU.

---

# 3. PSU Components

Một PSU điển hình có thể bao gồm:

- AC input
- EMI filter
- Rectifier
- PFC circuit
- Switching circuit
- Transformer
- Secondary rectification
- DC filtering
- Voltage regulation
- Protection circuit
- Cooling fan
- Control circuitry

### Important

Đây là các phần bên trong PSU và không nên tự tháo PSU nếu không có kiến thức điện tử công suất.

---

# 4. Input Side

PSU nhận nguồn AC từ:

- Wall outlet
- Power strip
- UPS
- Surge protector

Các PSU desktop thường được thiết kế để hoạt động trong một phạm vi điện áp AC nhất định theo thông số của nhà sản xuất.

---

# 5. Output Rails

### +12V

Rail quan trọng nhất trong PC hiện đại.

Thường cung cấp điện cho:

- CPU VRM input
- GPU
- Motors
- Fans
- Một số motherboard circuits

### +5V

Được sử dụng bởi một số mạch và thiết bị SATA/peripheral.

### +3.3V

Có thể được sử dụng bởi:

- Motherboard
- PCIe-related circuits
- Storage electronics
- Các thiết bị logic khác

### +5VSB

**5V Standby**.

Rail này có thể tồn tại khi PC đang tắt nhưng PSU vẫn được kết nối với AC.

Nó hỗ trợ các chức năng standby của hệ thống.

---

# 6. Voltage Regulation

PSU phải giữ điện áp trong giới hạn cho phép.

Theo ATX 3.0 của Intel:

| Rail | Nominal | Range |
|---|---:|---:|
| +12V | 12.00V | 11.20–12.60V |
| +5V | 5.00V | 4.75–5.25V |
| +3.3V | 3.30V | 3.14–3.47V |
| -12V | -12.00V | -10.80–-13.20V |
| +5VSB | 5.00V | 4.75–5.25V |

Các giới hạn này là yêu cầu thiết kế/điều chỉnh theo tài liệu ATX và cần được hiểu trong đúng điều kiện kiểm thử, không nên dùng một phép đo đơn lẻ để kết luận toàn bộ chất lượng PSU.

---

# 7. PSU Form Factor

## ATX

Phổ biến trong desktop tower.

## SFX

Nhỏ hơn ATX.

Thường dùng trong:

- Mini-ITX
- Small Form Factor PC

## SFX-L

Dài hơn SFX.

## TFX

Dùng trong một số hệ thống OEM nhỏ.

## Flex ATX

Dùng trong các case rất nhỏ.

---

# 8. Modular PSU

### Non-Modular

Cable cố định.

### Semi-Modular

Một số cable cố định.

### Fully Modular

Cable có thể tháo rời.

---

# 9. PSU Efficiency

Efficiency cho biết PSU chuyển đổi bao nhiêu phần năng lượng đầu vào thành năng lượng hữu ích ở đầu ra.

Công thức:

```text
Efficiency (%) =
DC Output Power / AC Input Power × 100
```

Ví dụ:

```text
DC Output = 500W
AC Input = 625W

Efficiency = 500 / 625 × 100
           = 80%
```

Phần còn lại chủ yếu biến thành nhiệt và các tổn hao khác.

---

# 10. PSU Quality

Không nên đánh giá PSU chỉ bằng Watt.

Các yếu tố cần xem xét:

- Platform
- Component quality
- Voltage regulation
- Ripple/noise
- Protections
- Efficiency
- Thermal design
- Fan quality
- Warranty
- Connector design
- Manufacturer specifications

---

# 11. PSU Labels

Thông tin trên nhãn PSU thường bao gồm:

- Brand
- Model
- AC input
- DC output
- +3.3V
- +5V
- +12V
- -12V
- +5VSB
- Maximum current
- Total wattage
- Certification information

---

# 12. Single-Rail vs Multi-Rail

### Single-Rail

Một rail +12V chính có thể cung cấp dòng lớn.

### Multi-Rail

+12V được chia thành nhiều giới hạn dòng/protection zones.

Không nên kết luận chất lượng PSU chỉ dựa vào single-rail hay multi-rail.

---

# 13. PSU and PC Stability

PSU có vấn đề có thể dẫn đến:

```text
PSU instability
      ↓
Voltage / Power problems
      ↓
System instability
      ↓
Random reboot / shutdown / crashes
```

Tuy nhiên, các triệu chứng này cũng có thể xuất phát từ:

- RAM
- CPU
- GPU
- Motherboard
- Overheating
- Driver
- Windows
- Storage
- BIOS
- Cable connection

Do đó cần troubleshooting theo quy trình.

---

## 🇬🇧 English

# PSU Overview

## 1. What Is a PSU?

A **Power Supply Unit (PSU)** provides electrical power to a computer.

Wall power is supplied as **AC**, while computer components primarily operate from regulated **DC** power.

Basic process:

```text
AC Input
   ↓
Power Conversion
   ↓
DC Output
   ↓
Computer Components
```

---

## 2. Main PSU Functions

### AC-to-DC Conversion

Converts AC input into DC output.

### Voltage Regulation

Maintains output voltage within specified limits.

### Power Distribution

Distributes power to:

- Motherboard
- CPU
- GPU
- Storage
- Fans
- Accessories

### Protection

Typical PSU protection functions include:

- OVP – Over Voltage Protection
- UVP – Under Voltage Protection
- OCP – Over Current Protection
- OPP – Over Power Protection
- SCP – Short Circuit Protection
- OTP – Over Temperature Protection

Implementation varies between PSU models.

---

## 3. Internal PSU Sections

A typical PSU may contain:

- AC input
- EMI filter
- Rectifier
- PFC circuit
- Switching stage
- Transformer
- Secondary rectification
- DC filtering
- Regulation circuitry
- Protection circuitry
- Cooling fan
- Control circuitry

Internal PSU repair should only be performed by appropriately trained personnel.

---

## 4. Output Rails

### +12V

The most important rail in modern PCs.

Common loads include:

- CPU VRM input
- GPU
- Motors
- Fans
- Motherboard circuits

### +5V

Used by various motherboard and peripheral circuits.

### +3.3V

Used by:

- Motherboard
- Storage electronics
- Logic circuits
- Other low-voltage electronics

### +5VSB

The **5V Standby** rail.

It may remain available while the computer is shut down but the PSU is still connected to AC power.

---

## 5. Voltage Regulation

Typical ATX nominal voltages are:

| Rail | Nominal | Example ATX 3.0 Range |
|---|---:|---:|
| +12V | 12.00V | 11.20–12.60V |
| +5V | 5.00V | 4.75–5.25V |
| +3.3V | 3.30V | 3.14–3.47V |
| -12V | -12.00V | -10.80–-13.20V |
| +5VSB | 5.00V | 4.75–5.25V |

These values come from Intel's ATX 3.0 design documentation.

---

## 6. PSU Form Factors

Common PSU form factors:

- ATX
- SFX
- SFX-L
- TFX
- Flex ATX

---

## 7. Modular Design

### Non-Modular

All cables are permanently attached.

### Semi-Modular

Some cables are permanently attached while others are removable.

### Fully Modular

Most or all PSU cables are removable.

---

## 8. PSU Efficiency

Efficiency indicates how effectively the PSU converts AC input power into DC output power.

Formula:

```text
Efficiency (%) =
DC Output Power / AC Input Power × 100
```

Example:

```text
DC Output = 500W
AC Input = 625W

Efficiency = 80%
```

---

## 9. PSU Quality Factors

PSU quality should not be judged by wattage alone.

Consider:

- PSU platform
- Component quality
- Voltage regulation
- Ripple/noise
- Protection circuits
- Efficiency
- Thermal design
- Fan quality
- Warranty
- Connector design
- Manufacturer specifications

---

## 10. PSU Label

A PSU label commonly includes:

- Brand
- Model
- AC input
- DC outputs
- Voltage rails
- Maximum current
- Total wattage
- Certification information

---

## 11. Single-Rail vs Multi-Rail

### Single-Rail

A major +12V output rail provides a large current capacity.

### Multi-Rail

The +12V output is divided into multiple current/protection zones.

Neither architecture alone determines PSU quality.

---

## 12. PSU and System Stability

A PSU problem may cause:

```text
PSU problem
    ↓
Power instability
    ↓
System instability
    ↓
Shutdown / reboot / crashes
```

However, similar symptoms can also come from:

- RAM
- CPU
- GPU
- Motherboard
- Overheating
- Drivers
- Windows
- Storage
- BIOS
- Loose cables

Proper troubleshooting is therefore required.
