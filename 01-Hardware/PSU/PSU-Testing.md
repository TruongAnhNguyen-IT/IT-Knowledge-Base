# PSU Testing

## 🇻🇳 Tiếng Việt

# 1. Mục tiêu kiểm tra

Mục tiêu của PSU testing:

- Kiểm tra PSU có bật hay không.
- Kiểm tra điện áp đầu ra.
- Kiểm tra connector.
- Kiểm tra cable.
- Kiểm tra dấu hiệu vật lý.
- Xác định PSU có khả năng gây lỗi hệ thống hay không.

---

# 2. Thiết bị cần thiết

Có thể sử dụng:

- PSU Tester
- Digital Multimeter (DMM)
- Paperclip jumper phù hợp cho mục đích test PS_ON khi hiểu rõ pinout
- Spare PSU đã biết hoạt động tốt
- AC power cable
- Load/system để kiểm tra thực tế

### Khuyến nghị

Người mới nên ưu tiên:

```text
PSU Tester
+
Digital Multimeter
+
Known-Good PSU
```

---

# 3. Visual Inspection

Trước khi cấp điện:

Kiểm tra:

- PSU casing
- Fan
- AC socket
- Power switch
- Cable
- Connector
- Bent pins
- Burn marks
- Melted plastic
- Corrosion
- Unusual smell

Nếu phát hiện:

```text
Burning smell
Smoke
Severe melting
Electrical damage
```

Không tiếp tục sử dụng PSU.

---

# 4. Check AC Cable

Kiểm tra:

```text
Wall Outlet
     ↓
AC Cable
     ↓
PSU
```

Kiểm tra:

- Cable có đứt?
- Plug có cháy?
- Connector có lỏng?
- Outlet có điện?
- Power strip có hoạt động?

---

# 5. Check PSU Switch

Một số PSU có:

```text
I = ON
O = OFF
```

Phải đảm bảo switch ở vị trí:

```text
I
```

---

# 6. Paperclip Test

Paperclip test thường được dùng để kiểm tra PSU có phản ứng khi PS_ON# được kích hoạt hay không.

### Mục tiêu

Kiểm tra:

```text
PSU
 ↓
Standby / PS_ON
 ↓
Main output startup
```

### Quan trọng

Paperclip test **không chứng minh PSU hoàn toàn tốt**.

PSU có thể bật nhưng vẫn:

- Sai điện áp
- Ripple cao
- Không ổn định dưới load
- Không đáp ứng tốt khi tải thay đổi

---

# 7. PSU Tester

PSU tester có thể kiểm tra nhanh:

- +12V
- +5V
- +3.3V
- 5VSB
- PG
- Một số connector

### Ưu điểm

- Nhanh
- Dễ sử dụng
- Phù hợp kiểm tra cơ bản

### Hạn chế

Không thay thế được toàn bộ testing chuyên sâu.

---

# 8. Digital Multimeter

DMM cho phép đo điện áp DC.

Các mức cần kiểm tra:

```text
+12V
+5V
+3.3V
+5VSB
```

---

# 9. ATX Voltage Reference

Theo ATX 3.0 Intel:

| Rail | Nominal | Min | Max |
|---|---:|---:|---:|
| +12V | 12.00V | 11.20V | 12.60V |
| +5V | 5.00V | 4.75V | 5.25V |
| +3.3V | 3.30V | 3.14V | 3.47V |
| +5VSB | 5.00V | 4.75V | 5.25V |


---

# 10. Testing Procedure

## Step 1 – Power Off

Tắt PC.

## Step 2 – Disconnect AC

Rút dây nguồn AC nếu thực hiện thao tác tháo/lắp.

## Step 3 – Inspect PSU

Kiểm tra vật lý.

## Step 4 – Check Connectors

Kiểm tra:

- 24-pin
- EPS
- PCIe
- SATA

## Step 5 – Test Standby

Nếu phù hợp với thiết bị đo và quy trình:

Kiểm tra +5VSB.

## Step 6 – Test PSU Startup

Sử dụng phương pháp test phù hợp.

## Step 7 – Measure Outputs

Đo:

```text
+12V
+5V
+3.3V
```

## Step 8 – Test Under Load

Kiểm tra PSU khi hệ thống hoạt động.

## Step 9 – Compare

So sánh với:

- PSU specification
- ATX limits
- Manufacturer data

---

# 11. Testing With Known-Good PSU

Một phương pháp troubleshooting thực tế:

```text
Suspected PSU
      ↓
Replace with Known-Good PSU
      ↓
Run Same Workload
      ↓
Compare Behavior
```

Nếu lỗi biến mất sau khi thay PSU, PSU cũ trở thành một suspect quan trọng.

Tuy nhiên vẫn cần kiểm tra các yếu tố khác trước khi kết luận.

---

# 12. Load Testing

Load testing nhằm kiểm tra PSU trong điều kiện tải.

Ví dụ:

```text
Idle
 ↓
CPU Load
 ↓
GPU Load
 ↓
CPU + GPU Load
```

Theo dõi:

- Shutdown
- Restart
- Black screen
- GPU crash
- Voltage behavior
- System stability
- Temperature

---

# 13. Voltage Drop

Nếu điện áp thay đổi đáng kể khi tải tăng, cần điều tra:

- PSU
- Cable
- Connector
- Load
- Measurement method

Không nên kết luận chỉ dựa vào một phép đo.

---

# 14. Ripple

Ripple là thành phần AC còn lại trên DC output.

Ripple cao có thể ảnh hưởng đến chất lượng nguồn điện.

Đo ripple chính xác thường cần:

- Oscilloscope
- Proper probing
- Appropriate test setup

Multimeter thông thường không phải công cụ đầy đủ để đánh giá ripple.

---

# 15. Testing Checklist

```text
[ ] Visual inspection
[ ] AC cable checked
[ ] PSU switch checked
[ ] Connectors checked
[ ] Modular cable compatibility checked
[ ] 5VSB checked
[ ] +12V checked
[ ] +5V checked
[ ] +3.3V checked
[ ] Load behavior checked
[ ] Known-good PSU comparison
[ ] Results documented
```

---

# 16. Test Documentation

Nên ghi:

```text
Date:
PSU Brand:
PSU Model:
Rated Wattage:
System:
CPU:
GPU:
RAM:
Storage:

Test:
12V:
5V:
3.3V:
5VSB:

Load:
Result:
Symptoms:
Conclusion:
```

---

## 🇬🇧 English

# PSU Testing

## 1. Testing Objectives

PSU testing aims to determine:

- Whether the PSU starts.
- Whether output voltages are present.
- Whether connectors are healthy.
- Whether cables are damaged.
- Whether physical damage exists.
- Whether the PSU may be responsible for system instability.

---

## 2. Tools

Useful tools include:

- PSU tester
- Digital multimeter
- Appropriate PS_ON test method
- Known-good PSU
- AC power cable
- Test system/load

---

## 3. Visual Inspection

Check:

- PSU housing
- Fan
- AC socket
- Power switch
- Cables
- Connectors
- Bent pins
- Burn marks
- Melted plastic
- Corrosion
- Unusual smell

If there is smoke, severe melting, or a burning smell, stop using the PSU.

---

## 4. AC Cable Check

Verify:

```text
Wall Outlet
    ↓
AC Cable
    ↓
PSU
```

Check the outlet, cable, plug, and PSU input.

---

## 5. PSU Switch

Typical switch positions:

```text
I = ON
O = OFF
```

---

## 6. Paperclip Test

A paperclip test can be used to check whether the PSU responds when PS_ON# is activated.

However:

**A successful paperclip test does not prove that the PSU is fully healthy.**

It does not adequately test:

- Voltage regulation
- Ripple
- Load stability
- Transient response

---

## 7. PSU Tester

A PSU tester can quickly check:

- +12V
- +5V
- +3.3V
- 5VSB
- PG
- Selected connectors

It is useful for basic diagnostics but does not replace comprehensive PSU testing.

---

## 8. Digital Multimeter

A DMM can measure DC output voltages such as:

- +12V
- +5V
- +3.3V
- +5VSB

---

## 9. ATX Voltage Reference

Intel's ATX 3.0 documentation specifies:

| Rail | Nominal | Minimum | Maximum |
|---|---:|---:|---:|
| +12V | 12.00V | 11.20V | 12.60V |
| +5V | 5.00V | 4.75V | 5.25V |
| +3.3V | 3.30V | 3.14V | 3.47V |
| +5VSB | 5.00V | 4.75V | 5.25V |


---

## 10. Testing Procedure

```text
Power Off
   ↓
Disconnect AC if required
   ↓
Visual Inspection
   ↓
Check Connectors
   ↓
Check Standby Voltage
   ↓
Test Startup
   ↓
Measure DC Outputs
   ↓
Test Under Load
   ↓
Compare Results
```

---

## 11. Known-Good PSU Test

A practical troubleshooting method is:

```text
Suspected PSU
      ↓
Known-Good PSU
      ↓
Same System
      ↓
Same Workload
      ↓
Compare Results
```

If the problem disappears, the original PSU becomes a strong suspect.

---

## 12. Load Testing

Possible test sequence:

```text
Idle
 ↓
CPU Load
 ↓
GPU Load
 ↓
CPU + GPU Load
```

Monitor:

- Shutdown
- Reboot
- Black screen
- GPU crashes
- Voltage behavior
- System stability
- Temperature

---

## 13. Voltage Drop

Significant voltage changes under load may require investigation of:

- PSU
- Cables
- Connectors
- System load
- Measurement method

---

## 14. Ripple

Ripple is residual AC variation present on a DC output.

Proper ripple measurement generally requires an oscilloscope and an appropriate test setup.

A standard multimeter is not sufficient for comprehensive ripple analysis.

---

## 15. Testing Checklist

```text
[ ] Visual inspection
[ ] AC cable checked
[ ] PSU switch checked
[ ] Connectors checked
[ ] Modular cable compatibility checked
[ ] 5VSB checked
[ ] +12V checked
[ ] +5V checked
[ ] +3.3V checked
[ ] Load behavior checked
[ ] Known-good PSU comparison
[ ] Results documented
```

---

## 16. Test Record

```text
Date:
PSU Brand:
PSU Model:
Rated Wattage:
System:
CPU:
GPU:
RAM:
Storage:

Test:
12V:
5V:
3.3V:
5VSB:

Load:
Result:
Symptoms:
Conclusion:
```
