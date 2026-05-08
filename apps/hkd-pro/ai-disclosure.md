---
title: Công bố sử dụng AI — HKD Pro
---

# Công bố sử dụng AI (AI Disclosure)

**Ứng dụng: HKD Pro** | **Hiệu lực: 08/05/2026**

> Trang này minh bạch về cách HKD Pro sử dụng AI — tuân thủ Đạo luật AI của EU (EU AI Act, áp dụng cho người dùng tại EU) và thông lệ tốt nhất toàn cầu.

---

## 1. Tính năng dùng AI trong HKD Pro

### 1.1. Quét hóa đơn (OCR — nhận dạng ký tự quang học)
- **Nhà cung cấp AI**: Google Gemini Vision API
- **Loại mô hình**: Gemini 1.5 Flash / Pro (có thể thay đổi)
- **Chức năng**: trích xuất từ ảnh hóa đơn → ngày, số tiền, nhà cung cấp, mã hóa đơn, thuế GTGT
- **Khi nào kích hoạt**: chỉ khi người dùng **chủ động** chụp ảnh hoặc chọn ảnh từ thư viện

### 1.2. Phát hiện bất thường (Anomaly Detection)
- **Loại**: dựa trên quy tắc cố định (KHÔNG dùng mô hình AI/ML bên ngoài) — chạy cục bộ trên thiết bị
- **Chức năng**: cảnh báo khi doanh thu tăng đột biến, tồn kho âm, v.v.

### 1.3. Tự động gợi ý (Autocomplete)
- Tìm kiếm cục bộ trên dữ liệu cache trong thiết bị — không phải AI

---

## 2. Luồng dữ liệu khi quét hóa đơn

```
Người dùng chụp ảnh hóa đơn
        │
        ▼
┌────────────────────────────────────────┐
│ Ứng dụng HKD Pro (trên thiết bị)       │
│ - Lưu ảnh tạm trong vùng nhớ riêng     │
└────────┬───────────────────────────────┘
         │
         │ (chỉ khi người dùng bấm "Trích xuất bằng AI")
         ▼
┌────────────────────────────────────────┐
│ Google Gemini API (Mỹ / toàn cầu)      │
│ - Nhận ảnh                             │
│ - Trả về dữ liệu JSON các trường       │
└────────┬───────────────────────────────┘
         │
         ▼
┌────────────────────────────────────────┐
│ Ứng dụng HKD Pro                       │
│ - Hiển thị trong màn hình "Kiểm tra"   │
│ - Người dùng KIỂM TRA và chỉnh sửa     │
│ - Bấm "Lưu" → ghi vào sổ kế toán       │
└────────────────────────────────────────┘
```

**Quan trọng**:
- ✓ Ảnh **CHỈ** được gửi lên Gemini khi người dùng chủ động bấm
- ✓ Gemini không lưu ảnh lâu dài (chính sách Google: tối đa 30 ngày để gỡ lỗi, không dùng để huấn luyện mô hình)
- ✓ Sau khi nhận kết quả → ảnh không tải lên lại nữa
- ✓ Người dùng có thể chỉnh sửa kết quả OCR trước khi lưu → AI không tự ghi sổ

---

## 3. Cảnh báo về độ tin cậy của AI

### 3.1. AI có thể sai
Gemini Vision rất tốt nhưng **KHÔNG hoàn hảo**. Thường sai khi:
- Hóa đơn mờ, viết tay, cong vênh
- Phông chữ lạ (phông cổ điển, không hỗ trợ tiếng Việt)
- Ánh sáng yếu hoặc bị lóa
- Hóa đơn có bảng phức tạp với nhiều dòng sản phẩm
- Chữ bị che bởi đóng dấu, chữ ký

### 3.2. Trách nhiệm của người dùng
- **Người dùng PHẢI kiểm tra** mọi trường thông tin OCR trước khi lưu vào sổ
- Ứng dụng có giao diện cho phép sửa từng trường
- Nếu OCR sai → lưu sai → có thể ảnh hưởng tờ khai thuế

### 3.3. NextAI không chịu trách nhiệm khi:
- Người dùng lưu dữ liệu OCR sai mà không kiểm tra
- Gemini API trả về kết quả sai (Google chịu trách nhiệm về chất lượng mô hình)
- Rò rỉ dữ liệu do người dùng gửi ảnh có nội dung nhạy cảm (ví dụ ảnh có thêm thông tin cá nhân khác)

---

## 4. Sự đồng ý của người dùng

### 4.1. Lần đầu sử dụng tính năng quét
Ứng dụng hiển thị thông báo:
> "Tính năng này gửi ảnh lên Google Gemini AI để trích xuất thông tin. Bằng việc tiếp tục, bạn đồng ý cho ảnh hóa đơn được xử lý bởi Google. Bạn có thể tắt tính năng AI và nhập thủ công thay thế."
>
> [Đồng ý] [Hủy]

### 4.2. Có thể từ chối
Người dùng có thể **không sử dụng AI** và nhập tay tất cả dữ liệu — ứng dụng vẫn hoạt động đầy đủ.

### 4.3. Rút lại sự đồng ý
Người dùng có thể rút lại sự đồng ý bất cứ lúc nào — chỉ cần ngừng sử dụng tính năng quét. Ảnh đã gửi lên Gemini sẽ tự xóa theo chính sách của Google (30 ngày).

---

## 5. Bảo vệ dữ liệu trong luồng AI

### 5.1. Khu vực máy chủ Gemini
- HKD Pro gọi Gemini qua endpoint toàn cầu của Google
- Google định tuyến đến máy chủ gần nhất — có thể là Singapore, Đài Loan, hoặc Mỹ
- Google cam kết KHÔNG dùng dữ liệu của người dùng để huấn luyện mô hình thương mại (theo Điều khoản Gemini API)

### 5.2. Tối thiểu hóa dữ liệu
- Ứng dụng chỉ gửi **ảnh hóa đơn** — không gửi thông tin định danh người dùng (email, mã số thuế, v.v.)
- Không kèm thông tin về người dùng khác

### 5.3. Thời gian lưu trữ
- Ảnh trong vùng nhớ ứng dụng: cho tới khi người dùng xóa phiếu
- Ảnh trên máy chủ Gemini: tối đa 30 ngày theo chính sách Google
- Kết quả OCR (định dạng JSON): lưu trong cơ sở dữ liệu ứng dụng cùng với phiếu giao dịch

---

## 6. Quyền của người dùng theo Đạo luật AI của EU (nếu là người dùng EU)

Mặc dù HKD Pro hướng đến thị trường Việt Nam, ứng dụng có thể được truy cập từ EU. Theo Đạo luật AI của EU (EU AI Act):

| Quyền | HKD Pro đáp ứng? |
|---|---|
| Quyền được biết AI đang được sử dụng | ✅ Trang này + thông báo trong ứng dụng |
| Quyền từ chối sử dụng AI | ✅ Có thể tắt AI và nhập tay |
| Quyền được con người xem xét | ✅ Người dùng luôn kiểm tra trước khi lưu |
| Quyền được giải thích | ✅ Có thể yêu cầu giải thích qua support@nextai.io |

HKD Pro không thuộc danh mục "hệ thống AI có rủi ro cao" (không quyết định việc làm, tín dụng, y tế).

---

## 7. Liên hệ

Câu hỏi về AI: **support@nextai.io**

---

← [Quay lại trang Pháp lý HKD Pro](/legal/apps/hkd-pro/)
