# CPU Overview / Tổng quan về CPU

## 1. What is a CPU? / CPU là gì?

**Tiếng Việt**

CPU (Central Processing Unit) là bộ xử lý trung tâm của máy tính. CPU thực hiện các lệnh từ hệ điều hành, ứng dụng và các chương trình đang chạy.

CPU có thể thực hiện các nhiệm vụ như:

- Tính toán dữ liệu.
- Thực hiện lệnh của chương trình.
- Điều khiển hoạt động của hệ thống.
- Xử lý dữ liệu từ RAM.
- Giao tiếp với các thiết bị phần cứng khác.

**English**

The CPU (Central Processing Unit) is the primary processor of a computer. It executes instructions from the operating system, applications, and running programs.

Typical CPU tasks include:

- Processing data.
- Executing program instructions.
- Controlling system operations.
- Reading and processing data from RAM.
- Communicating with other hardware components.

---

# 2. CPU Architecture / Kiến trúc CPU

**Tiếng Việt**

Kiến trúc CPU mô tả cách CPU được thiết kế và cách CPU thực hiện các lệnh.

Một số kiến trúc phổ biến:

- x86
- x86-64 / x64
- ARM
- ARM64

**English**

CPU architecture describes how a processor is designed and how it executes instructions.

Common architectures include:

- x86
- x86-64 / x64
- ARM
- ARM64

---

# 3. CPU Core / Nhân CPU

**Tiếng Việt**

Core là một đơn vị xử lý vật lý bên trong CPU.

CPU có nhiều core có thể thực hiện nhiều tác vụ đồng thời.

Ví dụ:

```text
Intel Core i5-10400
6 Cores
12 Threads
```

**English**

A CPU core is a physical processing unit inside a processor.

A multi-core CPU can process multiple tasks concurrently.

---

# 4. CPU Thread / Luồng CPU

**Tiếng Việt**

Thread là một luồng xử lý mà hệ điều hành có thể sử dụng để phân phối công việc cho CPU.

Một CPU có thể có nhiều thread hơn số core nhờ các công nghệ như:

- Intel Hyper-Threading
- AMD SMT (Simultaneous Multithreading)

**English**

A thread is a logical processing unit that the operating system can use to schedule workloads.

A CPU may provide more threads than physical cores through technologies such as:

- Intel Hyper-Threading
- AMD SMT (Simultaneous Multithreading)

---

# 5. CPU Clock Speed / Xung nhịp CPU

## Base Clock / Xung nhịp cơ bản

**Tiếng Việt**

Base Clock là mức xung nhịp cơ bản được CPU sử dụng trong điều kiện hoạt động tiêu chuẩn.

**English**

Base Clock is the processor's rated operating frequency under defined conditions.

---

## Boost Clock / Turbo Clock

**Tiếng Việt**

Boost Clock là mức xung nhịp cao hơn mà CPU có thể đạt được khi điều kiện nhiệt độ, công suất và tải cho phép.

**English**

Boost Clock is a higher operating frequency that the CPU may reach when thermal, power, and workload conditions allow it.

---

# 6. CPU Cache / Bộ nhớ đệm CPU

CPU Cache là bộ nhớ tốc độ cao được sử dụng để lưu trữ dữ liệu và lệnh mà CPU thường xuyên cần.

CPU Cache thường gồm:

### L1 Cache

**Tiếng Việt:** Rất nhanh, dung lượng nhỏ và nằm rất gần các core.

**English:** Very fast, small-capacity cache located very close to the CPU cores.

### L2 Cache

**Tiếng Việt:** Lớn hơn L1 nhưng chậm hơn L1.

**English:** Larger than L1 but generally slower.

### L3 Cache

**Tiếng Việt:** Dung lượng lớn hơn L2 và thường được chia sẻ giữa nhiều core.

**English:** Larger than L2 and commonly shared among multiple CPU cores.

---

# 7. CPU Socket / Socket CPU

**Tiếng Việt**

Socket là giao tiếp vật lý giữa CPU và motherboard.

Ví dụ:

- LGA1200
- LGA1700
- AM4
- AM5

CPU phải sử dụng đúng socket của motherboard.

**English**

A CPU socket is the physical interface between the CPU and motherboard.

Examples include:

- LGA1200
- LGA1700
- AM4
- AM5

The processor must be physically compatible with the motherboard socket.

---

# 8. TDP / Công suất thiết kế nhiệt

**Tiếng Việt**

TDP (Thermal Design Power) là một thông số liên quan đến mức công suất nhiệt mà hệ thống tản nhiệt được thiết kế để xử lý trong các điều kiện xác định.

TDP không nên được hiểu đơn giản là mức điện năng tối đa CPU luôn tiêu thụ.

**English**

TDP (Thermal Design Power) is a thermal design specification indicating the amount of heat a cooling solution is expected to handle under defined conditions.

TDP should not simply be interpreted as the maximum power the CPU always consumes.

---

# 9. Integrated Graphics / GPU tích hợp

Một số CPU có GPU tích hợp (iGPU).

Ví dụ:

```text
Intel Core i5-10400
Integrated Graphics:
Intel UHD Graphics 630
```

Một số CPU không có iGPU.

Ví dụ Intel:

```text
Core i5-10400F
```

Hậu tố `F` thường cho biết CPU không có đồ họa tích hợp.

---

# 10. Memory Support / Hỗ trợ RAM

CPU có bộ điều khiển bộ nhớ và hỗ trợ một số loại RAM nhất định.

Các yếu tố cần kiểm tra:

- DDR4
- DDR5
- Maximum supported memory
- Memory channels
- Supported memory speed

---

# 11. PCI Express Support / Hỗ trợ PCIe

CPU có thể hỗ trợ một phiên bản PCI Express nhất định.

PCIe được sử dụng cho các thiết bị như:

- GPU
- NVMe SSD
- Network Adapter
- Expansion Cards

---

# 12. CPU Specification Example / Ví dụ thông số CPU

## Intel Core i5-10400

| Specification | Information |
|---|---|
| Manufacturer | Intel |
| Product Family | Core i5 |
| Generation | 10th Gen |
| Model | i5-10400 |
| Socket | LGA1200 |
| Cores | 6 |
| Threads | 12 |
| Base Clock | 2.9 GHz |
| Max Turbo | 4.3 GHz |
| Integrated Graphics | Intel UHD Graphics 630 |
| Memory Type | DDR4 |
| Architecture | Comet Lake |

---

# 13. CPU Form Factors / Các dạng CPU

CPU có thể xuất hiện trong:

- Desktop
- Laptop
- Server
- Workstation
- Embedded systems
- Mobile devices

---

# 14. CPU Manufacturers / Nhà sản xuất CPU

Các nhà sản xuất CPU phổ biến:

- Intel
- AMD
- Apple
- Qualcomm
- MediaTek

Đối với PC Windows truyền thống, Intel và AMD là hai nhà sản xuất phổ biến.
