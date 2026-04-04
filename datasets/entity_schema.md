## File trình bày lược đồ các thực thể và hướng dẫn chú thích nhãn

### I. Mục tiêu
1. Xây dựng một lược đồ thực thể cho bài toán Nhận diện thực thể toán học cho văn bản tiếng Việt các thực thể được chia thành hai nhóm chính là:
    - Nhóm khái niệm (Concept)
    - Nhóm các đối tượng cụ thể (Instance)
2. Trình bày phạm vi, cách gán nhãn cho từng loại thực thể; các nguyên tắc chung cho việc gán nhãn và các trường hợp ngoại lệ (nếu có).

### II. Danh sách nhãn thực thể
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

### III. Nguyên tắc chung
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


### IV. Quy tắc cụ thể từng nhãn

| Tên thực thể | Phạm vi | Ví dụ |
|----------|----------|----------|
| MATH_CONCEPT | Các thuật ngữ, định nghĩa, khái niệm phổ biến trong toán học (đại số, giải tích)| Hàm số, phương trình,,,, |
| GEOMETRIC_SHAPE | Các từ chỉ các dạng hình học | Hình vuông, hình nón,... |
| GEOMETRIC_OBJECT | Các từ chỉ các đối tượng trong hình học | Điểm, đường thẳng,... |
| THEOREM | Tên các định lí, công thức | Định lí Pi-ta-go, nhị thức Niu-tơn,... |
| PROPERTY | Các từ chỉ các tính chất hay mối quan hệ | Vuông góc, song song,... |
| QUANTITY | Các từ chỉ đại lượng | Diện tích, chu vi,... |
| SYMBOL | Các kí hiệu toán học hoặc kí tự đại diện cho các đối tượng toán học cụ thể (biến, tham số,...) | A, x, m,... |
| SET | Tập hợp hoặc miền số | {1, 2, 3}, (0, 1),... |
| EXPRESSION | BIểu thức toán học | sin(x), b^2 - 4ac,... |
| EQUATION | Phương trình, bất phương trình, mở rộng cho cả các công thức, đẳng thức | x^2 - 2x + 1 = 0 |
| FUNCTION | Hàm số | f(x) = 2x + 1 |
| GEOMETRIC_INSTANCE | Các đối tượng hình học cụ thể | ABCD (hình tứ giác), MN (đường thẳng) |

### V. Một vài ví dụ gán nhãn hoàn chỉnh

1. Cho tập hợp A = {a; b; c}. Tập A có bao nhiêu tập con?
    - Cho O
    - tập B-MATH_CONCEPT
    - hợp I-MATH_CONCEPT
    - A B-SYMBOL
    - = O
    - { B-SET
    - a I-SET
    - ; I-SET
    - b I-SET
    - ; I-SET
    - c I-SET
    - } I-SET
    - . O
    - Tập B-MATH_CONCEPT
    - A B-SYMBOL
    - có O
    - bao O
    - nhiêu O
    - tập B-MATH_CONCEPT
    - con I-MATH_CONCEPT
    - ? O

    Ghi chú 1: cụm "A = {a; b; c}" tuy chứa dấu "=" nhưng vì đây là phép gán/khai báo nên ta sẽ không gán nhãn là EQUATION mà sẽ gán nhãn riêng hai phần bên trái và phải dấu "=" và không gán nhãn dấu "=".

2. Hình nào dưới đây biểu diễn miền nghiệm của bất phương trình x - y < 3?
3. Cho tam giác ABC có \angle(B) = 60 \deg, \angle(C) = 45 \deg, AC = 10. Tính a, R, S, r.
4. Cho hình bình hành ABCD. Chứng minh rằng với mọi điểm M, ta có: \vector(MA) + \vector(MC) = \vecto(MB) + \vecto(MD).
5. Parabol y = - x^2 + 2x + 3 có đỉnh là:
6. Phương trình nào sau đây là phương trình tham số của đường thẳng?
7. Trong khai triển nhị thức Newton của (2x + 3)^5, hệ số của x^4 hay hệ số của x^3 lớn hơn?
8. Rút gọn biểu thức M = cos(a + b) cos(a – b) – sin(a + b) sin(a – b), ta được:
9. Cho hình chóp S.ABCD có đáy ABCD là hình bình hành. Gọi M là trung điểm của cạnh SD. Đường thẳng SB song song với mặt phẳng:
10. Cho hàm số f(x) = x^2 + sin(3x). Khi đó f′(\pi / 2) bằng:

### VI. Các trường hợp ngoại lệ hoặc cần lưu ý (xuất hiện trong lúc gán nhãn dữ liệu)