# Mainboard Compatibility

> Mainboard compatibility determines whether CPU, RAM, GPU, storage, power supply, chassis and other components can work together correctly.

> Khả năng tương thích của mainboard quyết định CPU, RAM, VGA, ổ lưu trữ, nguồn, case và các thiết bị khác có thể hoạt động cùng nhau hay không.

---

# 1. Compatibility Overview

## 🇻🇳 Tiếng Việt

Không thể xác định compatibility chỉ bằng một thông số.

Ví dụ:

```text
CPU Socket = LGA1200
```

không có nghĩa tất cả CPU LGA1200 đều hoạt động trên mọi mainboard LGA1200.

Cần kiểm tra:

```text
CPU
↓
Socket
↓
Chipset
↓
BIOS
↓
CPU Support List
↓
VRM / Power
↓
RAM
↓
PCIe
↓
Storage
↓
PSU
↓
Case
```

## 🇬🇧 English

Component compatibility is not determined by a single specification.

A compatible socket does not automatically guarantee CPU compatibility.

Always verify the motherboard manufacturer's documentation.

---

# 2. CPU Compatibility

## 🇻🇳 Tiếng Việt

Kiểm tra:

- CPU socket.
- Chipset.
- BIOS version.
- CPU support list.
- TDP/power requirements.
- VRM capability.
- RAM support.
- Manufacturer restrictions.

Ví dụ:

```text
CPU:
Intel Core i5-10400

Socket:
LGA1200

Required:
Compatible motherboard
Compatible chipset
Supported BIOS
Compatible DDR4 memory
```

## 🇬🇧 English

Check:

- CPU socket.
- Chipset.
- BIOS support.
- CPU support list.
- Power requirements.
- VRM capability.
- Memory compatibility.

---

# 3. CPU Support List

## 🇻🇳 Tiếng Việt

CPU Support List của nhà sản xuất thường cho biết:

| Information | Description |
|---|---|
| CPU Model | Model CPU |
| CPU Family | Generation/family |
| Core Count | Số nhân |
| BIOS Version | BIOS tối thiểu |
| TDP | Công suất thiết kế |
| Status | Supported/Not supported |

Ví dụ:

```text
CPU: Intel Core i7-10700
Socket: LGA1200
BIOS: Version XXXX or newer
```

## 🇬🇧 English

The CPU support list usually identifies:

- Supported CPU model.
- Required BIOS version.
- CPU family.
- TDP.
- Support status.

---

# 4. RAM Compatibility

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
RAM Generation
DDR4 / DDR5
```

Không thể sử dụng DDR4 trên khe DDR5 hoặc ngược lại.

Kiểm tra thêm:

- Maximum capacity.
- Number of DIMM slots.
- Supported frequency.
- Module type.
- ECC support.
- Registered/Unbuffered.
- XMP/EXPO support.
- Memory QVL.

## 🇬🇧 English

Check:

- DDR generation.
- Maximum capacity.
- Maximum supported frequency.
- DIMM type.
- ECC support.
- Registered/Unbuffered memory.
- XMP/EXPO.
- Memory QVL.

---

# 5. RAM QVL

## 🇻🇳 Tiếng Việt

**QVL (Qualified Vendor List)** là danh sách module RAM đã được nhà sản xuất kiểm tra hoặc xác nhận compatibility.

QVL không có nghĩa RAM ngoài danh sách chắc chắn không chạy.

Nó chỉ giúp giảm rủi ro compatibility.

## 🇬🇧 English

A QVL lists memory modules tested or validated by the motherboard manufacturer.

Memory not listed on the QVL may still work, but the QVL can reduce compatibility uncertainty.

---

# 6. GPU Compatibility

## 🇻🇳 Tiếng Việt

GPU thường sử dụng:

```text
PCI Express x16
```

Cần kiểm tra:

- PCIe slot.
- GPU physical dimensions.
- PSU requirement.
- Power connectors.
- Case clearance.
- Cooling.
- BIOS compatibility where applicable.

## 🇬🇧 English

GPU compatibility depends on:

- PCIe interface.
- Physical dimensions.
- PSU capacity.
- Power connectors.
- Case clearance.
- Cooling.
- Firmware/platform compatibility where applicable.

---

# 7. Storage Compatibility

## 🇻🇳 Tiếng Việt

Mainboard có thể hỗ trợ:

```text
SATA
M.2 SATA
M.2 NVMe
PCIe NVMe
```

Không phải mọi M.2 đều giống nhau.

Cần kiểm tra:

```text
M.2 Key
Protocol
PCIe Generation
Lane configuration
Physical size
```

Ví dụ:

```text
M.2 2280
NVMe
PCIe x4
```

## 🇬🇧 English

Storage compatibility depends on:

- SATA support.
- M.2 form factor.
- SATA or NVMe protocol.
- PCIe generation.
- PCIe lane configuration.
- M.2 physical size.

---

# 8. PCIe Lane Sharing

## 🇻🇳 Tiếng Việt

Một số mainboard chia sẻ lane giữa:

```text
M.2
SATA
PCIe slots
```

Ví dụ:

```text
M.2_2 occupied
      ↓
SATA_5 / SATA_6 disabled
```

Hoặc:

```text
PCIe Slot 2
      ↓
M.2 bandwidth changes
```

Phải kiểm tra manual của từng motherboard.

## 🇬🇧 English

Motherboards may share PCIe or chipset resources between:

- M.2 slots.
- SATA ports.
- PCIe slots.

Using one connector may disable or reduce another interface.

Always check the motherboard manual.

---

# 9. PSU Compatibility

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
24-pin ATX
8-pin / 4+4 CPU EPS
PCIe GPU power
12VHPWR / 12V-2x6 where applicable
PSU wattage
Connector compatibility
```

Không chỉ nhìn tổng watt.

Cần xem:

- PSU quality.
- 12V capability.
- GPU power requirement.
- CPU power requirement.
- Connector type.

## 🇬🇧 English

Check:

- ATX 24-pin.
- CPU EPS connector.
- GPU power connectors.
- PSU capacity.
- Connector compatibility.
- Power delivery capability.

---

# 10. Case Compatibility

## 🇻🇳 Tiếng Việt

Kiểm tra motherboard form factor:

```text
E-ATX
ATX
Micro-ATX
Mini-ITX
```

Sau đó kiểm tra:

- Case support.
- Standoff positions.
- GPU length.
- CPU cooler height.
- Radiator support.
- PSU dimensions.
- Cable clearance.

## 🇬🇧 English

Check:

- Motherboard form factor.
- Case support.
- Mounting holes.
- GPU clearance.
- CPU cooler clearance.
- Radiator support.
- PSU dimensions.

---

# 11. Front Panel Compatibility

## 🇻🇳 Tiếng Việt

Kiểm tra:

```text
Power Switch
Reset Switch
Power LED
HDD LED
Front USB
Front Audio
Front USB-C
```

Không nên cắm theo màu dây một cách máy móc.

Phải xem motherboard manual.

## 🇬🇧 English

Check compatibility for:

- Power switch.
- Reset switch.
- LEDs.
- USB headers.
- Front audio.
- Front USB-C.

Always follow the motherboard manual.

---

# 12. Compatibility Checklist

```text
[ ] CPU Socket
[ ] CPU Support List
[ ] BIOS Version
[ ] Chipset
[ ] VRM
[ ] RAM Generation
[ ] RAM Capacity
[ ] RAM QVL
[ ] GPU PCIe
[ ] GPU Size
[ ] PSU
[ ] Storage Interface
[ ] M.2 Compatibility
[ ] PCIe Lane Sharing
[ ] Case Form Factor
[ ] CPU Cooler
[ ] Front Panel
[ ] Cooling
```

---

# 13. Compatibility Documentation Template

```markdown
# Mainboard Compatibility Record

## Motherboard

- Brand:
- Model:
- Chipset:
- Form Factor:

## CPU

- Model:
- Socket:
- Supported BIOS:

## RAM

- Type:
- Maximum Capacity:
- Maximum Speed:
- QVL:

## GPU

- Interface:
- Slot:
- Clearance:

## Storage

- M.2:
- SATA:
- PCIe:

## PSU

- Recommended Wattage:
- CPU Power:
- GPU Power:

## Case

- Supported Form Factor:
- GPU Clearance:
- CPU Cooler Clearance:

## Notes

-
```

---

# Summary

Mainboard compatibility should always be checked as a complete system:

```text
CPU
RAM
GPU
Storage
PSU
Case
Cooling
BIOS
PCIe
I/O
```

Never assume compatibility from only one specification.
