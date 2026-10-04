
# Storage Health

## 🇻🇳 Tiếng Việt

## 1. Mục đích

Storage Health dùng để đánh giá tình trạng hoạt động của:

- HDD
- SATA SSD
- NVMe SSD

Các nguồn thông tin:

- SMART
- NVMe Health Information
- Temperature
- Error counters
- Power-on hours
- Host writes
- Bad sectors
- Percentage used
- Performance behavior

---

## 2. SMART

SMART = Self-Monitoring, Analysis and Reporting Technology.

SMART giúp storage và hệ thống theo dõi các thông số liên quan đến sức khỏe drive.

SMART không phải là một chỉ số duy nhất.

Một ổ có thể báo "Good" nhưng vẫn cần backup nếu có:

- I/O errors
- File corruption
- Abnormal noise
- Increasing error counts
- Unstable behavior

---

## 3. HDD Health Attributes

Một số attribute thường gặp:

### Reallocated Sector Count

Số sector đã được remap sang vùng dự phòng.

Nếu tăng liên tục:

> Cần theo dõi và chuẩn bị thay ổ.

### Current Pending Sector

Sector đang bị nghi ngờ có vấn đề.

### Offline Uncorrectable

Sector không thể sửa/đọc chính xác.

### Power-On Hours

Tổng thời gian ổ đã hoạt động.

### Power Cycle Count

Số lần drive được bật/tắt.

### Temperature

Nhiệt độ drive.

---

## 4. SATA SSD Health

Có thể theo dõi:

- Percentage Used
- Available Reserved Space
- Total Host Writes
- Total Host Reads
- Media Errors
- Temperature
- Power-on Hours
- Power Cycle Count

Tên và ý nghĩa chính xác của attribute có thể thay đổi theo manufacturer/model.

---

## 5. NVMe Health

Các trường thường gặp:

- Critical Warning
- Composite Temperature
- Available Spare
- Available Spare Threshold
- Percentage Used
- Data Units Read
- Data Units Written
- Host Read Commands
- Host Write Commands
- Controller Busy Time
- Power Cycles
- Power-on Hours
- Unsafe Shutdowns
- Media and Data Integrity Errors
- Error Information Log Entries

---

## 6. Percentage Used

Percentage Used là chỉ số liên quan đến mức độ endurance đã sử dụng của NVMe.

Ví dụ:

> Percentage Used = 20%

Không có nghĩa SSD đã mất 20% dung lượng lưu trữ.

Nó liên quan đến endurance estimate theo chuẩn/firmware của drive.

---

## 7. TBW

TBW = Terabytes Written.

Dùng để đánh giá endurance của SSD.

Không nên coi TBW là "ngày hết hạn".

SSD có thể:

- Vượt TBW và vẫn hoạt động.
- Có lỗi trước TBW.
- Phụ thuộc workload và điều kiện vận hành.

---

## 8. Temperature

Theo dõi nhiệt độ đặc biệt quan trọng đối với:

- NVMe SSD
- High-performance SSD
- SSD nằm dưới GPU
- Laptop storage

Nhiệt độ cao có thể dẫn tới thermal throttling.

---

## 9. Health Status

Có thể phân loại nội bộ:

### Good

Không phát hiện cảnh báo đáng kể.

### Warning

Có chỉ số cần theo dõi.

### Critical

Có lỗi nghiêm trọng hoặc dấu hiệu failure.

### Failed

Drive không còn đáng tin cậy cho production use.

Không nên chỉ dựa vào màu xanh/vàng/đỏ của một phần mềm.

---

## 10. Health Assessment

Đánh giá storage dựa trên nhiều yếu tố:

1. SMART.
2. Temperature.
3. Error count.
4. Performance.
5. System symptoms.
6. File integrity.
7. Age.
8. Workload.
9. Power events.
10. Manufacturer documentation.

---

## 11. Khi phát hiện ổ có dấu hiệu lỗi

Ưu tiên:

1. Ngừng workload không cần thiết.
2. Backup dữ liệu.
3. Clone nếu cần.
4. Không benchmark liên tục.
5. Ghi nhận SMART.
6. Kiểm tra cable/slot.
7. Thay drive nếu cần.
8. Verify backup.

---

## 12. Nguyên tắc quan trọng

> SMART là công cụ hỗ trợ chẩn đoán, không phải bảo hiểm dữ liệu.

Backup vẫn là biện pháp bảo vệ dữ liệu quan trọng nhất.

---

# 🇬🇧 English

## 1. Purpose

Storage Health evaluates:

- HDD
- SATA SSD
- NVMe SSD

Important health sources include:

- SMART
- NVMe health information
- Temperature
- Error counters
- Power-on hours
- Host writes
- Bad sectors
- Percentage used
- Performance behavior

---

## 2. SMART

SMART stands for Self-Monitoring, Analysis and Reporting Technology.

It provides diagnostic information about a storage device.

SMART is not a single universal health score.

A drive may report "Good" while still showing:

- I/O errors
- File corruption
- Abnormal noises
- Increasing error counts
- Unstable behavior

---

## 3. HDD Health

Common HDD indicators:

- Reallocated sectors
- Pending sectors
- Uncorrectable sectors
- Power-on hours
- Power-cycle count
- Temperature

Increasing bad-sector-related counters should be treated seriously.

---

## 4. SATA SSD Health

Common indicators:

- Percentage used
- Available reserve
- Host writes
- Host reads
- Media errors
- Temperature
- Power-on hours
- Power cycles

Exact SMART definitions vary by drive model.

---

## 5. NVMe Health

Common fields:

- Critical warning
- Composite temperature
- Available spare
- Available spare threshold
- Percentage used
- Data units read
- Data units written
- Host read commands
- Host write commands
- Controller busy time
- Power cycles
- Power-on hours
- Unsafe shutdowns
- Media and data integrity errors
- Error information log entries

---

## 6. Percentage Used

Percentage Used is related to estimated endurance consumption.

For example:

> Percentage Used = 20%

does not mean that 20% of the physical storage capacity has disappeared.

---

## 7. TBW

TBW means Terabytes Written.

It is an endurance metric.

It should not be treated as an exact expiration point.

---

## 8. Temperature

Temperature is especially important for:

- NVMe SSDs
- High-performance SSDs
- SSDs located beneath GPUs
- Laptop SSDs

Excessive temperature can cause thermal throttling.

---

## 9. Health Classification

### Good

No significant warning detected.

### Warning

One or more values require monitoring.

### Critical

Serious errors or failure indicators are present.

### Failed

The drive should no longer be considered reliable for normal production use.

---

## 10. Health Assessment

Evaluate multiple factors:

1. SMART.
2. Temperature.
3. Error counters.
4. Performance.
5. System symptoms.
6. File integrity.
7. Drive age.
8. Workload.
9. Power events.
10. Manufacturer documentation.

---

## 11. If a Drive Shows Failure Symptoms

Priority:

1. Reduce unnecessary workload.
2. Back up data.
3. Clone the drive if appropriate.
4. Avoid unnecessary stress testing.
5. Record health information.
6. Check cables and slots.
7. Replace the drive if necessary.
8. Verify the backup.

---

## 12. Key Principle

> SMART is a diagnostic tool, not a backup strategy.

Important data should always have a separate backup.
