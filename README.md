# NextAI Legal

Kho lưu trữ tập trung **Chính sách bảo mật**, **Điều khoản sử dụng** và các tài liệu pháp lý cho mọi sản phẩm của NextAI.

🌐 **Trang web đang hoạt động**: https://phulamhong.github.io/legal/

## Cấu trúc

```
legal/
├── _config.yml              # Cấu hình Jekyll (GitHub Pages)
├── index.md                 # Trang chủ liệt kê các ứng dụng
├── apps/
│   └── hkd-pro/             # HKD Pro
│       ├── index.md
│       ├── privacy.md       # Chính sách bảo mật (Nghị định 13/2023)
│       ├── terms.md         # Điều khoản sử dụng
│       ├── ai-disclosure.md # Công bố sử dụng AI Gemini
│       └── data-deletion.md # Quy trình yêu cầu xóa dữ liệu
├── shared/
│   └── company.md           # Thông tin NextAI
└── README.md
```

## Thêm ứng dụng mới

1. Tạo thư mục `apps/<tên-app>/`
2. Sao chép mẫu từ `apps/hkd-pro/` (privacy + terms + index + ai + data-deletion)
3. Sửa nội dung phù hợp với ứng dụng mới
4. Cập nhật `index.md` ở thư mục gốc để thêm liên kết tới ứng dụng mới
5. Commit + push → GitHub Pages tự build

## Xem trước cục bộ

```bash
# Cần Ruby + Bundler
bundle init
bundle add jekyll
bundle exec jekyll serve
# → http://localhost:4000/legal/
```

## Cập nhật chính sách

Mỗi lần sửa chính sách:
- ✓ Cập nhật trường "Cập nhật gần nhất" ở đầu file
- ✓ Commit message rõ ràng (ví dụ "privacy: thêm Resend SMTP vào danh sách bên xử lý")
- ✓ Nếu thay đổi quan trọng — gửi email thông báo người dùng trước 15-30 ngày tùy mức độ
- ✓ Trong ứng dụng: hiển thị thông báo "Chính sách đã cập nhật, xem tại …"

## Bản quyền

Nội dung trong kho lưu trữ này thuộc NextAI. Cho phép người dùng của các ứng dụng NextAI tham chiếu, không cho phép sử dụng làm chính sách cho sản phẩm khác.
