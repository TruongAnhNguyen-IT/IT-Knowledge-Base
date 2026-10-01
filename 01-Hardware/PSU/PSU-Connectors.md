# PSU Connectors

## 🇻🇳 Tiếng Việt

## 1. Tổng quan

PSU sử dụng nhiều loại connector để cung cấp điện cho các linh kiện.

Các connector quan trọng:

```text
24-pin ATX
4-pin ATX12V
4+4-pin EPS
6-pin PCIe
6+2-pin PCIe
12V-2x6
SATA Power
Molex
Berg
```

---

# 2. 24-Pin ATX Main Power

### Tên

**24-pin ATX Main Power Connector**

### Mục đích

Cấp nguồn chính cho motherboard.

### Kết nối

```text
PSU
 ↓
24-pin ATX
 ↓
Motherboard
```

### Điện áp thường gặp

- +3.3V
- +5V
- +12V
- GND
- +5VSB
- PS_ON#
- PWR_OK

### Lưu ý

Không ép connector nếu không đúng hướng.

Connector có latch để cố định với motherboard.

---

# 3. CPU 4-Pin ATX12V

### Tên

**4-pin ATX12V**

### Mục đích

Cấp nguồn cho CPU VRM trên motherboard.

```text
PSU
 ↓
4-pin CPU
 ↓
Motherboard CPU Power
 ↓
VRM
 ↓
CPU
```

Không nhầm với PCIe 6-pin.

---

# 4. 8-Pin EPS12V

### Tên

**8-pin EPS12V**

Thường dùng để cấp nguồn CPU.

Có thể gặp dạng:

```text
4+4 pin
```

Hai phần 4-pin ghép lại thành 8-pin.

### Mục đích

Cấp nguồn cho CPU VRM.

---

# 5. CPU EPS vs PCIe

Đây là một điểm rất quan trọng khi lắp PC.

### CPU EPS

Dùng cho:

```text
Motherboard CPU Power
```

### PCIe

Dùng cho:

```text
Graphics Card
```

Không nên dùng sai cable.

Hình dạng keying khác nhau nhằm giúp hạn chế việc cắm nhầm.

---

# 6. PCIe 6-Pin

PCIe 6-pin là connector cấp nguồn phụ cho GPU hoặc các expansion card phù hợp.

Cấu trúc:

```text
6-pin
```

Tài liệu Intel mô tả 2x3 PCIe connector ở mức 75W trong ngữ cảnh PCIe auxiliary power.

---

# 7. PCIe 6+2-Pin

Có thể sử dụng như:

```text
6-pin
```

hoặc:

```text
8-pin
```

Cấu trúc:

```text
[6-pin][+2-pin]
```

Mục đích chính:

- GPU
- PCIe expansion card

---

# 8. 12V-2x6

12V-2x6 là connector nguồn GPU hiện đại.

Intel mô tả PCIe 12V-2x6 là một trong các auxiliary power connectors và thiết kế có thể hỗ trợ các mức công suất đến 600W tùy cấu hình/điều kiện được quy định.

### Khi sử dụng

Cần:

- Cắm hoàn toàn connector.
- Kiểm tra latch.
- Tránh uốn cáp quá sát connector.
- Sử dụng cable phù hợp với PSU.
- Tuân thủ hướng dẫn của PSU/GPU.

---

# 9. SATA Power

Dùng để cấp nguồn cho:

- SATA SSD
- HDD
- Optical Drive
- Một số accessories

Các mức điện áp liên quan thường gồm:

- +3.3V
- +5V
- +12V
- GND

Không phải mọi thiết bị đều sử dụng tất cả các rail.

---

# 10. Molex 4-Pin

Tên phổ biến:

**Peripheral 4-pin**

Thường được gọi là:

**Molex**

Có thể cấp nguồn cho:

- Fan controller
- Legacy HDD
- Optical drive
- Một số accessories
- Adapter

---

# 11. Berg Connector

Connector nhỏ dùng cho floppy drive đời cũ.

Hiện nay rất ít được sử dụng.

---

# 12. Modular PSU Connectors

Ở PSU modular, connector phía PSU có thể khác nhau tùy manufacturer.

Ví dụ:

```text
PSU
├── MB
├── CPU
├── PCIe
├── SATA
└── Peripheral
```

### Cảnh báo cực kỳ quan trọng

**Không được giả định cable modular của PSU này có thể sử dụng với PSU khác.**

Ngay cả khi connector nhìn giống nhau, pinout phía PSU có thể khác.

Sai pinout có thể làm hỏng:

- PSU
- GPU
- SSD
- HDD
- Motherboard
- Các thiết bị khác

---

# 13. Connector Identification Table

| Connector | Primary Use |
|---|---|
| 24-pin ATX | Motherboard |
| 4-pin ATX12V | CPU |
| 4+4 EPS | CPU |
| 6-pin PCIe | GPU |
| 6+2 PCIe | GPU |
| 12V-2x6 | Modern GPU |
| SATA Power | SATA devices |
| Molex | Legacy peripherals |
| Berg | Floppy |

---

# 14. Connector Troubleshooting

Khi PC không nhận nguồn từ một thiết bị:

### Kiểm tra

1. Connector đúng loại?
2. Cắm hết chưa?
3. Latch đã khóa?
4. Cable có bị đứt?
5. Pin có bị cong?
6. Connector có cháy?
7. Có dấu hiệu melting?
8. Có sử dụng cable modular đúng PSU?
9. PSU có đủ công suất?
10. Thiết bị có hoạt động bình thường?

---

## 🇬🇧 English

# PSU Connectors

## 1. Overview

PSUs use multiple connectors to distribute power.

Common connectors include:

- 24-pin ATX
- 4-pin ATX12V
- 4+4-pin EPS
- 6-pin PCIe
- 6+2-pin PCIe
- 12V-2x6
- SATA Power
- 4-pin Peripheral / Molex
- Berg

---

## 2. 24-Pin ATX

The primary motherboard power connector.

```text
PSU
 ↓
24-pin ATX
 ↓
Motherboard
```

It can carry:

- +3.3V
- +5V
- +12V
- Ground
- +5VSB
- PS_ON#
- PWR_OK

---

## 3. 4-Pin ATX12V

Provides CPU power through the motherboard's CPU power circuitry.

```text
PSU
 ↓
ATX12V
 ↓
Motherboard VRM
 ↓
CPU
```

---

## 4. 8-Pin EPS12V

Common CPU power connector.

It may appear as:

```text
4+4-pin EPS
```

---

## 5. CPU EPS vs PCIe

### CPU EPS

Used for:

```text
CPU / Motherboard
```

### PCIe

Used primarily for:

```text
GPU / Expansion Cards
```

They should not be treated as interchangeable cables.

---

## 6. PCIe 6-Pin

Used as auxiliary power for compatible graphics cards and expansion cards.

The PCIe 2x3 connector is specified for 75W in the relevant Intel design documentation.

---

## 7. PCIe 6+2-Pin

Can operate as:

```text
6-pin
```

or:

```text
8-pin
```

Commonly used for graphics cards.

---

## 8. 12V-2x6

A modern high-power PCIe GPU connector.

The Intel documentation describes the 12V-2x6 connector as a PCIe auxiliary power connector, with configurations extending up to 600W under specified conditions.

Best practices:

- Fully insert the connector.
- Ensure the latch is secured.
- Follow PSU and GPU manufacturer instructions.
- Avoid excessive bending near the connector.
- Use the correct cable for the PSU.

---

## 9. SATA Power

Used by:

- SATA SSDs
- HDDs
- Optical drives
- Accessories

SATA power can provide:

- +3.3V
- +5V
- +12V
- Ground

Not every device necessarily uses every rail.

---

## 10. 4-Pin Peripheral / Molex

Used by:

- Legacy drives
- Fan controllers
- Accessories
- Older optical devices

---

## 11. Berg

A small legacy connector originally used for floppy drives.

It is rarely used in modern systems.

---

## 12. Modular PSU Connectors

Modular PSU connections may look similar between brands but can have different pinouts.

### Important

**Never assume that modular cables are interchangeable between PSU models.**

Incorrect pinouts can damage:

- PSU
- GPU
- SSD
- HDD
- Motherboard
- Other components

---

## 13. Connector Table

| Connector | Primary Use |
|---|---|
| 24-pin ATX | Motherboard |
| 4-pin ATX12V | CPU |
| 4+4 EPS | CPU |
| 6-pin PCIe | GPU |
| 6+2 PCIe | GPU |
| 12V-2x6 | Modern GPU |
| SATA Power | SATA devices |
| Molex | Legacy peripherals |
| Berg | Floppy |

---

## 14. Connector Troubleshooting

Check:

1. Correct connector?
2. Fully inserted?
3. Latch secured?
4. Cable damaged?
5. Bent pins?
6. Burn marks?
7. Melted plastic?
8. Correct modular cable?
9. Adequate PSU capacity?
10. Device itself functional?
