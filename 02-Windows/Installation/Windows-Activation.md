# Windows Activation – Kích hoạt Windows

## 1. Introduction – Giới thiệu

### Tiếng Việt

Windows Activation là quá trình xác minh bản Windows đã cài đặt có quyền sử dụng và giấy phép phù hợp hay không.

Kích hoạt Windows giúp xác nhận trạng thái cấp phép của hệ điều hành. Tuy nhiên, trạng thái đã kích hoạt không thay thế cho việc kiểm tra nguồn gốc giấy phép, điều khoản sử dụng hoặc quyền chuyển giấy phép sang thiết bị khác.

Các yếu tố ảnh hưởng đến quá trình kích hoạt bao gồm:

- Phiên bản và edition Windows được cài đặt.
- Loại giấy phép và quyền sử dụng tương ứng.
- Product Key hoặc Digital License.
- Kết nối Internet và khả năng liên lạc với máy chủ kích hoạt.
- Thay đổi phần cứng quan trọng.
- Chính sách cấp phép của tổ chức, nếu là máy tính doanh nghiệp.

### English

Windows Activation is the process of verifying whether the installed copy of Windows has an applicable activation entitlement.

Activation confirms the operating system's licensing status. However, an activated status does not replace verification of license authenticity, applicable license terms, or transfer rights.

Factors affecting activation include:

- Installed Windows version and edition.
- License type and associated usage rights.
- Product Key or Digital License.
- Internet connectivity and activation server availability.
- Significant hardware changes.
- Organizational licensing policies for managed devices.

---

## 2. License Types and Activation Methods – Loại giấy phép và phương thức kích hoạt

### 2.1 License Types – Các loại giấy phép

| License type | English description | Mô tả tiếng Việt |
|---|---|---|
| OEM | Typically supplied with a new device and subject to OEM license terms. | Thường đi kèm máy tính mới và tuân theo điều khoản giấy phép OEM. |
| Retail | Purchased separately and subject to applicable transfer conditions. | Mua riêng và tuân theo điều kiện chuyển nhượng được áp dụng. |
| Volume Licensing | Licensing arrangements intended for eligible organizations. | Hình thức cấp phép dành cho tổ chức đủ điều kiện theo thỏa thuận. |
| Other license arrangements | Rights depend on the specific product, subscription, or agreement. | Quyền sử dụng phụ thuộc sản phẩm, gói đăng ký hoặc thỏa thuận cụ thể. |

**Important:** OEM, Retail và Volume Licensing mô tả các hình thức cấp phép hoặc thỏa thuận cấp phép. Digital License và Product Key là các khái niệm liên quan đến quyền kích hoạt và phương thức kích hoạt, không phải những loại giấy phép tương đương với OEM hoặc Retail.

**Lưu ý:** Quyền chuyển giấy phép có thể khác nhau tùy sản phẩm và điều khoản. Không nên kết luận rằng mọi giấy phép OEM đều có thể chuyển sang máy khác hoặc mọi Product Key đều có thể sử dụng lại.

### 2.2 Activation Methods – Phương thức kích hoạt

| Method | English description | Mô tả tiếng Việt |
|---|---|---|
| Digital License | Activation entitlement that does not require manually entering a product key in supported scenarios. | Quyền kích hoạt kỹ thuật số, không cần nhập Product Key thủ công trong các trường hợp được hỗ trợ. |
| Product Key | A 25-character key used in supported activation scenarios. | Khóa sản phẩm gồm 25 ký tự, dùng trong các trường hợp kích hoạt được hỗ trợ. |
| KMS | Organizational activation using a Key Management Service infrastructure. | Kích hoạt trong tổ chức thông qua hạ tầng máy chủ KMS. |
| MAK | Multiple Activation Key used under applicable volume licensing arrangements. | Khóa kích hoạt nhiều lần theo thỏa thuận cấp phép số lượng lớn phù hợp. |

**English:** KMS and MAK are associated with applicable volume licensing scenarios. They should not be treated as generic activation methods for every personal Windows device.

**Tiếng Việt:** KMS và MAK thuộc các trường hợp cấp phép số lượng lớn phù hợp. Không nên xem chúng là phương thức kích hoạt chung cho mọi máy tính cá nhân.

---

## 3. Check Windows Edition and Version – Kiểm tra edition và phiên bản Windows

Before troubleshooting activation, identify the installed Windows edition and version.

Trước khi xử lý lỗi kích hoạt, cần xác định edition và phiên bản Windows đang sử dụng.

### Method 1: Using winver

Press `Win + R`, enter:

```cmd
winver
```

Review the displayed Windows version and OS build.

Kiểm tra phiên bản Windows và số hiệu bản dựng được hiển thị.

### Method 2: Using Settings

**Windows 11:**

1. Open Settings.
2. Select System.
3. Select About.
4. Review Windows specifications.

**Tiếng Việt:**

1. Mở Settings.
2. Chọn System.
3. Chọn About.
4. Kiểm tra thông tin Windows specifications.

**Windows 10:** Open Settings > System > About.

### Method 3: Using Command Prompt

```cmd
systeminfo
```

This command displays general system information, including Windows configuration details.

Lệnh này hiển thị thông tin hệ thống, bao gồm các thông tin cấu hình Windows.

### Method 4: Using PowerShell

Open PowerShell and run:

```powershell
Get-ComputerInfo | Select-Object WindowsProductName, WindowsVersion, OsBuildNumber
```

Review the product name, Windows version, and OS build number.

Kiểm tra tên sản phẩm, phiên bản Windows và số hiệu bản dựng.

**Troubleshooting note – Lưu ý xử lý sự cố:** A valid license for Windows Home does not automatically activate Windows Pro. Always verify the edition before changing the product key or reinstalling Windows.

Giấy phép Windows Home không mặc nhiên kích hoạt được Windows Pro. Luôn xác minh edition trước khi thay đổi Product Key hoặc cài đặt lại Windows.

---

## 4. Check Activation Status – Kiểm tra trạng thái kích hoạt

### Method 1: Settings

**Windows 11:**

1. Open Settings.
2. Select System.
3. Select Activation.
4. Review the activation status and any error message.

**Windows 10:**

1. Open Settings.
2. Select Update & Security.
3. Select Activation.
4. Review the activation status and any error message.

### Method 2: Check Using slmgr.vbs

Open Command Prompt or Windows Terminal and run the following commands.

#### Display activation expiration information

```cmd
slmgr /xpr
```

**English:** Displays activation expiration information where applicable. It is particularly useful for identifying expiration dates associated with KMS activation.

**Tiếng Việt:** Hiển thị thông tin thời hạn kích hoạt khi áp dụng. Lệnh này đặc biệt hữu ích để kiểm tra thời hạn của hình thức kích hoạt KMS.

For Retail or MAK activation, a perpetual activation may be reported instead of an expiration date. This command does not independently prove that a license is transferable or that its source is legitimate.

Đối với Retail hoặc MAK, hệ thống có thể thông báo đã kích hoạt vĩnh viễn thay vì hiển thị ngày hết hạn. Lệnh này không tự chứng minh giấy phép có thể chuyển nhượng hoặc có nguồn gốc hợp lệ.

#### Display basic license information

```cmd
slmgr /dli
```

Displays basic licensing information for the installed Windows edition.

Hiển thị thông tin cấp phép cơ bản của edition Windows đang cài đặt.

#### Display detailed license information

```cmd
slmgr /dlv
```

Displays detailed licensing information, which may include the activation channel and licensing status.

Hiển thị thông tin cấp phép chi tiết, có thể bao gồm kênh kích hoạt và trạng thái cấp phép.

**Security note – Lưu ý bảo mật:** Review command output before sharing it. Do not publish product keys, activation identifiers, or other sensitive licensing information in a public repository.

Xem lại kết quả trước khi chia sẻ. Không đăng Product Key, mã định danh kích hoạt hoặc thông tin cấp phép nhạy cảm lên repository công khai.

---

## 5. Activate Windows with a Digital License – Kích hoạt bằng giấy phép kỹ thuật số

### English

1. Connect the device to the Internet.
2. Open Settings > System > Activation on Windows 11.
3. Confirm that the installed edition matches the digital license.
4. Follow the activation instructions displayed by Windows.
5. If applicable, sign in with the Microsoft account associated with the license.
6. If activation fails, run the Activation troubleshooter when available.
7. Verify the activation status after troubleshooting.

### Tiếng Việt

1. Kết nối máy tính với Internet.
2. Trên Windows 11, mở Settings > System > Activation.
3. Xác nhận edition đang cài đặt phù hợp với giấy phép kỹ thuật số.
4. Làm theo hướng dẫn kích hoạt hiển thị trên Windows.
5. Nếu áp dụng, đăng nhập tài khoản Microsoft liên kết với giấy phép.
6. Nếu kích hoạt thất bại, chạy Activation troubleshooter khi có sẵn.
7. Kiểm tra lại trạng thái kích hoạt sau khi xử lý.

**Important – Quan trọng**

- A digital license may be associated with the device.
- A linked Microsoft account can help with supported reactivation scenarios.
- A significant hardware change, such as replacing the motherboard, may affect activation.
- The installed edition must match the license entitlement.

- Giấy phép kỹ thuật số có thể được liên kết với thiết bị.
- Tài khoản Microsoft liên kết có thể hỗ trợ một số trường hợp kích hoạt lại.
- Thay đổi phần cứng quan trọng, chẳng hạn thay mainboard, có thể ảnh hưởng đến kích hoạt.
- Edition đang cài đặt phải phù hợp với quyền sử dụng giấy phép.

---

## 6. Activate Using a Product Key – Kích hoạt bằng Product Key

### English

1. Obtain a valid product key from an authorized or otherwise legitimate source.
2. Open Settings > Activation.
3. Select the option to change the product key, if available.
4. Enter the 25-character product key.
5. Follow the on-screen instructions.
6. Review the resulting activation status.

### Tiếng Việt

1. Chuẩn bị Product Key hợp lệ từ nguồn được ủy quyền hoặc nguồn có tính hợp pháp phù hợp.
2. Mở Settings > Activation.
3. Chọn tùy chọn thay đổi Product Key nếu có.
4. Nhập Product Key gồm 25 ký tự.
5. Làm theo hướng dẫn trên màn hình.
6. Kiểm tra trạng thái kích hoạt sau khi hoàn tất.

### Important Notes – Lưu ý quan trọng

- The key must be applicable to the installed Windows edition.
- A key may be rejected if it is invalid, blocked, incompatible, or used outside its permitted licensing conditions.
- Do not publish a complete product key in a support ticket, screenshot, or public repository.
- Do not assume that a key offered at an unusually low price is legitimate.

- Khóa phải phù hợp với edition Windows đang cài đặt.
- Khóa có thể bị từ chối nếu không hợp lệ, bị chặn, không tương thích hoặc được sử dụng ngoài điều kiện cấp phép.
- Không công khai toàn bộ Product Key trong phiếu hỗ trợ, ảnh chụp màn hình hoặc repository.
- Không mặc nhiên cho rằng khóa được bán với giá thấp bất thường là hợp pháp.

---

## 7. Activation Troubleshooting – Xử lý lỗi kích hoạt

### Step 1: Collect Information – Thu thập thông tin

Before making changes, record:

Trước khi thay đổi cấu hình, hãy ghi nhận:

- Windows edition and version.
- Activation status.
- Exact error message and error code.
- License type or activation channel, if known.
- Whether the device was previously activated.
- Whether significant hardware changes occurred.
- Whether the device belongs to an organization.

- Edition và phiên bản Windows.
- Trạng thái kích hoạt.
- Thông báo lỗi và mã lỗi chính xác.
- Loại giấy phép hoặc kênh kích hoạt nếu đã xác định.
- Máy tính đã từng được kích hoạt hay chưa.
- Có thay đổi phần cứng quan trọng hay không.
- Thiết bị có thuộc tổ chức hay không.

### Step 2: Check Basic Conditions – Kiểm tra điều kiện cơ bản

1. Verify Internet connectivity.
2. Check the installed Windows edition.
3. Confirm the device date, time, and time zone.
4. Review the exact error code.
5. Check whether the license is valid for the device and installed edition.
6. For organizational devices, verify the applicable activation requirements with IT.

1. Kiểm tra kết nối Internet.
2. Kiểm tra edition Windows.
3. Xác nhận ngày, giờ và múi giờ của máy tính.
4. Ghi nhận chính xác mã lỗi.
5. Xác minh giấy phép phù hợp với thiết bị và edition đang cài.
6. Với máy tính doanh nghiệp, xác minh yêu cầu kích hoạt với bộ phận IT.

Do not disable Windows Firewall or security protections as a routine activation troubleshooting step.

Không tắt Windows Firewall hoặc các biện pháp bảo mật như một bước xử lý lỗi kích hoạt thông thường.

### Step 3: Run the Activation Troubleshooter – Chạy công cụ khắc phục sự cố

**Windows 11:**

1. Open Settings > System > Activation.
2. If Windows is not activated and the option is available, select Troubleshoot.
3. Follow the prompts.
4. Review the result and any new error code.

**Windows 10:**

1. Open Settings > Update & Security > Activation.
2. Select Troubleshoot if available.
3. Follow the displayed instructions.
4. Review the result.

**Tiếng Việt:**

Chạy Activation troubleshooter khi tùy chọn này xuất hiện. Công cụ có thể yêu cầu đăng nhập bằng tài khoản quản trị và không phải lúc nào cũng khả dụng. Sau khi chạy, hãy kiểm tra lại mã lỗi vì mã lỗi có thể thay đổi.

### Step 4: Check Edition Compatibility – Kiểm tra tính tương thích của edition

| Installed edition | License entitlement | Recommended action |
|---|---|---|
| Windows Home | Windows Home | Check connectivity and activation status. |
| Windows Home | Windows Pro | Determine whether an eligible upgrade to Pro is required. |
| Windows Pro | Windows Home | Install or return to the edition covered by the license, if appropriate. |
| Windows Enterprise | Personal Home/Pro license | Verify the applicable Enterprise licensing requirements. |

| Edition đang cài | Giấy phép | Hướng xử lý |
|---|---|---|
| Windows Home | Windows Home | Kiểm tra kết nối và trạng thái kích hoạt. |
| Windows Home | Windows Pro | Xác minh có cần nâng cấp lên Pro theo quyền sử dụng hay không. |
| Windows Pro | Windows Home | Xem xét cài lại hoặc quay về edition được cấp phép nếu phù hợp. |
| Windows Enterprise | Giấy phép Home/Pro cá nhân | Xác minh yêu cầu cấp phép Enterprise tương ứng. |

Do not reinstall Windows or change editions until the license entitlement and required edition are understood. Back up important data before reinstalling.

Không cài lại Windows hoặc đổi edition trước khi xác định được giấy phép và edition cần dùng. Sao lưu dữ liệu quan trọng trước khi cài lại.

### Step 5: Check Network and Activation Services – Kiểm tra mạng và dịch vụ kích hoạt

For online activation:

- Verify that the device can access the Internet.
- Check whether the activation service may be temporarily unavailable.
- Review firewall or proxy restrictions only when there is evidence they may interfere.
- Retry according to the displayed Windows instructions.

Đối với kích hoạt trực tuyến:

- Xác nhận thiết bị truy cập Internet được.
- Kiểm tra khả năng máy chủ kích hoạt đang tạm thời không khả dụng.
- Chỉ kiểm tra giới hạn Firewall hoặc Proxy khi có dấu hiệu liên quan.
- Thử lại theo hướng dẫn của Windows.

For an organization-managed KMS device, confirm that the device can reach the organization's required activation infrastructure and contact the administrator if necessary.

Với thiết bị doanh nghiệp sử dụng KMS, xác minh máy tính có thể kết nối đến hạ tầng kích hoạt cần thiết của tổ chức và liên hệ quản trị viên khi cần.

### Step 6: Escalate When Necessary – Chuyển cấp xử lý khi cần

Contact the appropriate party when the issue cannot be resolved:

- Microsoft Support for supported activation issues.
- The device manufacturer for an OEM license or a new-device activation problem.
- The seller for a questionable or rejected purchase.
- The organization's IT or licensing administrator for KMS, MAK, or other organizational licensing.

Liên hệ đúng đơn vị khi chưa giải quyết được:

- Microsoft Support đối với các vấn đề kích hoạt thuộc phạm vi hỗ trợ.
- Nhà sản xuất nếu liên quan giấy phép OEM hoặc máy mới.
- Người bán nếu khóa có dấu hiệu không hợp lệ hoặc bị từ chối.
- Bộ phận IT hoặc quản trị cấp phép nếu liên quan KMS, MAK hoặc giấy phép doanh nghiệp.

---

## 8. Common Windows Activation Error Codes – Các mã lỗi kích hoạt thường gặp

The following are common examples, not an exhaustive list. Always check Microsoft's current guidance for the exact code and Windows version.

Các mã dưới đây là ví dụ thường gặp, không phải danh sách đầy đủ. Luôn đối chiếu hướng dẫn hiện hành của Microsoft theo mã lỗi và phiên bản Windows cụ thể.

| Error code | Possible meaning | Recommended action |
|---|---|---|
| `0xC004F034` | Invalid key or a key that does not match the installed product/version. | Verify the key and edition. |
| `0xC004F210` | Edition mismatch between the key or digital license and installed Windows. | Confirm the licensed edition and follow the supported edition-change or installation process. |
| `0xC004C003` | Product key may be invalid or blocked. | Verify the purchase and contact the seller or Microsoft Support. |
| `0xC004C008` | Key may have been used on another device or beyond permitted usage. | Review license terms and contact the appropriate support channel. |
| `0xC004F211` | Windows detected a hardware change. | Run the Activation troubleshooter and follow the supported reactivation process. |
| `0xC004F213` | Windows cannot find a product key on the device. | Check the existing digital license or valid product key. |
| `0xC004FC03` | Network connectivity or firewall restrictions may prevent online activation. | Verify Internet access and investigate relevant network restrictions. |
| `0x8007267C` | Activation server unavailable or the device cannot connect to it. | Check connectivity and retry later. |
| `0x87E10BC6` | Activation or licensing service issue. | Follow the current Microsoft troubleshooting guidance and retry as instructed. |

### Tiếng Việt – Hướng xử lý theo mã lỗi

- **`0xC004F034`:** Kiểm tra Product Key và edition Windows; xác minh khóa có đúng sản phẩm hay không.
- **`0xC004F210`:** Kiểm tra sự không khớp giữa edition đã cài và giấy phép.
- **`0xC004C003`:** Xác minh nguồn mua khóa; liên hệ người bán hoặc Microsoft Support.
- **`0xC004C008`:** Kiểm tra điều khoản sử dụng và việc khóa đã được dùng trên thiết bị khác hay chưa.
- **`0xC004F211`:** Chạy công cụ khắc phục sự cố và làm theo quy trình kích hoạt lại sau thay đổi phần cứng.
- **`0xC004F213`:** Kiểm tra giấy phép kỹ thuật số hoặc Product Key hợp lệ của thiết bị.
- **`0xC004FC03`:** Kiểm tra Internet và các giới hạn mạng có liên quan.
- **`0x8007267C`:** Kiểm tra kết nối đến máy chủ kích hoạt và thử lại sau.
- **`0x87E10BC6`:** Đối chiếu hướng dẫn hiện hành của Microsoft cho sự cố dịch vụ kích hoạt.

**Note:** An error code identifies a possible cause; it does not prove the cause by itself. Read the complete error message and verify the device's licensing context before making changes.

**Lưu ý:** Mã lỗi chỉ gợi ý nguyên nhân có thể xảy ra, không tự chứng minh nguyên nhân. Cần đọc đầy đủ thông báo và xác minh tình trạng cấp phép trước khi thay đổi cấu hình.

---

## 9. Special Activation Scenarios – Các tình huống đặc biệt

### 9.1 Windows Not Activated After Reinstallation

**Possible causes:**

- The installed edition differs from the licensed edition.
- The device has not connected to the activation service.
- The original license cannot be located or matched.
- A significant hardware change has occurred.

**Recommended actions:**

1. Check the installed edition.
2. Connect to the Internet.
3. Open Activation settings.
4. Run the troubleshooter if available.
5. Check the original license or contact the appropriate support channel.

**Tiếng Việt:** Sau khi cài lại Windows, hãy kiểm tra edition, kết nối Internet, chạy công cụ khắc phục sự cố nếu có và xác minh giấy phép ban đầu. Không mặc nhiên mua khóa mới trước khi xác định nguyên nhân.

### 9.2 Activation Failure After a Hardware Change

Replacing a motherboard or making another significant hardware change may affect activation.

Thay mainboard hoặc thay đổi phần cứng quan trọng có thể ảnh hưởng đến kích hoạt.

Recommended actions:

1. Check Activation settings.
2. Run the Activation troubleshooter if available.
3. Follow the supported reactivation process.
4. Review the applicable license terms.
5. Contact the device manufacturer or Microsoft Support if unresolved.

Hướng xử lý:

1. Kiểm tra Settings > Activation.
2. Chạy Activation troubleshooter nếu có.
3. Làm theo quy trình kích hoạt lại được hỗ trợ.
4. Kiểm tra điều khoản giấy phép tương ứng.
5. Liên hệ nhà sản xuất hoặc Microsoft Support nếu chưa giải quyết được.

### 9.3 Organization-Managed Windows Devices

For company devices, activation may be managed through organizational infrastructure or licensing arrangements.

Đối với máy tính doanh nghiệp, việc kích hoạt có thể được quản lý thông qua hạ tầng hoặc thỏa thuận cấp phép của tổ chức.

Recommended actions:

- Identify whether the device uses KMS, MAK, or another organizational method.
- Confirm access to the required corporate network or activation service.
- Check organizational deployment and licensing policies.
- Contact the IT administrator.

Hướng xử lý:

- Xác định máy sử dụng KMS, MAK hay phương thức cấp phép khác của tổ chức.
- Kiểm tra khả năng truy cập mạng doanh nghiệp hoặc dịch vụ kích hoạt cần thiết.
- Kiểm tra chính sách triển khai và cấp phép.
- Liên hệ quản trị viên IT.

Do not apply personal-device troubleshooting instructions blindly to managed enterprise systems.

Không áp dụng máy móc hướng xử lý của máy cá nhân cho hệ thống doanh nghiệp được quản lý tập trung.

### 9.4 “Your Windows License Will Expire Soon”

This warning can occur in certain organizational activation scenarios, including KMS-managed devices.

Thông báo này có thể xuất hiện trong một số trường hợp kích hoạt của tổ chức, bao gồm thiết bị sử dụng KMS.

Recommended actions:

1. Run `slmgr /dlv` and review the licensing channel.
2. Run `slmgr /xpr` to check activation expiration information.
3. If the device belongs to an organization, contact its IT administrator.
4. Do not assume the warning means that every Windows license has expired.

Hướng xử lý:

1. Chạy `slmgr /dlv` để xem thông tin kênh cấp phép.
2. Chạy `slmgr /xpr` để kiểm tra thông tin thời hạn kích hoạt.
3. Nếu là máy doanh nghiệp, liên hệ quản trị viên IT.
4. Không mặc nhiên kết luận mọi giấy phép Windows đều đã hết hạn chỉ từ thông báo này.

---

## 10. Security and Licensing Compliance – Bảo mật và tuân thủ cấp phép

### English

- Use Windows licenses obtained through legitimate channels.
- Do not use unauthorized activation scripts, cracks, or activation bypass tools.
- Do not publish product keys or sensitive licensing information.
- Do not disable security protections to bypass activation.
- Keep purchase records and license documentation where appropriate.
- Follow the applicable Microsoft license terms and organizational policies.
- Verify suspicious low-cost license offers before purchase.

### Tiếng Việt

- Sử dụng giấy phép Windows từ nguồn hợp pháp.
- Không sử dụng script kích hoạt trái phép, crack hoặc công cụ vượt qua cơ chế kích hoạt.
- Không công khai Product Key hoặc thông tin cấp phép nhạy cảm.
- Không tắt các biện pháp bảo mật để vượt qua kích hoạt.
- Lưu chứng từ mua hàng và tài liệu giấy phép khi phù hợp.
- Tuân thủ điều khoản giấy phép Microsoft và chính sách của tổ chức.
- Xác minh các lời chào bán giấy phép giá thấp bất thường trước khi mua.

---

## 11. Technician Checklist – Checklist dành cho kỹ thuật viên

Use this checklist when receiving a Windows activation support request.

Sử dụng checklist này khi tiếp nhận yêu cầu hỗ trợ kích hoạt Windows.

- [ ] Record the computer model and device identifier according to company policy.
- [ ] Record Windows edition, version, and build.
- [ ] Check the activation status in Settings.
- [ ] Run `slmgr /xpr` when appropriate.
- [ ] Run `slmgr /dlv` if further licensing information is required.
- [ ] Record the exact error code and message.
- [ ] Check Internet connectivity.
- [ ] Verify the licensed edition.
- [ ] Determine whether the device is personally owned or organization-managed.
- [ ] Check whether significant hardware changes occurred.
- [ ] Run the Activation troubleshooter if available.
- [ ] Apply only supported troubleshooting steps.
- [ ] Verify the final activation status.
- [ ] Record the resolution and escalate unresolved cases.

### Tiếng Việt

- [ ] Ghi nhận model máy và mã thiết bị theo chính sách công ty.
- [ ] Ghi nhận edition, phiên bản và build Windows.
- [ ] Kiểm tra trạng thái kích hoạt trong Settings.
- [ ] Chạy `slmgr /xpr` khi phù hợp.
- [ ] Chạy `slmgr /dlv` nếu cần thêm thông tin cấp phép.
- [ ] Ghi chính xác mã lỗi và thông báo.
- [ ] Kiểm tra kết nối Internet.
- [ ] Xác minh edition được cấp phép.
- [ ] Xác định máy cá nhân hay máy doanh nghiệp được quản lý.
- [ ] Kiểm tra các thay đổi phần cứng quan trọng.
- [ ] Chạy Activation troubleshooter nếu có.
- [ ] Chỉ áp dụng các bước xử lý được hỗ trợ.
- [ ] Kiểm tra trạng thái kích hoạt cuối cùng.
- [ ] Ghi nhận kết quả và chuyển cấp nếu chưa giải quyết được.

---

## 12. Activation Record Template – Mẫu ghi nhận kích hoạt

Use the following template for an IT work log or support ticket.

Sử dụng mẫu dưới đây trong nhật ký công việc IT hoặc phiếu hỗ trợ.

```text
Computer Model:
Device Asset ID:
Windows Edition:
Windows Version:
OS Build:
Activation Status:
License Type / Channel:
Activation Error Code:
Previous Activation Status:
Recent Hardware Changes:
Network Connectivity:
Troubleshooting Steps:
Resolution:
Final Verification:
Verification Date:
Technician:
```

### Tiếng Việt – Giải thích các trường

| Field | Ý nghĩa |
|---|---|
| Computer Model | Model máy tính |
| Device Asset ID | Mã tài sản thiết bị |
| Windows Edition | Edition Windows |
| Windows Version | Phiên bản Windows |
| OS Build | Số hiệu bản dựng |
| Activation Status | Trạng thái kích hoạt |
| License Type / Channel | Loại giấy phép hoặc kênh kích hoạt |
| Activation Error Code | Mã lỗi kích hoạt |
| Previous Activation Status | Trạng thái kích hoạt trước đó |
| Recent Hardware Changes | Thay đổi phần cứng gần đây |
| Network Connectivity | Tình trạng kết nối mạng |
| Troubleshooting Steps | Các bước xử lý |
| Resolution | Kết quả xử lý |
| Final Verification | Kết quả xác minh cuối cùng |
| Verification Date | Ngày xác minh |
| Technician | Kỹ thuật viên thực hiện |

**Security note:** Never record the complete product key in a public or broadly accessible work log. Follow the organization's data-handling policy.

**Lưu ý bảo mật:** Không ghi toàn bộ Product Key trong nhật ký công khai hoặc nơi nhiều người có thể truy cập. Tuân thủ chính sách xử lý dữ liệu của tổ chức.

---

## 13. References – Tài liệu tham khảo

1. Microsoft Support – Get help with Windows activation errors  
   https://support.microsoft.com/en-us/windows/activation/get-help-with-windows-activation-errors

2. Microsoft Support – Using the Windows Activation troubleshooter  
   https://support.microsoft.com/en-us/windows/activation/using-the-windows-activation-troubleshooter

3. Microsoft Support – Activate Windows  
   https://support.microsoft.com/en-us/windows/activation/activate-windows

4. Microsoft Learn – Slmgr.vbs options for obtaining volume activation information  
   https://learn.microsoft.com/en-us/windows-server/get-started/activation-slmgr-vbs-options

---

**Disclaimer:** This document is an IT reference guide. Licensing rights and activation procedures may vary by Windows edition, product, agreement, and organizational policy. Always verify current Microsoft documentation and applicable license terms.

**Tuyên bố:** Đây là tài liệu tham khảo kỹ thuật IT. Quyền sử dụng và quy trình kích hoạt có thể khác nhau tùy edition Windows, sản phẩm, thỏa thuận và chính sách tổ chức. Luôn kiểm tra tài liệu Microsoft hiện hành và điều khoản giấy phép áp dụng.
