---
title: Yêu cầu xóa dữ liệu — HKD Pro
---

# Yêu cầu xóa dữ liệu (Data Deletion Request)

**Ứng dụng: HKD Pro** | **Hiệu lực: 08/05/2026**

> Quyền được lãng quên — theo Nghị định 13/2023/NĐ-CP Điều 9 Khoản 5 và hướng dẫn của Apple / Google.

---

## 1. Quyền của bạn

Bạn có quyền yêu cầu NextAI xóa toàn bộ dữ liệu cá nhân của mình bất cứ lúc nào, không cần lý do, miễn phí.

NextAI cam kết xử lý yêu cầu trong **30 ngày** kể từ khi nhận đủ thông tin xác minh.

---

## 2. Cách yêu cầu xóa

### Cách 1 — Tự xóa trong ứng dụng (nhanh nhất, không cần liên hệ)

1. Mở ứng dụng HKD Pro
2. Menu thanh bên → **Tài khoản**
3. Bấm **Đăng xuất** (xóa phiên đăng nhập)
4. Cài lại ứng dụng → tài khoản còn nhưng không truy cập được nếu không nhớ email

> ⚠️ Cách này KHÔNG xóa dữ liệu trên máy chủ. Để xóa hoàn toàn, dùng Cách 2.

### Cách 2 — Yêu cầu xóa hoàn toàn qua email (chính thức)

Gửi email tới **phu.lam@nextaivn.com** với:
- **Tiêu đề**: `[XOA DU LIEU] HKD Pro — <email tài khoản>`
- **Nội dung**: bao gồm thông tin xác minh:

```
1. Email tài khoản HKD Pro: [email của bạn]
2. Tên hiển thị trong ứng dụng: [tên]
3. Tên hộ kinh doanh đã đăng ký (ít nhất 1): [tên HKD]
4. Lý do (tùy chọn): [...]
5. Loại xóa:
   [ ] Xóa toàn bộ (tài khoản + sổ sách + ảnh hóa đơn)
   [ ] Chỉ xóa ảnh hóa đơn — giữ sổ sách
   [ ] Chỉ vô hiệu hóa tài khoản — giữ dữ liệu 90 ngày để khôi phục
```

NextAI sẽ phản hồi trong **3 ngày làm việc** xác nhận yêu cầu, sau đó xử lý trong **27 ngày** tiếp theo (tổng tối đa 30 ngày).

### Cách 3 — Yêu cầu xóa khi không nhớ email

Nếu bạn quên email tài khoản:
1. Email **phu.lam@nextaivn.com** mô tả tên hộ kinh doanh + mã số thuế + ngày đăng ký gần đúng
2. NextAI tra cứu, gửi email tới địa chỉ tìm được
3. Người dùng xác nhận "Đúng, xóa giúp" qua trả lời email
4. Xóa trong 30 ngày

---

## 3. Loại dữ liệu sẽ được xóa

### 3.1. Xóa toàn bộ

| Loại | Hành động |
|---|---|
| Tài khoản (auth.users) | Xóa khỏi Supabase Auth |
| Hồ sơ | Xóa hoàn toàn |
| Sổ sách giao dịch | Xóa khỏi cơ sở dữ liệu |
| Sổ chi phí | Xóa |
| Hồ sơ hộ kinh doanh | Xóa |
| Ảnh hóa đơn đính kèm | Xóa khỏi kho lưu trữ |
| Nhật ký thay đổi | Xóa |
| Lịch sử gói đăng ký | Ẩn danh hóa (giữ lại doanh số tổng cho thuế của NextAI) |
| Bộ nhớ đệm trên thiết bị | Người dùng phải tự gỡ ứng dụng |

### 3.2. Lưu giữ ngoại lệ (theo quy định pháp luật)
Một số dữ liệu NextAI **PHẢI giữ** theo luật, kể cả khi người dùng yêu cầu xóa:
- **Hóa đơn thanh toán mà NextAI đã xuất** (giữ 10 năm theo Luật Kế toán)
- **Nhật ký kiểm toán liên quan đến chống rửa tiền / gian lận** (giữ theo yêu cầu cơ quan)

Trong trường hợp này, dữ liệu được **ẩn danh hóa** (không gắn với định danh người dùng nữa) thay vì xóa hoàn toàn.

---

## 4. Hậu quả của việc xóa dữ liệu

### 4.1. Không thể khôi phục
Sau khi xóa, **dữ liệu KHÔNG thể khôi phục**. Nếu sau này muốn dùng lại ứng dụng:
- Phải đăng ký tài khoản mới với email khác
- Phải nhập lại toàn bộ thông tin hộ kinh doanh, sổ sách
- Gói đăng ký cũ bị mất (cần mua mới)

### 4.2. Sao lưu dữ liệu trước khi xóa
**Khuyến nghị**: trước khi yêu cầu xóa, **xuất Excel/PDF** mọi sổ sách qua menu **Xuất Excel** trong ứng dụng. Lưu 10 năm theo TT 152/2025 Điều 9 — đây là trách nhiệm của người dùng, không phải NextAI sau khi xóa.

### 4.3. Hủy yêu cầu đang chờ
Trong **7 ngày** đầu sau khi gửi yêu cầu, bạn có thể hủy bằng email trả lời "HUY YEU CAU XOA". Sau 7 ngày, quá trình xóa bắt đầu chạy và không thể đảo ngược.

---

## 5. Xác minh quyền yêu cầu

NextAI **CÓ QUYỀN** yêu cầu người dùng xác minh thân phận trước khi xóa, bằng cách:
- Gửi email xác nhận tới email tài khoản
- Yêu cầu người dùng trả lời email xác nhận
- Hỏi thông tin nội bộ (ví dụ mã số thuế của hộ kinh doanh đã đăng ký)

Mục đích: tránh kẻ xấu yêu cầu xóa nhầm tài khoản người khác. Quá trình xác minh tối đa **3 ngày làm việc**.

---

## 6. Phản hồi từ NextAI

Sau khi xử lý xong, NextAI gửi email xác nhận:

```
Tiêu đề: [HKD Pro] Xác nhận xóa dữ liệu — <email>

Email của bạn: <email>
Ngày yêu cầu: <ngày>
Ngày hoàn tất: <ngày>

Đã xóa:
- ✓ Tài khoản xác thực
- ✓ Hồ sơ
- ✓ <N> giao dịch
- ✓ <M> chi phí
- ✓ <K> ảnh hóa đơn
- ✓ <X> hộ kinh doanh

Đã ẩn danh hóa:
- Hóa đơn thanh toán (giữ theo Luật Kế toán)

Cảm ơn bạn đã sử dụng HKD Pro.
— Đội ngũ NextAI
```

Email này được lưu trong nhật ký kiểm toán hệ thống của NextAI **5 năm** để chứng minh đã thực hiện yêu cầu (nếu cơ quan thanh tra hỏi).

---

## 7. Khiếu nại

Nếu bạn cho rằng NextAI không xử lý đúng yêu cầu xóa dữ liệu:

### Bước 1: Khiếu nại nội bộ
Email **phu.lam@nextaivn.com** với tiêu đề `[KHIEU NAI XOA DU LIEU]` — phản hồi trong 7 ngày làm việc.

### Bước 2: Cơ quan có thẩm quyền
Nếu vẫn không hài lòng, có thể khiếu nại tới:
- **Cục An toàn thông tin** (Bộ Thông tin và Truyền thông) — theo Nghị định 13/2023 Điều 23
- **Tòa án có thẩm quyền tại TP.HCM**

---

## 8. Câu hỏi thường gặp

### Tôi xóa ứng dụng — có xóa dữ liệu trên máy chủ không?
**Không**. Xóa ứng dụng chỉ xóa bộ nhớ đệm cục bộ. Dữ liệu trên Supabase vẫn còn cho đến khi bạn yêu cầu xóa qua email.

### Tôi đổi sang phần mềm khác — phải làm gì với HKD Pro?
1. Xuất Excel toàn bộ sổ sách qua menu **Xuất Excel**
2. Nhập vào phần mềm mới
3. Yêu cầu xóa dữ liệu HKD Pro qua [Cách 2](#cách-2--yêu-cầu-xóa-hoàn-toàn-qua-email-chính-thức)

### Gói Thành viên Sáng lập có hoàn tiền khi yêu cầu xóa không?
Không — gói Thành viên Sáng lập là vĩnh viễn, thanh toán một lần. Yêu cầu xóa không hủy gói đăng ký đã thanh toán.

### Có giới hạn số lần yêu cầu xóa không?
Không — bạn có thể yêu cầu bất cứ lúc nào, miễn phí.

### Sau khi xóa, NextAI có giữ email của tôi không?
Email tài khoản: **xóa**. Email yêu cầu xóa dữ liệu (lưu trữ trong hộp thư phu.lam@nextaivn.com): **giữ 5 năm** để chứng minh tuân thủ. Nội dung email được coi là thông tin nghiệp vụ, không phải dữ liệu cá nhân nữa sau khi xử lý xong.

---

## 9. Liên hệ

| Mục đích | Email |
|---|---|
| Yêu cầu xóa dữ liệu | **phu.lam@nextaivn.com** |
| Người bảo vệ dữ liệu (DPO) | phu.lam@nextaivn.com |
| Khiếu nại | phu.lam@nextaivn.com |
| Hỗ trợ kỹ thuật | phu.lam@nextaivn.com |

**Địa chỉ**: 54 Thới An 13, phường Thới An, TP.HCM

---

← [Quay lại trang Pháp lý HKD Pro](/apps/hkd-pro/)
