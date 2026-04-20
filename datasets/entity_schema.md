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
| PROPERTY | Các từ chỉ các tính chất hay mối quan hệ giữa các đối tượng | Vuông góc, song song,... |
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
    - Hình O
    - nào O
    - dưới O
    - đây O
    - biểu O
    - diễn O
    - miền B-MATH_CONCEPT
    - nghiệm I-MATH_CONCEPT
    - của O
    - bất B-MATH_CONCEPT
    - phương I-MATH_CONCEPT
    - trình I-MATH_CONCEPT
    - x B-EQUATION
    - \- I-EQUATION
    - y I-EQUATION
    - < I-EQUATION
    - 3 I-EQUATION
    - ? O

3. Cho tam giác ABC có \hat(B) = 60 \deg, \hat(C) = 45 \deg, AC = 10. Tính a, R, S, r.
    - Cho O
    - tam B-GEOMETRIC_SHAPE
    - giác I-GEOMETRIC_SHAPE
    - ABC B-GEOMETRIC_INSTANCE
    - có O
    - \hat B-GEOMETRIC_INSTANCE
    - ( I-GEOMETRIC_INSTANCE
    - B I-GEOMETRIC_INSTANCE
    - ) I-GEOMETRIC_INSTANCE
    - = O
    = 60 O
    - \deg O
    - , O
    - \hat B-GEOMETRIC_INSTANCE
    - ( I-GEOMETRIC_INSTANCE
    - C I-GEOMETRIC_INSTANCE
    - ) I-GEOMETRIC_INSTANCE
    - = O
    - 45 O
    - \deg O
    - , O
    - AC B-GEOMETRIC_INSTANCE
    - = O
    - 10 O
    - . O
    - Tính O
    - a B-SYMBOL
    - , 0 
    - R B-SYMBOL
    - , O
    - S B-SYMBOL
    - , O
    - r B-SYMBOL
    - . O

    Ghi chú 2: ở đây 50 độ hay 45 độ đóng vai trò tương tự như các số nên sẽ không gán nhãn (nguyên tắc 3).  
    Ghi chú 3: các kí hiệu như a, R, S, r thật ra có ý nghĩa xác định trong ngữ cảnh nhưng ta vẫn sẽ coi nó như các kí hiệu toán học chung chung khác (nguyên tắc 6).

4. Cho hình bình hành ABCD. Chứng minh rằng với mọi điểm M, ta có: \vector(MA) + \vector(MC) = \vector(MB) + \vector(MD).
    - Cho O
    - hình B-GEOMETRIC_SHAPE
    - bình I-GEOMETRIC_SHAPE
    - hành I-GEOMETRIC_SHAPE
    - ABCD B-GEOMETRIC_INSTANCE
    - . O
    - Chứng O
    - minh O
    - rằng O
    - với O
    - mọi O
    - điểm B-GEOMETRIC_OBJECT
    - M B-GEOMETRIC_INSTANCE
    - , O
    - ta O
    - có O
    - : O
    - \vector B-EQUATION
    - ( I-EQUATION
    - MA I-EQUATION
    - ) I-EQUATION
    - \+ I-EQUATION
    - \vector I-EQUATION
    - ( I-EQUATION
    - MC I-EQUATION
    - ) I-EQUATION
    - = I-EQUATION
    - \vector I-EQUATION
    - ( I-EQUATION
    - MB I-EQUATION
    - ) I-EQUATION
    - \+ I-EQUATION
    - \vecto I-EQUATION
    - ( I-EQUATION
    - MD I-EQUATION
    - ) I-EQUATION
    - . O

5. Parabol y = - x^2 + 2x + 3 có đỉnh là:
    - Parabol B-GEOMETRIC_OBJECT
    - y B-EQUATION
    - = I-EQUATION
    - \- I-EQUATION
    - x I-EQUATION
    - ^ I-EQUATION
    - 2 I-EQUATION
    - \+ I-EQUATION
    - 2 I-EQUATION
    - x I-EQUATION
    - \+ I-EQUATION
    - 3 I-EQUATION
    - có O
    - đỉnh B-GEOMETRIC_OBJECT
    - là O
    - : O

    Ghi chú 4: Ta quy ước FUNCTION phải có kí hiệu f(x) hoặc các kí hiệu tương tự nên các (bất) phương trình biểu diễn các đối tượng trên đồ thị hàm số nếu không thỏa mãn vẫn sẽ xếp vào EQUATION (nguyên tắc 6).

6. Phương trình nào sau đây là phương trình tham số của đường thẳng?
    - Phương B-MATH_CONCEPT
    - trình I-MATH_CONCEPT
    - nào O
    - sau O
    - đây O
    - là O
    - phương B-MATH_CONCEPT
    - trình I-MATH_CONCEPT
    - tham I-MATH_CONCEPT
    - số I-MATH_CONCEPT
    - của O
    - đường B-GEOMETRIC_OBJECT
    - thẳng I-GEOMETRIC_OBJECT
    - ? O

7. Trong khai triển nhị thức Newton của (2x + 3)^5, hệ số của x^4 hay hệ số của x^3 lớn hơn?
    - Trong O
    - khai O
    - triển O
    - nhị B-THEOREM
    - thức I-THEOREM
    - Newton I-THEOREM
    - của O
    - ( B-EXPRESSION
    - 2 I-EXPRESSION
    - x I-EXPRESSION
    - \+ I-EXPRESSION
    - 3 I-EXPRESSION
    - ) I-EXPRESSION
    - ^ I-EXPRESSION
    - 5 I-EXPRESSION
    - , O
    - hệ B-MATH_CONCEPT
    - số I-MATH_CONCEPT
    - của O
    - x B-EXPRESSION
    - ^ I-EXPRESSION
    - 4 I-EXPRESSION
    - hay O
    - hệ B-MATH_CONCEPT
    - số I-MATH_CONCEPT
    - của O
    - x B-EXPRESSION
    - ^ I-EXPRESSION
    - 3 I-EXPRESSION
    - lớn O
    - hơn 0
    - ? O

8. Rút gọn biểu thức M = cos(a + b) cos(a - b) - sin(a + b) sin(a - b), ta được:
    - Rút O
    - gọn O
    - biểu B-MATH_CONCEPT
    - thức I-MATH_CONCEPT
    - M B-SYMBOL
    - = O
    - cos B-EXPRESSION
    - ( I-EXPRESSION
    - a I-EXPRESSION
    - \+ I-EXPRESSION
    - b I-EXPRESSION
    - ) I-EXPRESSION
    - cos I-EXPRESSION
    - ( I-EXPRESSION
    - a I-EXPRESSION
    - \- I-EXPRESSION
    - b I-EXPRESSION
    - ) I-EXPRESSION
    - \- I-EXPRESSION
    - sin I-EXPRESSION
    - ( I-EXPRESSION
    - a I-EXPRESSION
    - \+ I-EXPRESSION
    - b I-EXPRESSION
    - ) I-EXPRESSION
    - sin I-EXPRESSION
    - ( I-EXPRESSION
    - a I-EXPRESSION
    - \- I-EXPRESSION
    - b I-EXPRESSION
    - ) I-EXPRESSION
    - , O
    - ta O
    - được O
    - : O

9. Cho hình chóp S.ABCD có đáy ABCD là hình bình hành. Gọi M là trung điểm của cạnh SD. Đường thẳng SB song song với mặt phẳng:
    - Cho O
    - hình B-GEOMETRIC_SHAPE
    - chóp I-GEOMETRIC_SHAPE
    - S.ABCD B-GEOMETRIC_INSTANCE
    - có O
    - đáy B-GEOMETRIC_OBJECT
    - ABCD B-GEOMETRIC_INSTANCE
    - là O
    - hình B-GEOMETRIC_SHAPE
    - bình I-GEOMETRIC_SHAPE
    - hành I-GEOMETRIC_SHAPE
    - . O
    - Gọi O
    - M B-GEOMETRIC_INSTANCE
    - là O
    - trung B-GEOMETRIC_OBJECT
    - điểm I-GEOMETRIC_OBJECT
    - của O
    - cạnh B-GEOMETRIC_OBJECT
    - SD B-GEOMETRIC_INSTANCE
    - . O
    - Đường B-GEOMETRIC_OBJECT
    - thẳng I-GEOMETRIC_OBJECT
    - SB B-GEOMETRIC_INSTANCE
    - song B-PROPERTY
    - song I-PROPERTY
    - với O
    - mặt B-GEOMETRIC_OBJECT
    - phẳng I-GEOMETRIC_OBJECT
    - : O
10. Cho hàm số f(x) = x^2 + sin(3x). Khi đó f'(\pi / 2) bằng:
    - Cho O
    - hàm B-MATH_CONCEPT
    - số B-MATH_CONCEPT
    - f B-FUNCTION
    - ( I-FUNCTION
    - x I-FUNCTION
    - ) I-FUNCTION
    - = I-FUNCTION
    - x I-FUNCTION
    - ^ I-FUNCTION
    - 2 I-FUNCTION
    - \+ I-FUNCTION
    - sin I-FUNCTION
    - ( I-FUNCTION
    - 3 I-FUNCTION
    - x I-FUNCTION
    - ) I-FUNCTION
    - . O
    - Khi O 
    - đó O
    - f B-FUNCTION
    - ′ I-FUNCTION
    - ( I-FUNCTION
    - \pi I-FUNCTION
    - / I-FUNCTION
    - 2 I-FUNCTION
    - ) I-FUNCTION
    - bằng O
    - : O
    
    Ghi chú 5: f′(\pi / 2) ở đây là chỉ 1 giá trị cụ thể của hàm số, giống như một biểu thức hơn nhưng ta vẫn sẽ xếp vào FUNCTION (nguyên tắc 2).

### VI. Các trường hợp ngoại lệ hoặc cần lưu ý (xuất hiện trong lúc gán nhãn dữ liệu)
- \pi: SYMBOL - tuy có giá trị xác định nhưng vì lầ một hằng số có kí hiệu riêng nên ta vẫn gán \pi nhãn SYMBOL.
- p => Q: EXPRESSION - thực chất đây là một mệnh đề chứ không phải biểu thức nhưng sẽ được gộp chung vào đây để giữ cho P => Q là một thực thể.
- n(A) = 6: EQUATION - coi như là một phép tính thông thường.
- A \intersection B : EXPRESSION - vì ở đây phép giao có thể coi như có thực hiện tính toán thay vì là khai báo (như A \in B).
- A \intersection B = \emptyset: EQUATION - vì đây không phải phép gán/khai báo nên vẫn sẽ gán nhãn EQUATION để đảm bảo tính đồng nhất.
- C _ U A (phần bù của A trong U): EXPRESSION.
- Cặp số: nếu là dạng (x; y) thì sẽ gán nhãn x và y là SYMBOL còn là dạng (1; 2) thì toàn bộ gán là O.
- Dạng A = B => C = D: "A = B" và "C = D" gán là EQUATION, "=>" không gán nhãn.