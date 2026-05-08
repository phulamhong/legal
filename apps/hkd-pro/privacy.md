---
title: Chính sách bảo mật — HKD Pro
---

# Chính sách bảo mật (Privacy Policy)

**Ứng dụng: HKD Pro** | **Đơn vị phát hành: NextAI**
**Hiệu lực: 08/05/2026** | **Cập nhật gần nhất: 08/05/2026**

> Chính sách này tuân thủ **Nghị định 13/2023/NĐ-CP** ngày 17/04/2023 về bảo vệ dữ liệu cá nhân của Chính phủ Việt Nam.

---

## 1. Đơn vị chịu trách nhiệm xử lý dữ liệu

- **Đơn vị xử lý dữ liệu (Bên Kiểm soát Dữ liệu)**: NextAI — đại diện bởi Lâm Hồng Phú
- **Người bảo vệ dữ liệu (DPO)**: Lâm Hồng Phú
- **Email người bảo vệ dữ liệu**: phulamhong@gmail.com
- **Email pháp lý**: legal@nextai.io

---

## 2. Dữ liệu cá nhân được thu thập

### 2.1. Khi đăng ký tài khoản

| Loại dữ liệu | Mục đích | Bắt buộc? |
|---|---|---|
| Email | Định danh tài khoản, gửi email xác nhận / khôi phục | Bắt buộc khi đăng ký tài khoản chính thức |
| Mật khẩu | Xác thực — lưu dưới dạng mã hóa bcrypt qua Supabase Auth | Bắt buộc |
| Tên hiển thị | Cá nhân hóa giao diện | Tùy chọn |

### 2.2. Khi sử dụng ứng dụng

| Loại dữ liệu | Mục đích | Cơ sở pháp lý |
|---|---|---|
| Thông tin hộ kinh doanh (tên, MST, địa chỉ, ngành nghề, chủ hộ) | Tính thuế đúng theo TT 152/2025 | Thực hiện hợp đồng dịch vụ |
| Giao dịch mua/bán (số tiền, hóa đơn, nhà cung cấp/khách hàng) | Lập sổ sách kế toán | Thực hiện hợp đồng |
| Chi phí (số tiền, chứng từ) | Tính TNCN phương pháp thực tế | Thực hiện hợp đồng |
| Thông tin BHXH chủ hộ kinh doanh | Theo dõi tuân thủ Luật BHXH 41/2024 | Thực hiện hợp đồng |
| Thông tin nhân viên (lương, BHXH) | Tính TNCN tiền lương | Thực hiện hợp đồng |
| Tài khoản ngân hàng (số tài khoản, ngân hàng) | Đối soát sao kê | Sự đồng ý của người dùng |
| Ảnh hóa đơn (khi quét) | OCR trích xuất thông tin | Sự đồng ý của người dùng (xem [Công bố sử dụng AI](ai-disclosure)) |
| Mã thiết bị (UUID nội bộ) | Liên kết gói đăng ký với thiết bị | Lợi ích chính đáng |

### 2.3. Dữ liệu kỹ thuật tự động thu thập
- **Phiên bản ứng dụng, hệ điều hành, mẫu thiết bị** — qua Firebase Crashlytics khi có lỗi (chỉ thu khi người dùng đồng ý báo lỗi)
- **Địa chỉ IP** — lưu trong nhật ký kết nối Supabase (chỉ phục vụ chống lạm dụng, xóa sau 30 ngày)

---

## 3. Mục đích xử lý dữ liệu

NextAI sử dụng dữ liệu cá nhân của bạn cho các mục đích sau:

1. **Cung cấp dịch vụ HKD Pro** — tính thuế, lập sổ sách, kê khai theo quy định pháp luật Việt Nam
2. **Xác thực tài khoản** — đăng nhập, khôi phục mật khẩu, ngăn truy cập trái phép
3. **Hỗ trợ khách hàng** — xử lý yêu cầu, khiếu nại
4. **Cải thiện sản phẩm** — phân tích lỗi (Crashlytics) — KHÔNG bao gồm dữ liệu nghiệp vụ
5. **Tuân thủ pháp luật** — lưu giữ sổ sách 10 năm theo TT 152/2025 Điều 9

NextAI **KHÔNG**:
- ❌ Bán dữ liệu cá nhân của người dùng cho bên thứ ba
- ❌ Sử dụng dữ liệu cho quảng cáo
- ❌ Theo dõi người dùng qua các ứng dụng khác

---

## 4. Bên thứ ba được chia sẻ dữ liệu

Ứng dụng phụ thuộc vào các nhà cung cấp dịch vụ sau (Bên xử lý dữ liệu):

| Nhà cung cấp | Vai trò | Dữ liệu chia sẻ | Vị trí | Chính sách |
|---|---|---|---|---|
| **Supabase Inc.** | Hạ tầng máy chủ (cơ sở dữ liệu + xác thực + lưu trữ) | Toàn bộ dữ liệu người dùng | Singapore (apse-1) | [supabase.com/privacy](https://supabase.com/privacy) |
| **Google LLC (Gemini API)** | AI nhận dạng hóa đơn | Ảnh hóa đơn người dùng tải lên | Mỹ / toàn cầu | [policies.google.com/privacy](https://policies.google.com/privacy) |
| **Google LLC (Firebase Crashlytics)** | Báo lỗi treo ứng dụng | Vết lỗi (stack trace), hệ điều hành, phiên bản (KHÔNG có dữ liệu nghiệp vụ) | Mỹ | [firebase.google.com/support/privacy](https://firebase.google.com/support/privacy) |
| **PayOS / VNPay** (khi có giao dịch trả phí) | Cổng thanh toán | Email, số tiền, mã giao dịch | Việt Nam | [payos.vn/dieu-khoan](https://payos.vn) |

Các bên trên đã ký Hợp đồng Xử lý Dữ liệu (DPA) với chúng tôi và cam kết bảo vệ dữ liệu theo chuẩn GDPR / Nghị định 13/2023.

---

## 5. Thời gian lưu trữ dữ liệu

| Loại dữ liệu | Thời gian lưu | Lý do |
|---|---|---|
| Sổ sách kế toán (giao dịch, chi phí, kê khai) | **10 năm** | Tuân thủ TT 152/2025 Điều 9 |
| Ảnh hóa đơn đính kèm | 10 năm | Cùng quy định trên |
| Thông tin tài khoản (email, mật khẩu mã hóa) | Đến khi người dùng yêu cầu xóa hoặc 3 năm sau khi không hoạt động | Cho phép người dùng khôi phục tài khoản |
| Nhật ký thay đổi (audit log) | 5 năm | Tuân thủ + hỗ trợ điều tra gian lận |
| Nhật ký kết nối / địa chỉ IP | 30 ngày | Chống lạm dụng |
| Vết lỗi ứng dụng (Crashlytics) | 90 ngày | Đủ để gỡ lỗi |

Sau thời hạn trên, dữ liệu sẽ được xóa hoặc ẩn danh hóa tự động.

---

## 6. Quyền của người dùng (theo Nghị định 13/2023 Điều 9)

Bạn có các quyền sau đối với dữ liệu cá nhân của mình:

### 6.1. Quyền được biết
Quyền này được thực hiện qua chính sách này.

### 6.2. Quyền đồng ý / từ chối
- Khi đăng ký: bạn đồng ý chính sách này khi tạo tài khoản
- Khi quét hóa đơn: ứng dụng yêu cầu đồng ý gửi ảnh tới Google Gemini
- Bạn có thể rút lại sự đồng ý bất cứ lúc nào (xóa tài khoản)

### 6.3. Quyền truy cập
Bạn có thể xem toàn bộ dữ liệu của mình trong ứng dụng:
- Giao dịch / Chi phí / Sổ sách: trong các màn hình tương ứng
- Tài khoản: Menu thanh bên → Tài khoản
- Cài đặt hộ kinh doanh: Hồ sơ HKD

### 6.4. Quyền chỉnh sửa
Mọi dữ liệu trong ứng dụng đều có nút **Sửa** ngay trên màn hình tương ứng. Trường hợp đặc biệt (ví dụ email tài khoản) xin liên hệ legal@nextai.io.

### 6.5. Quyền xóa dữ liệu (quyền được lãng quên)
Xem chi tiết: [Yêu cầu xóa dữ liệu](data-deletion)

### 6.6. Quyền hạn chế xử lý
Bạn có thể yêu cầu chúng tôi tạm dừng xử lý dữ liệu (ví dụ trong khi đang điều tra khiếu nại) qua email legal@nextai.io.

### 6.7. Quyền chuyển giao dữ liệu
Toàn bộ dữ liệu nghiệp vụ có thể xuất ra Excel / PDF qua menu **Xuất Excel** trong ứng dụng (định dạng chuẩn, có thể nhập vào MISA / Fast / phần mềm khác).

### 6.8. Quyền phản đối + khiếu nại
- Liên hệ legal@nextai.io trong vòng 30 ngày
- Nếu không hài lòng với phản hồi, có thể khiếu nại lên **Cục An toàn thông tin (Bộ Thông tin và Truyền thông)** hoặc các cơ quan có thẩm quyền theo Nghị định 13/2023.

---

## 7. Bảo mật dữ liệu

NextAI áp dụng các biện pháp kỹ thuật và tổ chức để bảo vệ dữ liệu của bạn:

### 7.1. Kỹ thuật
- ✓ **Mã hóa khi truyền**: TLS 1.3 cho mọi kết nối giữa thiết bị và máy chủ
- ✓ **Mã hóa khi lưu trữ**: dữ liệu Supabase được mã hóa AES-256
- ✓ **Mật khẩu**: mã hóa bằng bcrypt (Supabase Auth)
- ✓ **Mã kích hoạt**: HMAC-SHA256 phía máy chủ, khóa bí mật trong Supabase Vault
- ✓ **Bộ nhớ đệm gói đăng ký trên thiết bị**: lưu trong Keychain (iOS) hoặc EncryptedSharedPreferences (Android)
- ✓ **Bảo mật theo hàng (RLS)**: mỗi người dùng chỉ truy cập được dữ liệu của chính mình

### 7.2. Tổ chức
- ✓ Số người có quyền truy cập dữ liệu sản xuất: **1** (Lâm Hồng Phú)
- ✓ Khóa quản trị máy chủ được bảo vệ qua 1Password
- ✓ Nhật ký kiểm toán mọi thay đổi quan trọng
- ✓ Sao lưu tự động hàng ngày qua Supabase

### 7.3. Trách nhiệm khi vi phạm
Trong trường hợp xảy ra **rò rỉ dữ liệu cá nhân**, NextAI cam kết:
- Thông báo cho Cục An toàn thông tin (Bộ Thông tin và Truyền thông) trong **72 giờ** theo Nghị định 13/2023 Điều 23
- Thông báo cho các người dùng bị ảnh hưởng qua email trong **72 giờ**
- Báo cáo nguyên nhân, phạm vi ảnh hưởng và biện pháp khắc phục

---

## 8. Trẻ em dưới 13 tuổi

HKD Pro là ứng dụng dành cho **chủ hộ kinh doanh** — không thiết kế cho trẻ em. NextAI không thu thập có chủ đích dữ liệu của trẻ em dưới 13 tuổi. Nếu phát hiện tài khoản tạo bởi trẻ em, chúng tôi sẽ xóa ngay.

---

## 9. Cookie & theo dõi

Ứng dụng **không sử dụng cookie** (vì là ứng dụng gốc, không phải web). Trang Chính sách bảo mật này (trên GitHub Pages) có thể có cookie kỹ thuật của GitHub — không theo dõi mục đích thương mại.

---

## 10. Thay đổi chính sách

NextAI có thể cập nhật chính sách này. Khi có thay đổi quan trọng:
- ✓ Email thông báo cho người dùng đã đăng ký
- ✓ Hiển thị thông báo trong ứng dụng
- ✓ Cập nhật trường "Hiệu lực" / "Cập nhật gần nhất" ở đầu trang
- ✓ Lịch sử thay đổi được giữ trên kho lưu trữ GitHub

Người dùng tiếp tục sử dụng ứng dụng sau khi cập nhật = đồng ý với phiên bản mới.

---

## 11. Pháp luật áp dụng

Chính sách này tuân thủ:
- **Hiến pháp 2013** Điều 21 (quyền riêng tư)
- **Luật An toàn thông tin mạng 86/2015/QH13**
- **Luật An ninh mạng 24/2018/QH14**
- **Nghị định 13/2023/NĐ-CP** (bảo vệ dữ liệu cá nhân)
- **Luật Bảo vệ quyền lợi người tiêu dùng 19/2023/QH15**

Mọi tranh chấp được giải quyết tại **Tòa án có thẩm quyền tại TP.HCM, Việt Nam**.

---

## 12. Liên hệ

| Mục đích | Email | Phản hồi trong |
|---|---|---|
| Câu hỏi về quyền riêng tư / Người bảo vệ dữ liệu | phulamhong@gmail.com | 7 ngày làm việc |
| Yêu cầu xóa dữ liệu | legal@nextai.io ([biểu mẫu](data-deletion)) | 30 ngày (theo Nghị định 13/2023) |
| Khiếu nại pháp lý | legal@nextai.io | 30 ngày |
| Hỗ trợ kỹ thuật | support@nextai.io | 1-2 ngày làm việc |

---

← [Quay lại trang Pháp lý HKD Pro](/legal/apps/hkd-pro/)
