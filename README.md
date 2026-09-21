# [Thực hành] CSS | grid-row Property

Dự án thực hành chuyên sâu và tương tác trực quan về thuộc tính **`grid-row`** trong CSS Grid Layout.

---

## 1. Giới thiệu tổng quan

Thuộc tính **`grid-row`** trong CSS được sử dụng để chỉ định kích thước và vị trí của một phần tử con (*grid item*) trong bố cục lưới theo trục dọc (các hàng).

Nó là cú pháp rút gọn (**shorthand**) kết hợp giữa hai thuộc tính:
- **`grid-row-start`**: Chỉ định đường lưới (*grid line*) mà tại đó phần tử bắt đầu hiển thị.
- **`grid-row-end`**: Chỉ định đường lưới (*grid line*) mà tại đó phần tử dừng hiển thị, hoặc số hàng mà phần tử sẽ kéo dài qua.

---

## 2. Cú pháp & Các giá trị thuộc tính

### Cú pháp chuẩn:
```css
grid-row: <grid-row-start> / <grid-row-end>;
```

### Bảng tra cứu giá trị và ý nghĩa:

| Giá trị thuộc tính | Ví dụ | Ý nghĩa chi tiết |
|---|---|---|
| **Đường kẻ lưới số (Grid Lines)** | `grid-row: 1 / 3;` | Bắt đầu tại đường kẻ ngang 1, kết thúc tại đường kẻ ngang 3 (chiếm trọn 2 hàng: hàng 1 và hàng 2). |
| **Từ khóa `span`** | `grid-row: 1 / span 2;` | Bắt đầu từ Line 1 và mở rộng thêm đúng 2 hàng (tương đương với `1 / 3`). |
| **Chỉ dùng `span`** | `grid-row: span 3;` | Chiếm 3 hàng, vị trí bắt đầu do thuật toán tự động sắp xếp. |
| **Số âm (Negative index)** | `grid-row: 1 / -1;` | Trải dài từ đường kẻ đầu tiên (đỉnh) đến đường kẻ cuối cùng (đáy), phủ trọn chiều cao container. |
| **Giá trị `auto`** | `grid-row: auto;` | Trình duyệt tự động định vị theo luồng thông thường (mặc định chiếm 1 hàng). |

> **Quy tắc vàng:** Trong CSS Grid, với một lưới có **N hàng**, sẽ luôn có **N + 1 đường lưới ngang** (Row Lines) được đánh số từ **1** đến **N + 1** (hoặc từ **-(N + 1)** đến **-1**).

---

## 3. Cấu trúc thư mục dự án

```
thuc-hanh-CSS-grid-row-Property/
│
├── index.html        # Trang chủ: Lý thuyết đầy đủ, bộ giả lập Playground tương tác, Grid lines visualizer & trắc nghiệm
├── vidu1.html        # Ví dụ 1: Kéo dài hàng cơ bản (1 / 3 vs 1 / span 2 vs span 2)
├── vidu2.html        # Ví dụ 2: Bố cục Admin Dashboard thực tế với Sidebar toàn màn hình (1 / 4)
├── vidu3.html        # Ví dụ 3: Bento Grid hiện đại với thẻ Feature cao gấp đôi (grid-row: span 2)
└── README.md         # Hướng dẫn chi tiết bài thực hành
```

---

## 4. Điểm nổi bật của dự án

1. **Giao diện hiện đại & thẩm mỹ cao**:
   - Thiết kế chuẩn Dark Mode công nghệ với bảng màu Indigo/Violet/Slate sang trọng.
   - Font chữ cao cấp: *Plus Jakarta Sans* & *JetBrains Mono*.
   - Hiệu ứng chuyển động mượt mà, bóng đổ 3D và thẻ Glassmorphism.
2. **Bộ giả lập trực quan (Interactive Playground)**:
   - Cho phép chọn bất kỳ Item nào từ 1 đến 6 để cấu hình `grid-row-start`, `grid-row-end`, `grid-column`.
   - Có sẵn các nút Preset mẫu thông dụng: *Trải 2 hàng*, *Sidebar full*, *Dùng span*, *Hàng giữa*, *Reset*.
   - Bật/tắt đường kẻ lưới trực quan (Row Lines 1, 2, 3, 4, 5 và các số âm -1, -2, -3, -4, -5).
   - Tự động sinh mã CSS kèm nút **Sao chép CSS** nhanh (với Toast thông báo).
3. **Bộ câu hỏi trắc nghiệm tương tác (Quiz)**:
   - 4 câu hỏi trắc nghiệm chọn lọc bám sát kiến thức trọng tâm.
   - Phản hồi đúng/sai tức thì và phần giải thích chi tiết củng cố kiến thức.
4. **Các ví dụ thực tế phong phú**:
   - `vidu1.html`: So sánh trực tiếp các biến thể cú pháp.
   - `vidu2.html`: Ứng dụng thực tế trong thiết kế Web Dashboard.
   - `vidu3.html`: Phong cách Bento Grid hiện đại theo xu hướng UI mới nhất.

---

## 5. Hướng dẫn chạy & Xem kết quả

Mở trực tiếp tệp `index.html` trong bất kỳ trình duyệt web hiện đại nào (Chrome, Edge, Firefox, Safari) hoặc sử dụng tiện ích Live Server trong VS Code.

```bash
# Hoặc mở nhanh bằng trình duyệt trên Windows PowerShell:
Start-Process "index.html"
```
