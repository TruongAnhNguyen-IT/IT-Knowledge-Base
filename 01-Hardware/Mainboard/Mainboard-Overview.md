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

A
