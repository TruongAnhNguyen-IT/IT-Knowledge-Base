# BIOS & UEFI

> BIOS/UEFI is the firmware responsible for initializing hardware and starting the operating system boot process.

> BIOS/UEFI là firmware chịu trách nhiệm khởi tạo phần cứng và bắt đầu quá trình khởi động hệ điều hành.

---

# 1. BIOS/UEFI là gì?

## 🇻🇳 Tiếng Việt

**BIOS** (Basic Input/Output System) và **UEFI** (Unified Extensible Firmware Interface) là firmware được lưu trên mainboard.

Firmware này chạy trước hệ điều hành và có nhiệm vụ:

- Kiểm tra phần cứng khi bật máy.
- Khởi tạo CPU.
- Khởi tạo RAM.
- Khởi tạo thiết bị lưu trữ.
- Khởi tạo USB và các thiết bị cơ bản.
- Xác định thiết bị boot.
- Cung cấp giao diện cấu hình phần cứng.
- Chuyển quyền điều khiển cho bootloader của hệ điều hành.

Quá trình tổng quát:

```text
Power ON
   │
   ▼
CPU Reset
   │
   ▼
BIOS / UEFI Firmware
   │
   ▼
Hardware Initialization
   │
   ├── CPU
   ├── RAM
   ├── GPU
   ├── Storage
   ├── USB
   └── Other devices
   │
   ▼
POST
   │
   ▼
Boot Device Selection
   │
   ▼
Windows Boot Manager / Linux Bootloader
   │
   ▼
Operating System
```

## 🇬🇧 English

**BIOS** and **UEFI** are motherboard firmware interfaces.

They run before the operating system and are responsible for:

- Hardware initialization.
- CPU initialization.
- Memory initialization.
- Storage initialization.
- USB initialization.
- Boot device detection.
- Hardware configuration.
- Starting the operating system bootloader.

---

# 2. BIOS và UEFI

## 🇻🇳 Tiếng Việt

BIOS truyền thống là firmware thế hệ cũ.

UEFI là firmware hiện đại thay thế BIOS legacy trên phần lớn hệ thống mới.

| Feature | Legacy BIOS | UEFI |
|---|---|---|
| Interface | Text-based | Graphical/Text |
| Boot mode | Legacy | UEFI |
| GPT support | Limited | Native |
| Secure Boot | Không | Có |
| Large storage support | Hạn chế | Tốt hơn |
| Boot management | Legacy | Windows Boot Manager / EFI |
| Modern OS | Limited | Recommended |

## 🇬🇧 English

Legacy BIOS is an older firmware environment.

UEFI is the modern firmware standard used by most current systems.

UEFI provides features such as:

- UEFI boot mode.
- GPT support.
- Secure Boot.
- Better boot management.
- Modern firmware interfaces.

---

# 3. POST

## 🇻🇳 Tiếng Việt

**POST (Power-On Self-Test)** là quá trình mainboard kiểm tra phần cứng cơ bản khi máy khởi động.

Các thành phần thường được kiểm tra:

```text
CPU
RAM
GPU / Display
Storage
Keyboard
Other motherboard devices
```

Nếu POST thất bại, máy có thể:

- Không lên hình.
- Restart liên tục.
- Beep code.
- Hiển thị Debug LED.
- Hiển thị POST Code.
- Dừng tại một bước boot.

## 🇬🇧 English

POST is the initial hardware self-test performed during system startup.

A POST failure may result in:

- No display.
- Continuous reboot.
- Beep codes.
- Debug LEDs.
- POST codes.
- Boot failure.

---

# 4. BIOS/UEFI Setup

## 🇻🇳 Tiếng Việt

BIOS/UEFI Setup thường được truy cập bằng phím:

```text
Delete
F2
F10
F12
Esc
```

Phím cụ thể phụ thuộc nhà sản xuất.

Các nhóm cấu hình phổ biến:

```text
Main
Advanced
Boot
Security
Power
Hardware Monitor
Overclocking
Tools
Exit
```

## 🇬🇧 English

BIOS/UEFI Setup can commonly be accessed using:

```text
Delete
F2
F10
F12
Esc
```

The exact key depends on the motherboard manufacturer.

---

# 5. Các thiết lập BIOS/UEFI quan trọng

## 🇻🇳 Tiếng Việt

### Boot Mode

```text
UEFI
Legacy / CSM
```

### Boot Priority

Xác định thiết bị được boot trước.

Ví dụ:

```text
1. Windows Boot Manager
2. SSD
3. USB
4. Network
```

### Secure Boot

Secure Boot giúp firmware kiểm tra bootloader trước khi thực thi.

### TPM

TPM thường được sử dụng cho:

- Windows 11.
- BitLocker.
- Security features.

### Virtualization

Các tùy chọn phổ biến:

```text
Intel VT-x
Intel VT-d
AMD SVM
AMD IOMMU
```

Dùng cho:

- Hyper-V.
- VMware.
- VirtualBox.
- Các nền tảng virtualization khác.

### XMP / EXPO

Dùng để áp dụng memory profile do nhà sản xuất RAM cung cấp.

Ví dụ:

```text
DDR5-6000
CL30
```

Thông số thực tế còn phụ thuộc CPU, mainboard và RAM.

## 🇬🇧 English

Important firmware settings include:

- Boot Mode.
- Boot Priority.
- Secure Boot.
- TPM.
- CPU Virtualization.
- IOMMU.
- XMP.
- EXPO.
- Fan configuration.
- Integrated graphics.
- Storage configuration.

---

# 6. BIOS Update

## 🇻🇳 Tiếng Việt

BIOS update có thể:

- Hỗ trợ CPU mới.
- Sửa lỗi firmware.
- Cải thiện compatibility.
- Cải thiện stability.
- Cập nhật security fixes.
- Cải thiện memory compatibility.

Quy trình tổng quát:

```text
1. Identify motherboard model
2. Check current BIOS version
3. Visit manufacturer support page
4. Check BIOS release notes
5. Download correct BIOS
6. Prepare USB
7. Enter BIOS
8. Start BIOS update utility
9. Select BIOS file
10. Wait for completion
11. Reboot
12. Load/verify settings
```

### Important

Không được:

- Tắt nguồn giữa quá trình update.
- Reset máy.
- Rút USB khi firmware đang được ghi.
- Sử dụng BIOS sai model.
- Flash BIOS không tương thích.

## 🇬🇧 English

BIOS updates may provide:

- New CPU support.
- Bug fixes.
- Compatibility improvements.
- Stability improvements.
- Security fixes.
- Memory compatibility improvements.

Always verify:

```text
Motherboard Model
Board Revision
BIOS Version
BIOS File
Release Notes
```

---

# 7. Clear CMOS

## 🇻🇳 Tiếng Việt

Clear CMOS đưa nhiều thiết lập firmware về mặc định.

Có thể thực hiện bằng:

- CMOS jumper.
- Clear CMOS button.
- Remove CMOS battery.
- Manufacturer-specific procedure.

Có thể hữu ích khi:

- Không POST sau khi thay đổi BIOS.
- Overclock không ổn định.
- RAM profile gây lỗi.
- Sai boot configuration.
- Thay đổi hardware khiến firmware không khởi động bình thường.

## 🇬🇧 English

Clear CMOS resets firmware configuration to default values.

It can help when:

- POST fails after BIOS changes.
- Memory settings are unstable.
- Overclocking settings fail.
- Incorrect boot configuration prevents startup.

---

# 8. BIOS Troubleshooting

## 🇻🇳 Tiếng Việt

### Máy không vào BIOS

Kiểm tra:

```text
Keyboard
USB port
Display
POST
CPU
RAM
GPU
BIOS settings
```

### BIOS không nhận RAM

Kiểm tra:

```text
RAM seating
DIMM slot
Memory compatibility
BIOS version
XMP/EXPO
CPU memory controller
```

### BIOS không nhận SSD

Kiểm tra:

```text
SATA cable
Power cable
M.2 installation
Storage interface
BIOS storage configuration
PCIe/SATA lane sharing
```

### Không boot Windows

Kiểm tra:

```text
Boot Mode
Boot Priority
Windows Boot Manager
EFI partition
Storage detection
Secure Boot
```

---

# 9. BIOS Documentation Template

```markdown
# BIOS / UEFI Record

## Motherboard

- Manufacturer:
- Model:
- Revision:

## Current BIOS

- Version:
- Date:

## CPU

- Model:

## RAM

- Capacity:
- Speed:

## Storage

- SSD:
- HDD:

## BIOS Configuration

- Boot Mode:
- Secure Boot:
- TPM:
- Virtualization:
- XMP/EXPO:

## Changes

- Date:
- Change:
- Reason:
- Result:

## Notes

- 
```

---

# 10. Best Practices

## 🇻🇳 Tiếng Việt

Luôn:

- Ghi lại BIOS version trước khi update.
- Đọc release notes.
- Kiểm tra đúng motherboard model.
- Kiểm tra revision nếu nhà sản xuất yêu cầu.
- Backup cấu hình quan trọng.
- Không update BIOS nếu không có lý do rõ ràng.

## 🇬🇧 English

Always:

- Record the current BIOS version.
- Read release notes.
- Verify the exact motherboard model.
- Verify board revision when required.
- Record important settings.
- Avoid unnecessary firmware updates.

---

# Summary

BIOS/UEFI là thành phần nền tảng của motherboard.

Cần hiểu:

```text
BIOS / UEFI
├── POST
├── Hardware Initialization
├── Boot Mode
├── Boot Priority
├── Secure Boot
├── TPM
├── Virtualization
├── Memory Configuration
├── Storage Configuration
├── BIOS Update
└── Clear CMOS
```
