# Mainboard

> Motherboard / Mainboard Knowledge Base

> Tài liệu kiến thức về Mainboard dành cho IT Support, Hardware Technician, System Administrator và người học Computer Networks.

---

# 🇻🇳 Tiếng Việt

## 1. Giới thiệu

Mainboard là thành phần trung tâm kết nối và giao tiếp giữa:

```text
CPU
│
├── RAM
├── GPU
├── Storage
├── PCIe Devices
├── USB Devices
├── Network
├── Audio
└── Other Peripherals
```

Hiểu mainboard giúp IT Technician có khả năng:

- Lắp ráp máy tính.
- Kiểm tra compatibility.
- Chẩn đoán lỗi hardware.
- Kiểm tra POST.
- Xử lý lỗi BIOS/UEFI.
- Kiểm tra RAM.
- Kiểm tra CPU.
- Kiểm tra storage.
- Kiểm tra I/O.
- Troubleshooting PC.

---

# 🇬🇧 English

A motherboard is the central platform that connects and communicates with:

```text
CPU
│
├── RAM
├── GPU
├── Storage
├── PCIe Devices
├── USB Devices
├── Network
├── Audio
└── Other Peripherals
```

Understanding motherboards helps IT technicians with:

- PC assembly.
- Hardware compatibility.
- Hardware diagnostics.
- POST troubleshooting.
- BIOS/UEFI troubleshooting.
- Memory testing.
- CPU testing.
- Storage troubleshooting.
- I/O testing.

---

# 2. Files

| File | 🇻🇳 Nội dung | 🇬🇧 Content |
|---|---|---|
| `BIOS-UEFI.md` | BIOS và UEFI | BIOS and UEFI |
| `Mainboard-Compatibility.md` | Compatibility | Hardware compatibility |
| `Mainboard-Overview.md` | Tổng quan Mainboard | Motherboard overview |
| `Mainboard-Ports.md` | Cổng và connector | Ports and connectors |
| `Mainboard-Testing.md` | Kiểm tra Mainboard | Motherboard testing |
| `Mainboard-Troubleshooting.md` | Xử lý lỗi | Troubleshooting |

---

# 3. Mainboard Architecture

```text
                         ┌──────────────┐
                         │     CPU      │
                         └──────┬───────┘
                                │
                    CPU Memory / PCIe
                                │
            ┌───────────────────┼───────────────────┐
            │                   │                   │
          RAM                  GPU                NVMe
            │                   │                   │
            └───────────────────┼───────────────────┘
                                │
                         ┌──────▼──────┐
                         │  Chipset    │
                         └──────┬──────┘
                                │
           ┌────────────────────┼────────────────────┐
           │                    │                    │
         SATA                  USB                 LAN
           │                    │                    │
         Audio              Front I/O           Network
```

---

# 4. Main Components

| Component | Function |
|---|---|
| CPU Socket | Kết nối CPU |
| Chipset | Quản lý nhiều I/O |
| DIMM Slots | Kết nối RAM |
| PCIe Slots | GPU và expansion cards |
| M.2 Slots | SSD |
| SATA Ports | SATA storage |
| VRM | Cung cấp điện cho CPU |
| BIOS/UEFI | Firmware |
| CMOS Battery | RTC / configuration support |
| ATX Connector | Main power |
| EPS Connector | CPU power |
| Fan Headers | Cooling |
| USB Headers | Front USB |
| Audio Header | Front audio |
| Network Controller | Ethernet |

---

# 5. Important Concepts

## 🇻🇳 Tiếng Việt

Khi học Mainboard cần nắm:

```text
Socket
Chipset
VRM
DIMM
PCIe
M.2
SATA
BIOS
UEFI
POST
Form Factor
QVL
PCIe Lane
I/O
Power Delivery
```

## 🇬🇧 English

Important motherboard concepts include:

```text
Socket
Chipset
VRM
DIMM
PCIe
M.2
SATA
BIOS
UEFI
POST
Form Factor
QVL
PCIe Lane
I/O
Power Delivery
```

---

# 6. Troubleshooting Workflow

```text
Identify
   ↓
Inspect
   ↓
Power
   ↓
POST
   ↓
BIOS
   ↓
Hardware Detection
   ↓
Operating System
   ↓
Device Testing
   ↓
Stress / Stability
   ↓
Document
```

---

# 7. Mainboard Checklist

```text
[ ] Identify motherboard model
[ ] Identify revision
[ ] Check BIOS version
[ ] Check CPU compatibility
[ ] Check RAM compatibility
[ ] Check GPU compatibility
[ ] Check storage compatibility
[ ] Check PSU requirements
[ ] Check case compatibility
[ ] Inspect motherboard
[ ] Test POST
[ ] Test RAM
[ ] Test CPU
[ ] Test GPU
[ ] Test storage
[ ] Test USB
[ ] Test Ethernet
[ ] Test Audio
[ ] Test PCIe
[ ] Test stability
[ ] Document results
```

---

# 8. Documentation Standard

Mỗi hardware case nên ghi:

```text
Device
Model
Revision
BIOS
CPU
RAM
GPU
Storage
PSU
Symptoms
Environment
Tests
Results
Root Cause
Solution
Verification
Notes
```

---

# 9. Knowledge vs Work Log

## 🇻🇳 Tiếng Việt

`IT-Knowledge-Base` chứa:

- Kiến thức tổng quát.
- Nguyên lý.
- Quy trình.
- Checklist.
- Troubleshooting methodology.
- Technical references.

`IT-Work-Log` chứa:

- Case thực tế.
- Thiết bị thực tế.
- Lỗi thực tế.
- Cách xử lý.
- Kết quả.
- Hình ảnh nếu cần.

Ví dụ:

```text
IT-Knowledge-Base
└── Mainboard
    └── Mainboard-Troubleshooting.md

IT-Work-Log
└── 01-Hardware
    └── Mainboard
        └── 2026
            └── ASUS-B760-No-POST.md
```

## 🇬🇧 English

`IT-Knowledge-Base` contains:

- General knowledge.
- Technical concepts.
- Procedures.
- Checklists.
- Troubleshooting methodology.
- Technical references.

`IT-Work-Log` contains:

- Real-world cases.
- Real devices.
- Actual symptoms.
- Troubleshooting steps.
- Results.
- Supporting images when needed.

---

# 10. Recommended Learning Path

```text
01. Mainboard Overview
        ↓
02. Mainboard Ports
        ↓
03. BIOS / UEFI
        ↓
04. Compatibility
        ↓
05. Testing
        ↓
06. Troubleshooting
        ↓
07. Real-world Work Logs
```

---

# 11. Learning Goals

## 🇻🇳 Tiếng Việt

Sau khi hoàn thành phần Mainboard, mục tiêu là có thể:

- Đọc thông số motherboard.
- Xác định socket.
- Xác định chipset.
- Kiểm tra CPU compatibility.
- Kiểm tra RAM compatibility.
- Hiểu PCIe.
- Hiểu M.2.
- Hiểu SATA.
- Cấu hình BIOS.
- Thực hiện POST testing.
- Kiểm tra I/O.
- Phân tích lỗi no POST.
- Phân tích lỗi no display.
- Phân tích lỗi RAM.
- Phân tích lỗi storage.
- Phân tích lỗi USB/network/audio.

## 🇬🇧 English

After completing this section, you should be able to:

- Read motherboard specifications.
- Identify CPU sockets.
- Identify chipsets.
- Check CPU compatibility.
- Check memory compatibility.
- Understand PCIe.
- Understand M.2.
- Understand SATA.
- Configure BIOS/UEFI.
- Perform POST testing.
- Test motherboard I/O.
- Troubleshoot no-POST problems.
- Troubleshoot display problems.
- Troubleshoot memory problems.
- Troubleshoot storage problems.
- Troubleshoot USB/network/audio issues.

---

# 12. Mainboard Knowledge Map

```text
Mainboard
│
├── Overview
│   ├── Socket
│   ├── Chipset
│   ├── VRM
│   ├── DIMM
│   ├── PCIe
│   ├── M.2
│   └── SATA
│
├── BIOS / UEFI
│   ├── POST
│   ├── Boot
│   ├── Secure Boot
│   ├── TPM
│   ├── Virtualization
│   └── BIOS Update
│
├── Compatibility
│   ├── CPU
│   ├── RAM
│   ├── GPU
│   ├── Storage
│   ├── PSU
│   └── Case
│
├── Ports
│   ├── USB
│   ├── Display
│   ├── Ethernet
│   ├── Audio
│   ├── SATA
│   └── Internal Headers
│
├── Testing
│   ├── POST
│   ├── RAM
│   ├── CPU
│   ├── Storage
│   ├── I/O
│   └── Stability
│
└── Troubleshooting
    ├── No Power
    ├── No POST
    ├── No Display
    ├── RAM
    ├── Storage
    ├── USB
    ├── Network
    └── Audio
```

---

# 13. Important Notes

## 🇻🇳 Tiếng Việt

Thông số và tính năng có thể khác nhau giữa từng motherboard.

Không nên áp dụng một thông tin của một model cho tất cả motherboard.

Luôn kiểm tra:

- Official specifications.
- User manual.
- CPU Support List.
- Memory QVL.
- BIOS release notes.
- Motherboard revision.

## 🇬🇧 English

Specifications and features vary between motherboard models.

Do not assume that a feature on one motherboard exists on every motherboard.

Always verify:

- Official specifications.
- User manual.
- CPU support list.
- Memory QVL.
- BIOS release notes.
- Board revision.

---

# 14. Related Knowledge

```text
../CPU/
../RAM/
../SSD-HDD/
../VGA/
../PSU/
../PC/
```

---

# 15. Final Principle

## 🇻🇳 Tiếng Việt

> **Không chỉ học cách lắp Mainboard. Hãy học cách đọc, kiểm tra, chẩn đoán và giải thích Mainboard.**

## 🇬🇧 English

> **Do not only learn how to install a motherboard. Learn how to read, test, troubleshoot and explain it.**
