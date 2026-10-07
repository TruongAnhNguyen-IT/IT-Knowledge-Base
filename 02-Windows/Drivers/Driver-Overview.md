# Driver Overview

## 🇻🇳 TIẾNG VIỆT

## 1. Driver là gì?

**Driver** là phần mềm trung gian cho phép hệ điều hành Windows giao tiếp và điều khiển một thiết bị phần cứng.

Có thể hình dung:

```text
Application
     ↓
Windows
     ↓
Driver
     ↓
Hardware
```

Ví dụ:

```text
Windows
   ↓
Network Driver
   ↓
Intel / Realtek Network Adapter
   ↓
Network
```

Nếu driver không tồn tại hoặc không tương thích, Windows có thể không sử dụng được đầy đủ chức năng của thiết bị.

---

# 2. Driver có vai trò gì?

Driver giúp Windows:

- Nhận diện hardware.
- Giao tiếp với hardware.
- Điều khiển hardware.
- Cấu hình hardware.
- Cung cấp các chức năng nâng cao.
- Quản lý tài nguyên thiết bị.
- Xử lý giao tiếp giữa OS và thiết bị.

Ví dụ:

### VGA

```text
Windows
↓
NVIDIA / AMD / Intel Driver
↓
GPU
```

### Audio

```text
Windows
↓
Audio Driver
↓
Audio Controller
↓
Speaker / Headphone
```

### Network

```text
Windows
↓
LAN / Wi-Fi Driver
↓
Network Adapter
↓
Network
```

---

# 3. Các loại driver phổ biến

## 3.1 Chipset Driver

Quản lý và hỗ trợ giao tiếp giữa:

- CPU.
- Chipset.
- PCIe.
- USB.
- Storage.
- Motherboard controllers.

---

## 3.2 Graphics Driver

Dùng cho:

- Integrated GPU.
- Dedicated GPU.

Ví dụ:

- Intel Graphics.
- NVIDIA GeForce.
- AMD Radeon.

---

## 3.3 Network Driver

Bao gồm:

- Ethernet.
- Wi-Fi.
- Bluetooth.

Nhà sản xuất phổ biến:

- Intel.
- Realtek.
- MediaTek.
- Broadcom.
- Qualcomm.

---

## 3.4 Audio Driver

Dùng cho:

- Internal audio.
- Speaker.
- Headphone.
- Microphone.
- HDMI/DisplayPort audio.

Ví dụ:

- Realtek Audio.
- Intel Audio.
- AMD Audio.
- NVIDIA High Definition Audio.

---

## 3.5 Storage Driver

Có thể liên quan đến:

- SATA controller.
- NVMe.
- RAID controller.
- Storage controller.

---

## 3.6 USB Driver

Windows thường có sẵn nhiều USB driver, nhưng một số thiết bị cần driver riêng.

Ví dụ:

- USB controller.
- USB-to-Serial.
- USB printer.
- USB device.

---

## 3.7 Printer Driver

Cho phép Windows giao tiếp với:

- Laser printer.
- Inkjet printer.
- Label printer.
- Barcode printer.
- POS printer.

---

## 3.8 Bluetooth Driver

Điều khiển Bluetooth adapter và hỗ trợ:

- Keyboard.
- Mouse.
- Headset.
- Smartphone.
- Other Bluetooth devices.

---

# 4. Windows Driver Model

Windows sử dụng các mô hình driver để giao tiếp với hardware.

Một số khái niệm:

- WDM – Windows Driver Model.
- WDF – Windows Driver Framework.
- KMDF – Kernel-Mode Driver Framework.
- UMDF – User-Mode Driver Framework.

Không phải IT Support cần viết driver, nhưng cần hiểu các khái niệm này khi troubleshooting.

---

# 5. Hardware ID

Windows có thể xác định thiết bị thông qua Hardware ID.

Ví dụ:

```text
PCI\VEN_8086&DEV_XXXX
```

Trong đó:

```text
VEN = Vendor
DEV = Device
```

Hardware ID rất hữu ích khi:

- Unknown Device.
- Không biết model hardware.
- Không tìm được driver.
- Driver tự động không hoạt động.

Có thể xem tại:

```text
Device Manager
→ Device
→ Properties
→ Details
→ Hardware Ids
```

---

# 6. Device Manager

Device Manager là công cụ quan trọng để quản lý driver.

Mở bằng:

```text
Win + X
→ Device Manager
```

Hoặc:

```text
Win + R
→ devmgmt.msc
```

Có thể kiểm tra:

- Device name.
- Driver provider.
- Driver version.
- Driver date.
- Device status.
- Hardware ID.
- Driver files.

---

# 7. Driver Store

Windows lưu driver packages trong Driver Store.

Vị trí thường gặp:

```text
C:\Windows\System32\DriverStore
```

Không nên tự ý xóa file trong thư mục này.

Windows sử dụng Driver Store để:

- Lưu driver package.
- Cài driver.
- Reinstall driver.
- Manage driver packages.

---

# 8. Driver Package

Một driver package có thể bao gồm:

- `.inf`
- `.sys`
- `.cat`
- `.dll`
- Supporting files

### `.inf`

Chứa thông tin hướng dẫn cài đặt driver.

### `.sys`

Có thể chứa driver binary.

### `.cat`

Chứa thông tin chữ ký và tính toàn vẹn của package.

---

# 9. Signed Driver

Windows có cơ chế kiểm tra chữ ký driver.

Driver được ký giúp xác minh:

- Nguồn driver.
- Tính toàn vẹn.
- Khả năng tương thích với Windows.

Không nên cài driver không rõ nguồn gốc.

---

# 10. Microsoft Driver và OEM Driver

## Microsoft Driver

Driver được Microsoft phân phối hoặc tích hợp trong Windows.

Ưu điểm:

- Dễ cài.
- Tương thích tốt với Windows.
- Có thể cài tự động.

## OEM Driver

Driver do nhà sản xuất thiết bị cung cấp.

Ví dụ:

- Dell.
- HP.
- Lenovo.
- ASUS.
- Acer.

OEM driver đôi khi được tùy chỉnh cho model cụ thể.

---

# 11. Windows Update Driver

Windows Update có thể tự động cung cấp driver.

Ưu điểm:

- Dễ sử dụng.
- Tự động.
- Phù hợp cho nhiều thiết bị.

Nhược điểm:

- Có thể không phải phiên bản mới nhất.
- Một số driver chuyên dụng cần tải trực tiếp từ vendor.

---

# 12. Driver Version

Thông tin driver thường gồm:

```text
Driver Provider
Driver Date
Driver Version
Digital Signer
```

Ví dụ:

```text
Provider:
Intel

Version:
31.x.x.x

Date:
2026-xx-xx
```

---

# 13. Khi nào cần kiểm tra Driver?

Cần kiểm tra driver khi:

- Cài Windows mới.
- Thay hardware.
- Hardware không nhận.
- Device Manager có dấu `!`.
- Mất mạng.
- Mất âm thanh.
- Màn hình lỗi.
- GPU crash.
- Printer không hoạt động.
- Bluetooth không hoạt động.
- USB device lỗi.

---

# 14. Nguyên tắc quản lý Driver

Nên:

- Download từ nguồn chính thức.
- Xác định đúng model.
- Kiểm tra Windows version.
- Kiểm tra architecture.
- Backup driver quan trọng.
- Ghi lại version.
- Test sau khi cài.

Không nên:

- Tải driver từ website không rõ nguồn.
- Cài driver không đúng model.
- Dùng nhiều driver updater không cần thiết.
- Xóa Driver Store thủ công.

---

## Driver Management Checklist

```text
[ ] Identify hardware
[ ] Identify Hardware ID
[ ] Identify Windows version
[ ] Check architecture
[ ] Download correct driver
[ ] Verify source
[ ] Install
[ ] Restart if required
[ ] Check Device Manager
[ ] Test hardware
[ ] Record driver version
```

---

# 🇬🇧 ENGLISH

# 1. What is a Driver?

A **driver** is software that allows Windows to communicate with and control hardware.

Basic architecture:

```text
Application
     ↓
Windows
     ↓
Driver
     ↓
Hardware
```

---

# 2. Driver Functions

A driver allows Windows to:

- Detect hardware.
- Communicate with hardware.
- Control hardware.
- Configure hardware.
- Provide advanced functions.
- Manage device resources.

---

# 3. Common Driver Types

Common Windows drivers include:

- Chipset drivers.
- Graphics drivers.
- Network drivers.
- Audio drivers.
- Storage drivers.
- USB drivers.
- Printer drivers.
- Bluetooth drivers.

---

# 4. Hardware ID

Hardware IDs identify hardware devices.

Example:

```text
PCI\VEN_8086&DEV_XXXX
```

Hardware IDs are useful when:

- A device is unknown.
- Automatic driver installation fails.
- The exact hardware model is unknown.

Location:

```text
Device Manager
→ Device
→ Properties
→ Details
→ Hardware Ids
```

---

# 5. Device Manager

Open:

```text
Win + X
→ Device Manager
```

or:

```text
Win + R
→ devmgmt.msc
```

Device Manager can show:

- Device name.
- Driver provider.
- Driver version.
- Driver date.
- Device status.
- Hardware ID.

---

# 6. Driver Store

Windows stores driver packages in the Driver Store.

Typical location:

```text
C:\Windows\System32\DriverStore
```

Do not manually delete files from this directory.

---

# 7. Driver Package

A driver package may contain:

```text
.inf
.sys
.cat
.dll
```

The `.inf` file contains installation information, while `.sys` files may contain driver binaries.

---

# 8. Driver Sources

Common sources:

- Microsoft.
- Windows Update.
- OEM manufacturer.
- Hardware vendor.

Preferred sources should be official and trusted.

---

# 9. Driver Management Best Practices

Always:

- Identify the exact hardware.
- Verify the Windows version.
- Download from a trusted source.
- Check driver compatibility.
- Record driver versions.
- Test after installation.
- Maintain backups when appropriate.

Avoid:

- Unknown driver websites.
- Incorrect drivers.
- Unnecessary driver updater applications.
- Manual deletion from Driver Store.

---

# 2. `Driver-Installation.md`
