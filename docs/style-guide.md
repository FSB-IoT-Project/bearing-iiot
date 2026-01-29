# Hướng dẫn Thiết kế & Màu sắc (Style Guide)

Dự án này sử dụng bộ nhận diện màu sắc dựa trên hệ thống thiết kế của **Atlassian Jira**, tối ưu hóa cho cả hai chế độ Sáng (Light mode) và Tối (Dark mode).

## 🎨 Bảng màu (Jira Inspired)

### 1. Chế độ Sáng (Light Mode)
*   **Màu chủ đạo (Primary Blue)**: `#0052CC` (Sử dụng cho Header và các liên kết chính).
*   **Màu nền (Background)**: `#FFFFFF`.
*   **Màu nền phụ (Surface/Sidebar)**: `#F4F5F7`.
*   **Màu văn bản chính**: `#172B4D` (N800 - Đảm bảo độ tương phản cao).
*   **Màu văn bản phụ**: `#42526E` (N500).

### 2. Chế độ Tối (Dark Mode)
*   **Màu chủ đạo (Primary Blue)**: `#579DFF` (Xanh sáng hơn để nổi bật trên nền tối).
*   **Màu nền (Background)**: `#1D2125`.
*   **Màu bề mặt (Surface)**: `#22272B`.
*   **Màu văn bản chính**: `#C1C7D0` (Đảm bảo không bị chìm).
*   **Màu văn bản phụ**: `#8C9BAB`.

---

## 📏 Quy tắc tuân thủ (Rules for Maintenance)

Để duy trì tính nhất quán và khả năng đọc, mọi thay đổi về giao diện hoặc thêm nội dung mới cần tuân theo các quy tắc sau:

1.  **Độ tương phản (Contrast)**:
    *   Không bao giờ sử dụng màu văn bản xám nhạt trên nền trắng.
    *   Trong Dark mode, văn bản chính luôn phải sử dụng tông màu `Neutral` sáng (như `#C1C7D0`) để tránh mỏi mắt.
2.  **Sử dụng Design Tokens**:
    *   Ưu tiên sử dụng các biến CSS đã định nghĩa trong `stylesheets/extra.css` thay vì gán mã màu trực tiếp (hard-code hex).
    *   Ví dụ: dùng `var(--md-typeset-color)` cho văn bản.
3.  **Admonitions (Ghi chú)**:
    *   Sử dụng các block `!!! note`, `!!! info`, `!!! warning` để phân biệt nội dung, nhưng đảm bảo màu nền của chúng không xung đột với màu nền Jira Dark.
4.  **Cấu trúc tệp tin CSS**:
    *   Mọi tùy chỉnh giao diện tập trung tại `docs/stylesheets/extra.css`.
    *   Không sửa trực tiếp các tệp lõi của theme.

---

## 🛠 Cách kiểm tra
Chạy lệnh preview cục bộ để đảm bảo màu sắc hiển thị đúng trên cả 2 mode:
```bash
mkdocs serve
```
Khi xem trang, sử dụng icon ☀️/🌙 trên Header để chuyển đổi giữa các theme.
