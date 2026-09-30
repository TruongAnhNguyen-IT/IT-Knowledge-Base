# Mainboard

## Bo mạch chủ / Motherboard

---

## 🇻🇳 Tổng quan

**Mainboard (Bo mạch chủ)** là bảng mạch chính của máy tính, có nhiệm vụ kết nối và điều phối hoạt động giữa CPU, RAM, GPU, Storage, PSU và các thiết bị ngoại vi.

Mainboard quyết định phần lớn khả năng tương thích và khả năng mở rộng của hệ thống.

**English:**

A **mainboard (motherboard)** is the primary circuit board of a computer. It connects and enables communication between the CPU, RAM, GPU, storage devices, PSU, and peripheral devices.

The motherboard plays an important role in determining system compatibility, connectivity, and upgradeability.

---

# 📚 Contents

| File | Nội dung / Content |
|---|---|
| [BIOS-UEFI.md](BIOS-UEFI.md) | BIOS/UEFI, boot process, configuration and firmware |
| [Mainboard-Compatibility.md](Mainboard-Compatibility.md) | CPU, RAM, GPU, storage and PSU compatibility |
| [Mainboard-Overview.md](Mainboard-Overview.md) | Mainboard architecture and components |
| [Mainboard-Ports.md](Mainboard-Ports.md) | Internal headers and external I/O ports |
| [Mainboard-Testing.md](Mainboard-Testing.md) | Mainboard inspection and testing procedures |
| [Mainboard-Troubleshooting.md](Mainboard-Troubleshooting.md) | Mainboard troubleshooting and fault diagnosis |

---

# 🎯 Learning Objectives

## 🇻🇳 Mục tiêu học tập

Sau khi hoàn thành phần này, có thể:

- Hiểu cấu trúc của mainboard.
- Nhận biết các thành phần chính trên mainboard.
- Hiểu socket CPU và chipset.
- Hiểu khe RAM.
- Hiểu PCIe và các khe mở rộng.
- Hiểu SATA và M.2.
- Nhận biết các cổng I/O.
- Hiểu BIOS/UEFI.
- Kiểm tra khả năng tương thích phần cứng.
- Kiểm tra và chẩn đoán lỗi mainboard.
- Thực hiện quy trình troubleshooting có hệ thống.
- Ghi nhận kết quả kiểm tra vào báo cáo kỹ thuật.

## English

After completing this section, you should be able to:

- Understand motherboard architecture.
- Identify major motherboard components.
- Understand CPU sockets and chipsets.
- Understand RAM slots.
- Understand PCIe expansion slots.
- Understand SATA and M.2 interfaces.
- Identify external I/O ports.
- Understand BIOS/UEFI.
- Verify hardware compatibility.
- Test and troubleshoot motherboard problems.
- Follow a systematic troubleshooting process.
- Document technical test results.

---

# 🧩 Mainboard Components

| Component | Tiếng Việt | Chức năng |
|---|---|---|
| CPU Socket | Socket CPU | Kết nối CPU với mainboard |
| Chipset | Chipset | Điều phối nhiều chức năng I/O |
| DIMM Slots | Khe RAM | Lắp RAM |
| PCIe Slots | Khe PCI Express | GPU và card mở rộng |
| M.2 Slots | Khe M.2 | SSD M.2 và một số thiết bị khác |
| SATA Ports | Cổng SATA | Kết nối HDD/SSD SATA |
| VRM | Mạch cấp nguồn CPU | Cung cấp điện áp ổn định cho CPU |
| BIOS/UEFI | Firmware | Khởi tạo phần cứng và boot hệ điều hành |
| CMOS Battery | Pin CMOS | Duy trì một số thiết lập firmware/clock |
| 24-pin ATX | Nguồn mainboard | Cấp nguồn chính |
| CPU Power | EPS 4/8-pin hoặc tương ứng | Cấp nguồn cho CPU |
| Audio | Âm thanh | Xử lý âm thanh |
| LAN | Mạng | Kết nối Ethernet |
| Rear I/O | I/O phía sau | Kết nối thiết bị bên ngoài |

---

# 🔧 Common Mainboard Tasks

## 🇻🇳

Các công việc thường gặp:

- Lắp ráp máy tính.
- Thay mainboard.
- Nâng cấp CPU.
- Nâng cấp RAM.
- Lắp SSD.
- Lắp GPU.
- Cập nhật BIOS.
- Reset BIOS/CMOS.
- Kiểm tra nguồn.
- Kiểm tra POST.
- Kiểm tra RAM.
- Kiểm tra CPU.
- Kiểm tra khe PCIe.
- Kiểm tra USB.
- Kiểm tra LAN.
- Kiểm tra Audio.
- Chẩn đoán lỗi không POST.
- Chẩn đoán lỗi không nhận thiết bị.

## English

Common motherboard tasks include:

- PC assembly.
- Motherboard replacement.
- CPU upgrade.
- RAM upgrade.
- SSD installation.
- GPU installation.
- BIOS update.
- BIOS/CMOS reset.
- Power testing.
- POST testing.
- RAM testing.
- CPU testing.
- PCIe slot testing.
- USB testing.
- LAN testing.
- Audio testing.
- No-POST troubleshooting.
- Hardware detection troubleshooting.

---

# 📝 Documentation Template

```text
Device:
Motherboard:
Manufacturer:
Model:
Revision:
BIOS Version:

CPU:
RAM:
GPU:
Storage:
PSU:

Physical Condition:

POST Result:

BIOS/UEFI Result:

RAM Test:

Storage Test:

PCIe Test:

USB Test:

LAN Test:

Audio Test:

Temperature:

Detected Problems:

Troubleshooting Actions:

Final Result:

Technician Notes:
```

---

# ⚠️ Safety

## 🇻🇳

Khi làm việc với mainboard:

- Tắt máy hoàn toàn.
- Ngắt nguồn AC.
- Rút dây nguồn.
- Không thao tác khi hệ thống đang cấp điện nếu không cần thiết.
- Sử dụng biện pháp chống tĩnh điện.
- Không chạm tay trực tiếp vào chân socket CPU.
- Không làm cong socket CPU.
- Không ép linh kiện vào khe cắm.
- Kiểm tra đúng chiều trước khi lắp.
- Kiểm tra tài liệu của nhà sản xuất trước khi thay đổi phần cứng.

## English

When working with a motherboard:

- Shut down the computer completely.
- Disconnect AC power.
- Unplug the power cable.
- Avoid working on powered hardware unless required for testing.
- Use appropriate ESD protection.
- Do not touch CPU socket contacts directly.
- Do not bend CPU socket pins.
- Do not force components into slots.
- Verify orientation before installation.
- Check manufacturer documentation before hardware modifications.
