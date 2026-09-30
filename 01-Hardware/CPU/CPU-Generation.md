# CPU Generation Guide / Hướng Dẫn Về Thế Hệ CPU

---

## 1. Introduction / Giới Thiệu
* **EN:** A CPU Generation represents a specific technological cycle in processor design, featuring updates in architecture, microarchitecture, socket compatibility, manufacturing process (nanometers), and instruction sets.
* **VI:** Thế hệ CPU (CPU Generation) đại diện cho một chu kỳ công nghệ trong thiết kế vi xử lý, bao gồm các cải tiến về kiến trúc, vi kiến trúc, socket (chân cắm), tiến trình sản xuất (nm), và tập lệnh xử lý.

---

## 2. Naming Conventions & Decoding / Cách Đọc Mã & Nhận Biết Thế Hệ

### A. Intel Processors / Vi Xử Lý Intel

#### Legacy Scheme (Core i3 / i5 / i7 / i9)
* **Example / Ví dụ:** `Intel Core i7-14700K`
  * **Brand / Thương hiệu:** Intel Core
  * **Modifier / Phân khúc:** i7
  * **Generation / Thế hệ:** **14** (Thế hệ 14 - 14th Gen)
  * **SKU / Mã sản phẩm:** 700
  * **Suffix / Hậu tố:** K (Cho phép ép xung / Unlocked)

#### New Scheme (Core Ultra Series)
* **Example / Ví dụ:** `Intel Core Ultra 7 265K`
  * **Brand / Thương hiệu:** Intel Core Ultra
  * **Tier / Phân cấp:** 7
  * **Series / Thế hệ:** **Series 2** (Arrow Lake)
  * **SKU / Mã sản phẩm:** 65
  * **Suffix / Hậu tố:** K (Unlocked)

---

### B. AMD Processors / Vi Xử Lý AMD

#### Desktop Scheme (Ryzen)
* **Example / Ví dụ:** `AMD Ryzen 7 9800X3D`
  * **Brand / Thương hiệu:** AMD Ryzen
  * **Tier / Phân cấp:** 7
  * **Generation / Thế hệ:** **9** (Series 9000 - Architecture Zen 5)
  * **SKU / Mã sản phẩm:** 800
  * **Suffix / Hậu tố:** X3D (Công nghệ bộ nhớ đệm 3D V-Cache)

---

## 3. Intel CPU Generations Overview / Tổng Quan Các Thế Hệ Intel

| Generation / Thế hệ | Architecture / Kiến trúc | Socket / Chân cắm | Process / Tiến trình | RAM Support / Loại RAM | Key Features / Đặc điểm chính |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Core Ultra Series 2** | Arrow Lake / Lunar Lake | LGA 1851 | TSMC N3B / N4P | DDR5 | Built-in NPU (AI), high power efficiency, no Hyper-Threading on E-cores / Tích hợp NPU AI, tối ưu điện năng. |
| **14th Gen** | Raptor Lake Refresh | LGA 1700 | Intel 7 (10nm) | DDR4 / DDR5 | Increased clock speeds, higher E-core counts / Tăng xung nhịp, bổ sung số lượng nhân tiết kiệm điện. |
| **13th Gen** | Raptor Lake | LGA 1700 | Intel 7 (10nm) | DDR4 / DDR5 | Improved hybrid architecture, larger L2/L3 cache / Tối ưu kiến trúc nhân hỗn hợp (P-core & E-core). |
| **12th Gen** | Alder Lake | LGA 1700 | Intel 7 (10nm) | DDR4 / DDR5 | First performance-hybrid architecture (P+E cores), PCIe 5.0 / Thế hệ đầu tiên áp dụng kiến trúc nhân hỗn hợp. |
| **11th Gen** | Rocket Lake | LGA 1200 | 14nm | DDR4 | Native PCIe 4.0, Xe Graphics / Hỗ trợ chuẩn PCIe 4.0 và đồ họa tích hợp Intel Xe. |
| **10th Gen** | Comet Lake | LGA 1200 | 14nm | DDR4 | Hyper-Threading enabled across all tiers (i3 to i9) / Bổ sung Siêu phân luồng cho tất cả phân khúc. |

---

## 4. AMD CPU Generations Overview / Tổng Quan Các Thế Hệ AMD

| Generation / Thế hệ | Architecture / Kiến trúc | Socket / Chân cắm | Process / Tiến trình | RAM Support / Loại RAM | Key Features / Đặc điểm chính |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Ryzen 9000 Series** | Zen 5 | AM5 | TSMC 4nm / 6nm | DDR5 | +16% IPC improvement, Full AVX-512 support / Cải thiện 16% hiệu suất IPC, hỗ trợ AVX-512 full-width. |
| **Ryzen 8000 Series** | Zen 4 (Hawk Point) | AM5 | TSMC 4nm | DDR5 | APU with strong RDNA 3 graphics and XDNA NPU / Tích hợp GPU RDNA 3 mạnh mẽ và nhân NPU AI. |
| **Ryzen 7000 Series** | Zen 4 | AM5 | TSMC 5nm / 6nm | DDR5 | Native PCIe 5.0, EXPO RAM profiles, LGA socket transition / Chuyển sang socket LGA AM5, hỗ trợ DDR5. |
| **Ryzen 5000 Series** | Zen 3 | AM4 | TSMC 7nm | DDR4 | Unified L3 cache, introduced 3D V-Cache technology / Unified L3 Cache giúp tăng mạnh hiệu năng chơi game. |
| **Ryzen 3000 Series** | Zen 2 | AM4 | TSMC 7nm | DDR4 | Chiplet design architecture, PCIe 4.0 support / Tách rời thiết kế Chiplet, hỗ trợ PCIe 4.0. |

---

## 5. Notes & Best Practices / Lưu Ý Quan Trọng

### EN:
1. **Socket Compatibility:** A newer CPU generation often requires a motherboard with a matching socket (e.g., Intel LGA1700 vs LGA1851, AMD AM4 vs AM5).
2. **BIOS Updates:** Using a newer generation CPU on an older compatible motherboard chipset almost always requires updating the BIOS beforehand.
3. **Memory Standard:** Pay attention to RAM type requirements (DDR4 vs DDR5) when matching CPU generations with motherboard platforms.

### VI:
1. **Độ tương thích Socket:** Thế hệ CPU mới hơn thường đi kèm với socket mới (Ví dụ: Intel LGA1700 chuyển sang LGA1851, AMD AM4 chuyển sang AM5).
2. **Cập nhật BIOS:** Khi lắp CPU thế hệ mới lên các bo mạch chủ dòng cũ có hỗ trợ tương thích, bạn bắt buộc phải cập nhật BIOS trước khi lắp đặt.
3. **Chuẩn RAM:** Chú ý chuẩn RAM tương thích (DDR4 hay DDR5) khi lựa chọn thế hệ CPU và mainboard tương ứng.
