# Windows Post-Installation – Windows Post-Installation Configuration Guide

## 1. Purpose – Mục đích

### English

This document provides a standardized procedure for verifying, configuring, securing, and testing Windows after a clean installation or reinstallation.

The objective is to ensure that the computer is stable, properly configured, updated, secure, and ready for personal or business use.

This procedure is intended for IT Support technicians, Helpdesk personnel, and junior system administrators.

### Tiếng Việt

Tài liệu cung cấp quy trình chuẩn để kiểm tra, cấu hình, bảo mật và thử nghiệm Windows sau khi cài mới hoặc cài đặt lại.

Mục tiêu là đảm bảo máy tính hoạt động ổn định, được cấu hình đúng, cập nhật đầy đủ theo yêu cầu, an toàn và sẵn sàng phục vụ công việc cá nhân hoặc doanh nghiệp.

Quy trình dành cho kỹ thuật viên IT Support, nhân viên Helpdesk và quản trị viên hệ thống cấp độ cơ bản.

---

## 2. Post-Installation Checklist – Checklist sau cài đặt

### English

- [ ] Complete the initial Windows setup.
- [ ] Verify Windows edition, version, and system architecture.
- [ ] Check activation and licensing status.
- [ ] Verify firmware boot mode and system disk partition style.
- [ ] Install required device drivers.
- [ ] Run Windows Update according to policy.
- [ ] Verify network connectivity and IP configuration.
- [ ] Configure user accounts and access permissions.
- [ ] Review Windows Security, Firewall, and device encryption.
- [ ] Install approved applications.
- [ ] Test hardware and peripherals.
- [ ] Restore required user data.
- [ ] Verify backup and recovery arrangements where applicable.
- [ ] Document the final configuration.
- [ ] Obtain user confirmation before closing the support task.

### Tiếng Việt

- [ ] Hoàn tất thiết lập Windows ban đầu.
- [ ] Xác minh edition, phiên bản và kiến trúc hệ thống.
- [ ] Kiểm tra kích hoạt và bản quyền.
- [ ] Kiểm tra chế độ boot firmware và kiểu phân vùng ổ đĩa hệ thống.
- [ ] Cài đặt driver cần thiết.
- [ ] Chạy Windows Update theo chính sách.
- [ ] Kiểm tra kết nối mạng và cấu hình IP.
- [ ] Cấu hình tài khoản và quyền truy cập.
- [ ] Kiểm tra Windows Security, Firewall và mã hóa thiết bị.
- [ ] Cài phần mềm được phê duyệt.
- [ ] Kiểm tra phần cứng và thiết bị ngoại vi.
- [ ] Khôi phục dữ liệu cần thiết.
- [ ] Xác minh phương án sao lưu và phục hồi khi phù hợp.
- [ ] Ghi nhận cấu hình cuối cùng.
- [ ] Xác nhận với người dùng trước khi đóng yêu cầu hỗ trợ.

---

## 3. Step 1: Verify Windows Edition and Version – Kiểm tra edition và phiên bản Windows

### English

1. Open Settings.
2. Navigate to System > About.
3. Record the Windows edition, version, OS build, and system type.
4. Confirm that the installed edition matches the device's license and organizational requirements.
5. Check that the Windows version remains supported for the intended use.

Run the following command to open the Windows version dialog:

```cmd
winver
```

To retrieve additional operating system information, open PowerShell:

```powershell
Get-ComputerInfo |
    Select-Object WindowsProductName, WindowsVersion, OsBuildNumber, OsArchitecture
```

### Tiếng Việt

1. Mở Settings.
2. Truy cập System > About.
3. Ghi lại edition, phiên bản, OS build và kiến trúc hệ thống.
4. Xác nhận edition đã cài phù hợp với giấy phép và yêu cầu của tổ chức.
5. Kiểm tra phiên bản Windows còn được hỗ trợ cho mục đích sử dụng hay không.

Lệnh `winver` mở cửa sổ thông tin phiên bản Windows.

Lệnh PowerShell cung cấp thêm thông tin hệ điều hành, hữu ích khi ghi nhận cấu hình máy.

**Note:** Windows edition, version, build, and architecture are different attributes. Do not use them interchangeably.

**Lưu ý:** Edition, version, build và architecture là các thuộc tính khác nhau, không được sử dụng thay thế cho nhau.

---

## 4. Step 2: Verify Firmware Mode and Partition Style – Kiểm tra chế độ boot và kiểu phân vùng

### English

Verify the current boot mode:

1. Press `Win + R`.
2. Enter `msinfo32`.
3. Check the BIOS Mode field.

Inspect physical disks using PowerShell:

```powershell
Get-Disk |
    Select-Object Number, FriendlyName, PartitionStyle, OperationalStatus, Size |
    Format-Table -AutoSize
```

For a standard Windows installation booted in UEFI mode, the Windows system disk should use GPT.

### Tiếng Việt

Kiểm tra chế độ boot hiện tại:

1. Nhấn `Win + R`.
2. Nhập `msinfo32`.
3. Kiểm tra mục BIOS Mode.

Sử dụng PowerShell để kiểm tra ổ đĩa vật lý, kiểu phân vùng, trạng thái và dung lượng.

Đối với cài đặt Windows thông thường khởi động theo UEFI, ổ đĩa hệ thống Windows phải sử dụng GPT.

Do not change firmware settings or partition schemes if the system is already working correctly and there is no documented requirement to do so.

Không thay đổi firmware hoặc kiểu phân vùng nếu hệ thống đang hoạt động bình thường và không có yêu cầu kỹ thuật cụ thể.

---

## 5. Step 3: Install and Verify Drivers – Cài đặt và kiểm tra driver

### 5.1 Recommended driver sources – Nguồn driver khuyến nghị

Use the following sources in order of preference:

1. Windows Update for applicable drivers.
2. The computer manufacturer's official support page.
3. The component manufacturer's official website when appropriate.
4. An organization's approved driver repository.

Tiếng Việt:

Ưu tiên Windows Update, trang hỗ trợ chính thức của hãng máy tính, website chính thức của nhà sản xuất linh kiện khi phù hợp và kho driver đã được doanh nghiệp phê duyệt.

Avoid unknown driver-download websites and unofficial driver-pack tools.

Tránh website tải driver không rõ nguồn gốc và các công cụ cài hàng loạt driver không đáng tin cậy.

### 5.2 Typical driver checklist – Checklist driver

| Driver | Purpose / Chức năng |
|---|---|
| Chipset | Supports platform devices and system controllers. / Hỗ trợ thiết bị nền tảng và bộ điều khiển hệ thống. |
| Storage controller | Supports storage devices and controller features when required. / Hỗ trợ ổ lưu trữ và tính năng bộ điều khiển khi cần. |
| Ethernet | Enables wired network connectivity. / Hỗ trợ mạng có dây. |
| Wi-Fi | Enables wireless network connectivity. / Hỗ trợ mạng không dây. |
| Graphics | Supports display resolution, acceleration, and graphics functions. / Hỗ trợ độ phân giải, tăng tốc và chức năng đồ họa. |
| Audio | Enables audio devices and related features. / Hỗ trợ thiết bị âm thanh. |
| Bluetooth | Enables supported Bluetooth devices. / Hỗ trợ thiết bị Bluetooth. |
| Touchpad and input | Enables laptop input features. / Hỗ trợ touchpad và thiết bị nhập liệu trên laptop. |
| Printer and peripherals | Supports required external devices. / Hỗ trợ máy in và thiết bị ngoại vi. |

### 5.3 Verify Device Manager – Kiểm tra Device Manager

1. Right-click Start.
2. Open Device Manager.
3. Review devices for warning icons.
4. Inspect unknown devices and devices with errors.
5. Install the correct driver where required.
6. Restart if requested and verify again.

Tiếng Việt:

1. Nhấp phải Start.
2. Mở Device Manager.
3. Kiểm tra thiết bị có biểu tượng cảnh báo.
4. Xem xét thiết bị không xác định và thiết bị có lỗi.
5. Cài driver phù hợp khi cần.
6. Khởi động lại nếu được yêu cầu và kiểm tra lại.

**Important:** A warning icon is a reason to investigate, not proof that a driver is the only possible cause. Check the device status and error code.

**Quan trọng:** Biểu tượng cảnh báo là dấu hiệu cần kiểm tra, không chứng minh driver là nguyên nhân duy nhất. Cần xem trạng thái thiết bị và mã lỗi.

---

## 6. Step 4: Run Windows Update – Cập nhật Windows

### English

1. Open Settings.
2. Navigate to Windows Update.
3. Select Check for updates.
4. Install applicable security, quality, and feature updates according to the device's update policy.
5. Review optional updates when a specific driver or feature is needed.
6. Restart when required.
7. Check again after restarting.
8. Confirm that no required updates remain pending.

For managed business devices, follow the organization's approved update schedule and deployment controls.

### Tiếng Việt

1. Mở Settings.
2. Truy cập Windows Update.
3. Chọn Check for updates.
4. Cài đặt các bản cập nhật bảo mật, chất lượng và tính năng phù hợp với chính sách của máy.
5. Kiểm tra Optional updates khi cần một driver hoặc tính năng cụ thể.
6. Khởi động lại khi được yêu cầu.
7. Kiểm tra lại sau khi khởi động.
8. Xác nhận không còn bản cập nhật bắt buộc đang chờ.

Với máy tính doanh nghiệp, tuân thủ lịch cập nhật và quy trình triển khai của tổ chức.

**Note:** Do not install optional drivers indiscriminately. Verify compatibility and business requirements before deployment.

**Lưu ý:** Không cài tất cả driver tùy chọn một cách máy móc. Cần xác minh khả năng tương thích và nhu cầu sử dụng.

---

## 7. Step 5: Verify Network Connectivity – Kiểm tra kết nối mạng

### 7.1 Inspect IP configuration – Kiểm tra cấu hình IP

Run Command Prompt:

```cmd
ipconfig /all
```

Check:

- Network adapter status.
- IPv4 or IPv6 address as applicable.
- Subnet mask or prefix information.
- Default gateway.
- DNS servers.
- DHCP status where applicable.

Tiếng Việt:

Kiểm tra trạng thái card mạng, địa chỉ IPv4/IPv6, subnet mask hoặc prefix, default gateway, DNS server và trạng thái DHCP nếu áp dụng.

### 7.2 Test network connectivity – Kiểm tra kết nối

Test the local TCP/IP stack:

```cmd
ping 127.0.0.1
```

Check the local gateway:

```cmd
ping <default-gateway>
```

Replace `<default-gateway>` with the actual gateway address.

Test DNS resolution:

```cmd
nslookup microsoft.com
```

Test HTTPS connectivity when PowerShell is available:

```powershell
Test-NetConnection www.microsoft.com -Port 443
```

### Tiếng Việt

- `ping 127.0.0.1`: kiểm tra TCP/IP loopback trên máy.
- `ping <default-gateway>`: kiểm tra khả năng liên lạc với gateway nếu ICMP được cho phép.
- `nslookup microsoft.com`: kiểm tra phân giải DNS.
- `Test-NetConnection ... -Port 443`: kiểm tra kết nối TCP đến cổng HTTPS.

A failed ping alone does not prove that a device is offline because ICMP may be blocked.

Ping thất bại không đủ để kết luận thiết bị mất kết nối vì ICMP có thể bị chặn.

### 7.3 Basic network troubleshooting – Xử lý sự cố mạng cơ bản

If network connectivity fails:

1. Check the physical cable or Wi-Fi connection.
2. Verify that the correct network adapter is enabled.
3. Check the IP address, subnet mask, gateway, and DNS configuration.
4. Determine whether the device uses DHCP or a static IP.
5. Check for IP address conflicts where relevant.
6. Test connectivity to the gateway and DNS server.
7. Review proxy, VPN, firewall, and organizational network requirements.

Tiếng Việt:

Nếu mạng không hoạt động, kiểm tra cáp hoặc Wi-Fi, trạng thái card mạng, cấu hình IP/DNS, DHCP hoặc IP tĩnh, xung đột IP nếu có, khả năng liên lạc với gateway/DNS và các cấu hình proxy, VPN, firewall hoặc mạng doanh nghiệp.

Do not assign an arbitrary static IP address on a managed network.

Không tự ý đặt IP tĩnh bất kỳ trên mạng doanh nghiệp đang được quản lý.

---

## 8. Step 6: Configure User Accounts and Permissions – Cấu hình tài khoản và quyền truy cập

### English

- Confirm whether the device uses a local account, Microsoft account, domain account, or organization-managed identity.
- Create or configure the required user account.
- Apply the principle of least privilege.
- Avoid using an administrator account for routine work when practical.
- Configure supported sign-in and recovery methods.
- Follow organizational password, identity, and access policies.
- Confirm that the user can sign in and access required resources.

### Tiếng Việt

- Xác định máy sử dụng tài khoản local, Microsoft account, domain account hay tài khoản được tổ chức quản lý.
- Tạo hoặc cấu hình tài khoản cần thiết.
- Áp dụng nguyên tắc quyền tối thiểu.
- Hạn chế dùng tài khoản Administrator cho công việc thông thường khi có thể.
- Cấu hình phương thức đăng nhập và khôi phục được hỗ trợ.
- Tuân thủ chính sách mật khẩu, danh tính và quyền truy cập của tổ chức.
- Xác nhận người dùng đăng nhập được và truy cập các tài nguyên cần thiết.

### Account security – Bảo mật tài khoản

Never share administrator passwords unnecessarily. Store credentials only through approved secure mechanisms.

Không chia sẻ mật khẩu quản trị khi không cần thiết. Chỉ lưu thông tin xác thực thông qua phương thức bảo mật được phê duyệt.

For domain-joined or managed computers, use the approved enrollment and identity-management process.

Với máy gia nhập domain hoặc được quản lý tập trung, sử dụng quy trình triển khai và quản lý danh tính đã được phê duyệt.

---

## 9. Step 7: Review Windows Security – Kiểm tra bảo mật Windows

### 9.1 Security checklist – Checklist bảo mật

- [ ] Microsoft Defender status is reviewed.
- [ ] Firewall status is reviewed.
- [ ] Windows Security notifications are checked.
- [ ] Security updates are installed according to policy.
- [ ] Device encryption or BitLocker status is checked.
- [ ] Recovery-key availability is verified when encryption is enabled.
- [ ] Unnecessary applications and services are reviewed.
- [ ] Organizational security policies are applied where applicable.

### Tiếng Việt

- [ ] Kiểm tra trạng thái Microsoft Defender.
- [ ] Kiểm tra Windows Firewall.
- [ ] Kiểm tra thông báo Windows Security.
- [ ] Cài đặt cập nhật bảo mật theo chính sách.
- [ ] Kiểm tra trạng thái Device Encryption hoặc BitLocker.
- [ ] Xác minh khóa khôi phục khi bật mã hóa.
- [ ] Rà soát ứng dụng và dịch vụ không cần thiết.
- [ ] Áp dụng chính sách bảo mật doanh nghiệp khi cần.

### 9.2 Check Defender and Firewall – Kiểm tra Defender và Firewall

Open Windows Security from the Start menu.

Review:

- Virus & threat protection.
- Firewall & network protection.
- App & browser control.
- Device security.
- Device encryption where available.

Tiếng Việt:

Mở Windows Security từ Start và kiểm tra các mục bảo vệ chống virus, firewall, kiểm soát ứng dụng và trình duyệt, bảo mật thiết bị và mã hóa thiết bị nếu có.

For a basic PowerShell check on supported Windows editions, run:

```powershell
Get-MpComputerStatus |
    Select-Object AntivirusEnabled, RealTimeProtectionEnabled, AntivirusSignatureLastUpdated
```

This command checks selected Microsoft Defender status fields. It does not prove that every security control is correctly configured.

Lệnh này kiểm tra một số trạng thái Microsoft Defender. Nó không chứng minh tất cả cơ chế bảo mật đều được cấu hình đúng.

### 9.3 Check BitLocker – Kiểm tra BitLocker

Run:

```cmd
manage-bde -status
```

Review the protection status and encryption status for relevant volumes.

Kiểm tra trạng thái bảo vệ và mã hóa của các volume liên quan.

Do not enable, disable, or modify encryption without understanding the recovery implications. Confirm that recovery information is safely available before changing firmware or TPM settings.

Không bật, tắt hoặc thay đổi mã hóa khi chưa hiểu các ảnh hưởng đến khôi phục. Xác nhận thông tin khôi phục được lưu giữ an toàn trước khi thay đổi firmware hoặc TPM.

---

## 10. Step 8: Check Windows Activation – Kiểm tra kích hoạt Windows

### English

1. Open Settings.
2. Navigate to System > Activation.
3. Review the activation status.
4. Confirm that the installed edition matches the intended license.
5. Follow the organization's licensing process if activation fails.

For additional licensing information, run:

```cmd
slmgr /xpr
```

This command displays the activation expiration information reported by Windows licensing.

### Tiếng Việt

1. Mở Settings.
2. Truy cập System > Activation.
3. Kiểm tra trạng thái kích hoạt.
4. Xác nhận edition đã cài phù hợp với giấy phép.
5. Thực hiện theo quy trình cấp phép của tổ chức nếu kích hoạt thất bại.

Lệnh `slmgr /xpr` hiển thị thông tin hết hạn kích hoạt theo cơ chế cấp phép Windows.

**Note:** Activation status and license entitlement are related but not identical concepts. Follow the applicable Microsoft licensing terms and organizational policy.

**Lưu ý:** Trạng thái kích hoạt và quyền sử dụng giấy phép có liên quan nhưng không hoàn toàn đồng nhất. Cần tuân thủ điều khoản cấp phép Microsoft và chính sách tổ chức.

---

## 11. Step 9: Install Required Applications – Cài đặt phần mềm cần thiết

### English

Install only applications required by the user or organization.

Common examples include:

- Approved web browsers.
- Office or productivity applications.
- PDF readers.
- File compression utilities.
- Approved remote-support tools.
- Business applications.
- Printer and peripheral utilities.
- VPN clients or other approved connectivity software.

Download applications from official vendor sources or the organization's software repository.

### Tiếng Việt

Chỉ cài phần mềm cần thiết cho người dùng hoặc tổ chức.

Các ví dụ thường gặp gồm trình duyệt được phê duyệt, phần mềm văn phòng, trình đọc PDF, công cụ nén file, phần mềm hỗ trợ từ xa được phê duyệt, ứng dụng nghiệp vụ, tiện ích máy in, VPN client và phần mềm kết nối cần thiết.

Tải phần mềm từ website chính thức của nhà cung cấp hoặc kho phần mềm nội bộ.

### Application verification – Kiểm tra ứng dụng

- Confirm that installation completes successfully.
- Open the application and test basic functionality.
- Check licensing and activation where applicable.
- Confirm that required updates are installed.
- Remove temporary installers when no longer needed and permitted by policy.

Tiếng Việt:

Xác nhận cài đặt thành công, mở thử ứng dụng, kiểm tra bản quyền nếu có, cập nhật cần thiết và xóa bộ cài tạm khi không còn sử dụng nếu chính sách cho phép.

---

## 12. Step 10: Test Hardware and Peripherals – Kiểm tra phần cứng và thiết bị ngoại vi

| Component | Verification procedure |
|---|---|
| CPU and RAM | Check system information and confirm expected capacity. |
| Storage | Confirm disk visibility, capacity, and available health indicators. |
| Display | Check resolution, scaling, refresh rate, and stability. |
| Ethernet | Test wired network connectivity. |
| Wi-Fi | Test wireless connectivity and signal stability. |
| Audio | Test speakers, headphones, and microphone. |
| Webcam | Test camera access where applicable. |
| Bluetooth | Test a compatible peripheral where required. |
| USB ports | Test with a known-good device. |
| Printer | Install the correct driver and print a test page if applicable. |
| Keyboard and mouse | Verify input and basic functions. |
| Sleep and restart | Confirm expected power and restart behavior. |

### Tiếng Việt

| Thành phần | Quy trình kiểm tra |
|---|---|
| CPU và RAM | Kiểm tra thông tin hệ thống và dung lượng nhận diện. |
| Ổ lưu trữ | Kiểm tra khả năng nhận diện, dung lượng và thông tin sức khỏe ổ đĩa nếu có. |
| Màn hình | Kiểm tra độ phân giải, scaling, tần số quét và độ ổn định. |
| Ethernet | Kiểm tra mạng có dây. |
| Wi-Fi | Kiểm tra kết nối không dây và độ ổn định tín hiệu. |
| Âm thanh | Kiểm tra loa, tai nghe và micro. |
| Webcam | Kiểm tra camera nếu có. |
| Bluetooth | Kiểm tra thiết bị ngoại vi tương thích khi cần. |
| Cổng USB | Thử bằng thiết bị đã xác nhận hoạt động tốt. |
| Máy in | Cài driver đúng và in trang thử nếu áp dụng. |
| Bàn phím và chuột | Kiểm tra nhập liệu và chức năng cơ bản. |
| Sleep và restart | Kiểm tra chế độ nguồn và khởi động lại. |

### Storage health check – Kiểm tra sức khỏe ổ đĩa

Run PowerShell:

```powershell
Get-PhysicalDisk |
    Select-Object FriendlyName, MediaType, HealthStatus, OperationalStatus, Size
```

This reports available storage status information. Not all devices expose the same health details, and a healthy status does not guarantee that a disk will never fail.

Lệnh này hiển thị thông tin trạng thái lưu trữ mà thiết bị cung cấp. Không phải thiết bị nào cũng báo cáo đầy đủ thông tin, và trạng thái Healthy không đảm bảo ổ đĩa sẽ không hỏng.

For suspected storage problems, use appropriate manufacturer diagnostics and back up important data before performing tests that could stress the device.

Nếu nghi ngờ ổ đĩa có vấn đề, hãy sử dụng công cụ chẩn đoán phù hợp của nhà sản xuất và sao lưu dữ liệu trước khi chạy các bài kiểm tra có thể tạo tải lên thiết bị.

---

## 13. Step 11: Restore User Data – Khôi phục dữ liệu người dùng

### English

1. Verify the backup source and the intended user's identity.
2. Restore only required files and approved settings.
3. Preserve the appropriate folder structure.
4. Verify that restored files open correctly.
5. Check access permissions where relevant.
6. Confirm that required business data is available.
7. Run appropriate security checks on suspicious or untrusted files.

### Tiếng Việt

1. Xác minh nguồn sao lưu và đúng người dùng cần khôi phục.
2. Chỉ khôi phục file và thiết lập được yêu cầu, cho phép.
3. Giữ cấu trúc thư mục phù hợp.
4. Kiểm tra file đã khôi phục mở được bình thường.
5. Kiểm tra quyền truy cập khi cần.
6. Xác nhận dữ liệu nghiệp vụ cần thiết đã sẵn sàng.
7. Kiểm tra bảo mật đối với file đáng ngờ hoặc không đáng tin cậy.

Do not restore unknown executables, suspicious scripts, or untrusted applications without verification.

Không khôi phục file thực thi, script đáng ngờ hoặc ứng dụng không đáng tin cậy khi chưa xác minh.

### User data checklist – Checklist dữ liệu

- [ ] Desktop and Documents.
- [ ] Downloads where required.
- [ ] Pictures and other user folders.
- [ ] Browser bookmarks or profile data where authorized.
- [ ] Business application data.
- [ ] Required network share access.
- [ ] File permissions and ownership where applicable.

---

## 14. Step 12: Final Verification and Handover – Kiểm tra cuối cùng và bàn giao

### Final verification checklist – Checklist cuối cùng

- [ ] Windows starts normally after restart.
- [ ] Correct Windows edition and version are confirmed.
- [ ] Activation status is checked.
- [ ] Required drivers are installed.
- [ ] No unresolved critical Device Manager errors remain.
- [ ] Required updates are installed according to policy.
- [ ] Network connectivity works.
- [ ] Audio and display function correctly.
- [ ] Required applications launch successfully.
- [ ] Security settings are appropriate.
- [ ] Required user data is available.
- [ ] Peripherals work as expected.
- [ ] The user can sign in and access required resources.
- [ ] Outstanding issues are documented.

### Tiếng Việt

- [ ] Windows khởi động bình thường sau restart.
- [ ] Đã xác nhận đúng edition và phiên bản Windows.
- [ ] Đã kiểm tra trạng thái kích hoạt.
- [ ] Đã cài driver cần thiết.
- [ ] Không còn lỗi nghiêm trọng trong Device Manager chưa được xử lý.
- [ ] Đã cài các bản cập nhật cần thiết theo chính sách.
- [ ] Kết nối mạng hoạt động.
- [ ] Âm thanh và màn hình hoạt động bình thường.
- [ ] Ứng dụng cần thiết mở thành công.
- [ ] Thiết lập bảo mật phù hợp.
- [ ] Dữ liệu người dùng cần thiết đã sẵn sàng.
- [ ] Thiết bị ngoại vi hoạt động theo yêu cầu.
- [ ] Người dùng đăng nhập được và truy cập tài nguyên cần thiết.
- [ ] Các vấn đề còn tồn tại đã được ghi nhận.

---

## 15. IT Support Handover Template – Mẫu bàn giao IT Support

```text
Computer Model:
Asset Tag:
Serial Number:
Assigned User:
Windows Edition:
Windows Version:
OS Build:
System Architecture:
Installation Date:
BIOS Mode:
System Disk Partition Style:
Driver Status:
Windows Update Status:
Activation Status:
Defender Status:
Firewall Status:
BitLocker / Device Encryption Status:
Applications Installed:
Network Test Results:
Hardware Test Results:
Data Restored:
Outstanding Issues:
Technician:
Handover Date:
User Confirmation:
```

### Tiếng Việt

| Field | Nội dung cần ghi |
|---|---|
| Computer Model | Model máy tính |
| Asset Tag | Mã tài sản |
| Serial Number | Số serial thiết bị theo chính sách quản lý |
| Assigned User | Người sử dụng được bàn giao |
| Windows Edition | Edition Windows |
| Windows Version | Phiên bản Windows |
| OS Build | Build hệ điều hành |
| System Architecture | Kiến trúc hệ thống |
| Installation Date | Ngày cài đặt |
| BIOS Mode | Chế độ boot |
| System Disk Partition Style | Kiểu phân vùng ổ hệ thống |
| Driver Status | Trạng thái driver |
| Windows Update Status | Trạng thái cập nhật |
| Activation Status | Trạng thái kích hoạt |
| Defender Status | Trạng thái Microsoft Defender |
| Firewall Status | Trạng thái Firewall |
| BitLocker / Device Encryption Status | Trạng thái mã hóa |
| Applications Installed | Phần mềm đã cài |
| Network Test Results | Kết quả kiểm tra mạng |
| Hardware Test Results | Kết quả kiểm tra phần cứng |
| Data Restored | Dữ liệu đã khôi phục |
| Outstanding Issues | Lỗi còn tồn tại |
| Technician | Kỹ thuật viên |
| Handover Date | Ngày bàn giao |
| User Confirmation | Xác nhận của người dùng |

Do not include passwords, BitLocker recovery keys, or other secrets in the handover document.

Không ghi mật khẩu, khóa khôi phục BitLocker hoặc thông tin bí mật khác vào biên bản bàn giao.

---

## 16. Best Practices – Thực hành tốt

### English

- Follow a consistent post-installation checklist.
- Use official driver and software sources.
- Apply least-privilege access.
- Maintain appropriate endpoint security.
- Verify updates and restart behavior.
- Confirm the backup and recovery approach.
- Test the actual user workflow, not just whether Windows starts.
- Record unresolved issues and communicate them before handover.
- Follow organizational asset, licensing, and data-handling policies.

### Tiếng Việt

- Sử dụng checklist sau cài đặt thống nhất.
- Dùng nguồn driver và phần mềm chính thức.
- Áp dụng quyền truy cập tối thiểu.
- Duy trì bảo mật thiết bị đầu cuối phù hợp.
- Kiểm tra cập nhật và quá trình restart.
- Xác nhận phương án sao lưu và khôi phục.
- Kiểm tra quy trình sử dụng thực tế của người dùng, không chỉ kiểm tra Windows có khởi động.
- Ghi nhận lỗi chưa xử lý và thông báo trước khi bàn giao.
- Tuân thủ chính sách quản lý tài sản, bản quyền và dữ liệu của tổ chức.

---

## 17. References – Tài liệu tham khảo

1. **Microsoft Support – Windows Help and Learning**

   https://support.microsoft.com/windows

   General Windows troubleshooting and support documentation.

2. **Microsoft Support – Windows Security**

   https://support.microsoft.com/windows

   Windows security guidance and related support resources.

3. **Microsoft Learn – Windows deployment**

   https://learn.microsoft.com/windows/deployment/

   Windows deployment and configuration documentation.

4. **Microsoft Learn – Windows commands**

   https://learn.microsoft.com/windows-server/administration/windows-commands/windows-commands

   Reference for Windows command-line tools.

5. **Microsoft – Windows 11 specifications and requirements**

   https://www.microsoft.com/windows/windows-11-specifications

   Windows 11 hardware and system requirements.

6. **Device manufacturer support website**

   Use the official support page for the computer model to obtain validated drivers, firmware updates, and hardware documentation.

   Sử dụng trang hỗ trợ chính thức theo model máy tính để tải driver, firmware và tài liệu phần cứng phù hợp.

---


**Disclaimer:** This document is a technical learning guide. Follow the device manufacturer's documentation, applicable licensing terms, and organizational IT policies when performing production work.

**Lưu ý:** Đây là tài liệu học tập kỹ thuật. Khi thực hiện trên hệ thống thực tế, cần tuân thủ tài liệu của nhà sản xuất, điều khoản bản quyền và chính sách IT của tổ chức.

