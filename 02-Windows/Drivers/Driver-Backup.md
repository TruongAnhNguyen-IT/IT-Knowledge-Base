
# Driver Backup – Sao lưu Driver

## 1. Purpose – Mục đích

**Tiếng Việt**

Sao lưu driver giúp chuẩn bị phương án khôi phục khi cài lại Windows, thay đổi cấu hình hệ thống hoặc xử lý sự cố. Bản sao lưu có thể giúp giảm thời gian tìm kiếm driver, nhưng không thay thế hoàn toàn bộ cài đặt chính thức của nhà sản xuất.

**English**

Driver backup helps prepare for Windows reinstallation, system changes, and troubleshooting. A backup can reduce the time required to locate drivers, but it does not completely replace the manufacturer's original installation packages.

## 2. When to Back Up – Khi nào cần sao lưu?

- Before reinstalling Windows.
- Before performing major system changes.
- Before replacing a storage device.
- Before updating critical drivers.
- When preparing a recovery toolkit for IT support.

Tiếng Việt:

- Trước khi cài lại Windows.
- Trước khi thay đổi lớn đối với hệ thống.
- Trước khi thay thiết bị lưu trữ.
- Trước khi cập nhật driver quan trọng.
- Khi chuẩn bị bộ công cụ khôi phục cho IT Support.

## 3. Method 1: Export Drivers with PnPUtil

### Step 1: Prepare a backup folder

Open Command Prompt as Administrator:

```cmd
mkdir C:\DriverBackup
```

### Step 2: Export driver packages

```cmd
pnputil /export-driver * C:\DriverBackup
```

The command exports eligible third-party driver packages from the Windows Driver Store to the specified folder.

Tiếng Việt:

Lệnh trên xuất các gói driver bên thứ ba đủ điều kiện từ Driver Store của Windows sang thư mục `C:\DriverBackup`.

Lưu ý:
- Đây không phải bản sao lưu toàn bộ hệ điều hành.
- Không phải mọi driver tích hợp sẵn của Microsoft đều được xuất như một gói độc lập.
- Các ứng dụng cài đặt, tiện ích đi kèm và firmware không nhất thiết được sao lưu.
- Kiểm tra thông báo kết quả của lệnh để xác định thao tác có thành công hay không.

## 4. Method 2: Export Drivers with PowerShell

Run PowerShell as Administrator:

```powershell
Export-WindowsDriver `
    -Online `
    -Destination "C:\DriverBackup"
```

English: This command exports third-party driver packages from the running Windows installation to the destination folder.

Tiếng Việt: Lệnh xuất các gói driver bên thứ ba từ hệ điều hành Windows đang chạy sang thư mục chỉ định.

## 5. Verify the Backup – Kiểm tra bản sao lưu

1. Open `C:\DriverBackup`.
2. Confirm that driver folders and package files exist.
3. Check for INF, SYS, CAT, and related files where applicable.
4. Record the computer model and Windows version.
5. Copy the backup to a separate storage device if needed.
6. Test the recovery procedure on a suitable test system when possible.

Tiếng Việt:

1. Mở thư mục `C:\DriverBackup`.
2. Kiểm tra các thư mục và file driver.
3. Kiểm tra các file INF, SYS, CAT và file liên quan nếu có.
4. Ghi lại model máy và phiên bản Windows.
5. Sao chép bản backup sang thiết bị lưu trữ khác nếu cần.
6. Kiểm tra quy trình khôi phục trên hệ thống thử nghiệm phù hợp nếu có thể.

## 6. Restore Drivers – Khôi phục Driver

For a trusted backup containing compatible INF packages, use Device Manager or PnPUtil.

Example:

```cmd
pnputil /add-driver "D:\DriverBackup\*.inf" /subdirs /install
```

Tiếng Việt:

- Thay `D:\DriverBackup` bằng đường dẫn bản sao lưu thực tế.
- Chỉ sử dụng gói driver phù hợp với thiết bị và Windows.
- Kiểm tra thông báo của PnPUtil sau khi chạy.
- Mở Device Manager để xác nhận kết quả.

English:

- Replace `D:\DriverBackup` with the actual backup path.
- Use only packages compatible with the target device and Windows.
- Review the PnPUtil output.
- Verify the result in Device Manager.

Note: Importing packages does not guarantee that every package will be selected as the active driver. Some devices may require the original vendor installer.

## 7. Recommended Backup Structure – Cấu trúc sao lưu đề xuất

```text
DriverBackup/
├── Network/
├── Graphics/
├── Audio/
├── Chipset/
├── Storage/
├── Bluetooth/
└── README.txt
```

These folders are organizational examples. PnPUtil may export packages into folders named according to their published driver identifiers.

Các thư mục trên chỉ nhằm mục đích tổ chức. PnPUtil có thể tạo thư mục theo tên hoặc mã gói driver được xuất bản trong hệ thống.

## 8. Backup Checklist – Checklist sao lưu

- [ ] Backup command completed successfully.
- [ ] Backup files are present.
- [ ] Computer model is documented.
- [ ] Windows version and architecture are documented.
- [ ] Backup is stored in a safe location.
- [ ] Recovery procedure is documented.

## 9. References – Tài liệu tham khảo

- Microsoft Learn: https://learn.microsoft.com/
- PnPUtil command reference: https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/pnputil-command-syntax
- Export-WindowsDriver: https://learn.microsoft.com/en-us/powershell/module/dism/export-windowsdriver
