# Nhà Sách Phương Pắc

Bài tập lớn môn Thiết kế Web cơ bản (PTIT): website nhà sách, chỉ dùng HTML + CSS, không dùng JavaScript.
Nhóm 4 người, mỗi người 10 trang có bố cục khác nhau.

## Cấu trúc

```text
_mau.html         trang mẫu: header, menu, footer. Copy file này để tạo trang mới
css/bien.css      biến màu, font, bo góc, bóng (file chung)
css/chung.css     lưới 12 cột, nút, ô nhập, thẻ sách, header, menu, footer (file chung)
img/  fonts/

Mỗi người tự tạo và tự push:
css/nguoi-X.css   CSS riêng của mình (X = 1, 2, 3, 4)
ten-trang.html    các trang của mình (trang chủ là index.html, do Người 1 làm)
```

## Cách làm một trang

1. `git checkout main` rồi `git pull`
2. `git checkout -b feature/ten-trang`
3. Copy `_mau.html` thành `ten-trang.html`, sửa `<title>`, đổi `css/nguoi-X.css` thành file của mình (lần đầu thì tạo file này), sửa breadcrumb, thêm class `dang-chon` vào mục menu của trang
4. Làm xong: `git add .`, `git commit -m "Ten trang: mo ta"`, `git push -u origin feature/ten-trang`
5. Trên GitHub mở Pull Request vào `main`, nhờ 1 bạn duyệt, được Approve thì Merge và xóa nhánh

`main` đã khóa: không đẩy thẳng lên được, mọi thay đổi đi qua Pull Request.

## Quy ước tránh xung đột

- Chỉ sửa file HTML của trang mình và `css/nguoi-X.css` của mình.
- `css/bien.css`, `css/chung.css`, `_mau.html` là file chung: muốn đổi thì báo nhóm, làm trên nhánh `chung/ten-viec`.
- Class đặt bằng tiếng Việt không dấu, nối bằng gạch ngang: `.the-sach`, `.menu-chinh`.
- Không dùng JavaScript. Tương tác làm bằng `:checked`, `:target`, `<details>`, `:hover`, `:focus-within`, `:has()`.

## Phân công (tên file)

| Người | Khu vực | Trang |
| --- | --- | --- |
| 1 | Trưng bày & tiếp thị | index, khuyen-mai, tu-sach-kinh-dien, sach-moi-theo-tuan, xep-hang, the-qua-tang, goi-qua, gioi-thieu, tuyen-dung, hoi-sach |
| 2 | Sản phẩm & khám phá | danh-muc, van-hoc, chi-tiet-sach, chi-tiet-vpp, combo, doc-thu, so-sanh, tac-gia, tac-gia-a-z, goi-y-sach |
| 3 | Mua hàng & tài khoản | gio-hang, thanh-toan, hoan-tat, tra-cuu-don, dang-nhap, quen-mat-khau, tai-khoan, don-hang, hoa-don, ho-so |
| 4 | Nội dung & hỗ trợ | goc-doc-sach, bai-viet, cau-lac-bo, lich-su-kien, cua-hang, chi-tiet-cua-hang, tro-giup, chinh-sach, lien-he, so-do-trang, 404 |

Mô tả chi tiết từng trang và tiêu chuẩn "xong" nằm trong tài liệu Checklist của nhóm.
