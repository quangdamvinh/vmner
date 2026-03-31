## File hướng dẫn tiền xử lí các kí hiệu toán học thành dạng kí tự giả toán (pseudo-math text)

1. Mục đích: tạo ra một bộ quy tắc chuẩn hóa các kí tự toán học không thể được viết từ bàn phím thông thường thành các kí tự phổ thông, dựa trên LaTeX parsing, nhằm:
    - Đơn giản hóa đầu vào cho mô hình.
    - Đơn giản hóa luồng xử lí.
    - Tăng tính đồng nhất.

2. Quy ước:
    - Các kí tự không thể biểu diễn được bằng bàn phím thông thường thì dùng tên (có thể viết tắt) thông dụng, có kí tự "\" ở đầu để phân biệt. Ví dụ $\pi$ chuyển thành \pi, $\int$ chuyển thành \int,...
    - Các kí tự, toán tử, phép toán có thể biểu diễn (hoặc biểu diễn tương đương) được bằng chữ có thể giữ nguyên (không dùng "\"). Ví dụ sin, cos,...
    - Số đứng riêng, toán tử đứng riêng và các dấu ngoặc đứng riêng. Ví dụ $\sin(2x + 3)$ chuyển thành "sin ( 2 x + 3 )".

3. Bảng quy đổi
| Kí tự toán học | Kí tự quy đổi tương ứng | Ví dụ |
|---|---|---|
| Phân số | Sử dụng "/" | $\frac{a}{b} -> a / b |
| $\pi$ | \pi| | 
