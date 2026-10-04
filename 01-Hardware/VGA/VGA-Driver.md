# VGA Driver

> **Tiếng Việt:** Driver VGA và quy trình cài đặt, cập nhật, gỡ bỏ, rollback và xác minh driver.  
> **English:** Graphics drivers and procedures for installation, updating, removal, rollback, and verification.

---

# 1. Driver là gì? | What is a Driver?

## 🇻🇳

Driver là phần mềm trung gian giúp hệ điều hành giao tiếp với phần cứng.

GPU driver cho phép:

```text
Windows
   ↓
GPU Driver
   ↓
GPU Hardware
```

Driver cung cấp:

- Hardware communication.
- Graphics rendering.
- Hardware acceleration.
- Video acceleration.
- Application support.
- Power management.

## 🇬🇧

A driver is software that allows the operating system to communicate with hardware.

The GPU driver provides:

- Hardware communication.
- Graphics rendering.
- Hardware acceleration.
- Video acceleration.
- Application support.
- Power management.

---

# 2. GPU Driver Vendors

Các nhà cung cấp chính:

```text
NVIDIA
AMD
Intel
```

---

# 3. Khi nào cần cài driver?

## 🇻🇳

- Cài Windows mới.
- Lắp VGA mới.
- Windows không nhận GPU.
- Driver bị lỗi.
- Game bị crash.
- Màn hình lỗi.
- Hiệu năng bất thường.
- Cần tính năng mới.

## 🇬🇧

Install or update drivers when:

- Installing Windows.
- Installing a new GPU.
- Windows does not detect the GPU correctly.
- The driver is corrupted.
- Games crash.
- Display problems occur.
- Performance is abnormal.
- New features are required.

---

# 4. Xác định GPU

Có thể sử dụng:

### Device Manager

```text
Device Manager
→ Display adapters
```

### DirectX Diagnostic Tool

```text
Win + R
→ dxdiag
→ Display
```

### System Information

```text
Win + R
→ msinfo32
```

### PowerShell

```powershell
Get-CimInstance Win32_VideoController |
Select-Object Name, DriverVersion, DriverDate
```

---

# 5. Tải driver

## 🇻🇳

Nên tải driver từ nguồn chính thức của nhà sản xuất.

Cần xác định:

```text
GPU Model
Operating System
Driver Branch
Architecture
```

Không nên tải driver từ website không đáng tin cậy.

## 🇬🇧

Download drivers from the official GPU manufacturer whenever possible.

Verify:

```text
GPU Model
Operating System
Driver Branch
Architecture
```

Avoid untrusted driver websites.

---

# 6. Cài driver

Quy trình:

```text
Identify GPU
      ↓
Download Driver
      ↓
Verify Driver
      ↓
Install
      ↓
Restart
      ↓
Verify
      ↓
Test GPU
```

---

# 7. Driver Installation Options

Một số installer có thể cung cấp:

- Express installation.
- Custom installation.
- Clean installation.

### 🇻🇳

Clean installation hữu ích khi:

- Driver bị lỗi.
- Đổi GPU.
- Driver conflict.
- Màn hình bất thường.

### 🇬🇧

A clean installation can be useful when:

- The driver is corrupted.
- Replacing a GPU.
- Driver conflicts occur.
- Display problems persist.

---

# 8. DDU

**Display Driver Uninstaller (DDU)** là công cụ thường được sử dụng để loại bỏ driver đồ họa trong các tình huống cần làm sạch driver.

Quy trình tổng quát:

```text
Download required driver
↓
Boot into Safe Mode
↓
Run DDU
↓
Remove graphics driver
↓
Restart
↓
Install driver
↓
Verify
```

---

# 9. Driver Update

## 🇻🇳

Trước khi cập nhật:

```text
Record current driver
Create restore point when appropriate
Download new driver
```

Sau khi cập nhật:

```text
Restart
Check Device Manager
Check GPU monitoring
Run test
```

## 🇬🇧

Before updating:

```text
Record current driver
Create restore point when appropriate
Download new driver
```

After updating:

```text
Restart
Check Device Manager
Check GPU monitoring
Run test
```

---

# 10. Driver Rollback

Nếu driver mới gây lỗi:

```text
Device Manager
→ Display adapters
→ GPU
→ Properties
→ Driver
→ Roll Back Driver
```

Nếu rollback không khả dụng:

- Tải phiên bản driver trước.
- Gỡ driver hiện tại nếu cần.
- Cài phiên bản ổn định trước đó.

---

# 11. Device Manager Error Codes

Các lỗi thường gặp:

```text
Code 10
Code 12
Code 22
Code 31
Code 43
```

Không nên kết luận nguyên nhân chỉ dựa trên code.

Kiểm tra:

```text
Driver
Hardware
Power
PCIe
BIOS
Windows
```

---

# 12. Driver Verification

Sau khi cài:

```text
Device Manager
→ Display adapters
```

Kiểm tra:

```text
Correct GPU name
No warning icon
Device enabled
Driver installed
Device status normal
```

Có thể xác minh thêm bằng:

- GPU-Z.
- HWiNFO.
- NVIDIA software.
- AMD software.
- Intel graphics software.

---

# 13. Driver Troubleshooting

Nếu driver không cài được:

```text
Check GPU model
↓
Check OS
↓
Check driver package
↓
Remove previous driver if necessary
↓
Restart
↓
Install again
↓
Verify
```

---

# 14. Driver Documentation

```text
GPU Model:
OS:
Previous Driver:
New Driver:
Installation Date:

Installation Type:
[ ] Standard
[ ] Custom
[ ] Clean Installation

Installation Result:
[ ] PASS
[ ] FAIL

Device Manager:
[ ] Normal
[ ] Error

Testing:
[ ] PASS
[ ] FAIL

Notes:
```

---

# 15. Best Practices

## 🇻🇳

- Dùng driver chính thức.
- Xác định chính xác GPU.
- Ghi lại phiên bản driver.
- Không cập nhật tùy tiện trên hệ thống production.
- Test sau khi cập nhật.
- Giữ lại driver ổn định khi cần rollback.
- Không dùng driver mod nếu không hiểu rõ rủi ro.

## 🇬🇧

- Use official drivers.
- Identify the exact GPU.
- Record driver versions.
- Do not update production systems without a reason.
- Test after updating.
- Keep a known-good driver available for rollback.
- Avoid modified drivers unless you understand the risks.
