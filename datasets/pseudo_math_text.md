## File hướng dẫn tiền xử lí các kí hiệu toán học thành dạng kí tự giả toán (pseudo-math text)

1. Mục đích: tạo ra một bộ quy tắc chuẩn hóa các kí tự toán học không thể được viết từ bàn phím thông thường thành các kí tự phổ thông, dựa trên LaTeX parsing, nhằm:
    - Đơn giản hóa đầu vào cho mô hình.
    - Đơn giản hóa luồng xử lí.
    - Tăng tính đồng nhất.

2. Quy ước:
    - Các kí tự không thể biểu diễn được bằng bàn phím thông thường thì dùng tên (có thể viết tắt) thông dụng, có kí tự "\\" ở đầu để phân biệt. Ví dụ $\pi$ chuyển thành \pi, $\int$ chuyển thành \int,...
    - Các kí tự, toán tử, phép toán có thể biểu diễn (hoặc biểu diễn tương đương) được bằng chữ có thể giữ nguyên (không dùng "\\"). Ví dụ sin, cos,...
    - Các kí hiệu tác động lên các kí tự khác thì sẽ được đánh dấu bằng cặp ngoặc tròn. Ví dụ $\vec a$ chuyển thành \vec ( a ) thay vì \vec a.
    - Số đứng riêng, toán tử đứng riêng và các dấu ngoặc đứng riêng. Ví dụ $\sin(2x + 3)$ chuyển thành "sin ( 2 x + 3 )".

3. Bảng quy đổi

| Kí tự toán học | Quy đổi tương ứng | Ví dụ |
|----------|----------|----------|
| Phân số | / | $\frac{a}{b}$ -> a / b |
| Mũ | ^ | $a^b$ -> a ^ b |
| Chỉ số dưới | _ | $x_0$ -> x _ 0 |
| Căn bậc hai | \sqrt | $\sqrt a$ -> \sqrt ( a ) |
| Số pi ($\pi$) | \pi | |
| Vô cực ($\inf$) | \inf | |
| Độ | \deg | $30\textdegree$ -> 30 \deg |
| $\leqslant$ | <= | |
| $\geqslant$ | >= | |
| Kéo theo, suy ra | => | $A \Rightarrow B$ -> A => B |
| Tương đương | <=> | $A \Leftrightarrow B$ -> A <=> B |
| Với mọi | \forall | $\forall P$ -> \forall P |
| Tồn tại | \exists | $\exists P$ -> \exists P |
| Thuộc | \in | $x \in A$ -> x \in A |
| Không thuộc | \notin | $x \notin A$ -> x \notin A |
| Tập rỗng ($\emptyset$) | \emptyset | |
| Tập con | \subset | $A \subset B -> A \subset B |
| Tập cha | \supset | $A \supset B -> A \supset B |
| Không phải tập con | \notsubset | $A \notsubset B -> A \notsubset B |
| Giao | \intersection | $A \cap B$ -> A \intersection B |
| Hợp | \union | $A \cup B$ -> A \union B |
| Phủ định (gạch ngang trên đầu) | \bar | $\bar A$ -> \bar ( A ) |