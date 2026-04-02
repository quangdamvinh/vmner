## File trình bày lược đồ các thực thể và hướng dẫn chú thích nhãn

### Mục tiêu
1. Xây dựng một lược đồ thực thể cho bài toán Nhận diện thực thể toán học cho văn bản tiếng Việt các thực thể được chia thành hai nhóm chính là:
    - Nhóm khái niệm (Concept)
    - Nhóm các đối tượng cụ thể (Instance)
2. Trình bày phạm vi, cách gán nhãn cho từng loại thực thể; các nguyên tắc chung cho việc gán nhãn và các trường hợp ngoại lệ (nếu có).

### Danh sách nhãn thực thể
1. Nhóm Concept:
    - MATH_CONCEPT
    - GEOMETRIC_SHAPE
    - GEOMETRIC_OBJECT
    - PROPERTY 
    - THEOREM 
    - QUANTITY 
2. Nhóm Instance:
    - SYMBOL 
    - SET 
    - EXPRESSION 
    - EQUATION 
    - FUNCTION 
    - GEOMETRIC_INSTANCE 
3. Các nhãn sử dụng chuẩn BIO tagging.

### Nguyên tắc chung
1. Gán nhãn thực thể dài nhất có ý nghĩa.
    - Ví dụ trong câu xuất hiện "hàm số bậc hai" thì đó sẽ coi là một thực thể mặc dù bản thân từ "hàm số" cũng có thể được coi là một thực thể.
2. Ưu tiên tính nhất quán hơn sự chính xác tuyệt đối.
    - Không chia các nhãn quá chi tiết.
    - Một nhãn có thể chấp nhận các phạm trù, đối tượng gần giống nhau thep quy ước cho trước.
3. Không gán nhãn số nếu đứng lẻ (không nằm trong phương trình, biểu thức,...).
4. Không cố gán nhãn toàn bộ các kí hiệu toán học xuất hiện.
    - Ví dụ như các toán tử đứng lẻ (thuộc, giao, hợp, tập con,...).
5. Nếu thực thể dạng có dạng Concept + Instance thì sẽ được tách ra thành các thực thể riêng thay vì gộp chung vào làm một thực thể.
    - Nhằm tăng tính nhất quán, tránh mơ hồ cho việc gán nhãn.
    - Ví dụ "điểm A" sẽ tách thành hai thực thể là "điểm" (khái niệm) và "A" (đối tượng) thay vì gộp vào làm một thực thể.
6. Việc gán nhãn sẽ không cố SUY LUẬN quá sâu về bản chất toán học mà chỉ NHẬN DẠNG dựa trên những gì được viết ra.


### Quy tắc cụ thể từng nhãn

| Tên thực thể | Phạm vi | Ví dụ |
|----------|----------|----------|

### Một vài ví dụ gán nhãn hoàn chỉnh

### Các trường hợp ngoại lệ hoặc cần lưu ý (xuất hiện trong lúc gán nhãn dữ liệu)