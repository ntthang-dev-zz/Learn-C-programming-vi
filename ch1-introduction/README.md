---
description: Độ khó - Dễ
---

# Giới thiệu ngôn ngữ lập trình C

C là một ngôn ngữ lập trình thủ tục. Ban đầu nó được phát triển bởi Dennis Ritchie vào năm 1972. Nó chủ yếu được phát triển như một ngôn ngữ lập trình hệ thống để viết một hệ điều hành. Các tính năng chính của ngôn ngữ C bao gồm quyền truy cập cấp thấp vào bộ nhớ, một bộ từ khóa đơn giản và phong cách gọn gàng, những tính năng này làm cho ngôn ngữ C phù hợp với các lập trình hệ thống như phát triển hệ điều hành hoặc trình biên dịch.

Nhiều ngôn ngữ sau này đã vay mượn cú pháp / tính năng trực tiếp hoặc gián tiếp từ ngôn ngữ C. Giống như cú pháp của Java, PHP, JavaScript và nhiều ngôn ngữ khác chủ yếu dựa trên ngôn ngữ C. C++ gần như là một tập hợp siêu ngôn ngữ C \(Có rất ít chương trình có thể biên dịch bằng C, nhưng không phải với  C++\).

## Bắt đầu với lập trình C

### Cấu trúc của một chương trình 

Sau phần khi giới thiệu ở trên, chúng ta có thể chính thức đánh giá cấu trúc của một chương trình C, có nghĩa là bất kỳ chương trình nào cũng chỉ có thể được viết trong cấu trúc này. Viết một chương trình C trong bất kỳ cấu trúc nào khác do đó sẽ dẫn đến _Lỗi biên dịch \( Compilation Error \)_.

Cấu trúc của một chương trình C như sau:

| Thành phần cấu trúc | Ví dụ |
| :--- | :--- |
| header \( lệnh tiền xử lý \) | `#include`<stdio.h>` |
| main \( hàm chính \) | `int main() {` |
| variable \( biến \) | `int a = 10;` |
| body \( các lệnh và biểu thức \) | `printf("%d",a);` |
| return \( trả giá trị về nếu có \) | `return 0;  }` |

Các thành phần của cấu trúc trên là:

#### Header 

Thành phần đầu tiên và quan trọng nhất là bao gồm các tệp Header trong chương trình C. Tệp tiêu đề là tệp  `extension .h` trong đó chứa các khai báo hàm C và các định nghĩa `macro` sẽ được chia sẻ giữa một số tệp nguồn.

Một Header file là một file với định dạng`.h` chứa các khai báo hàm và định nghĩa marco và có thể được chia sẻ qua nhiều file nguồn. Có 2 loại Header file là : File mà lập trình viên viết ra và file đi kèm với trình biên dịch của bạn.

Bạn yêu cầu việc sử dụng Header file trong chương trình bởi việc thêm nó vào chương trình, với ký tự tiền xử lý `#include` như việc bạn thêm `stdio.h` vào phần Header file, nó sẽ đi kèm với trình biên dịch của bạn.

Việc bao gồm Header file tương đương với việc bạn sao chép nội dụng của Header file nhưng bạn không cần phải làm như thế, mà chỉ cần `#include`, code bạn sẽ gọn và đẹp hơn mà vẫn sử dụng được nội dung của Header file.

Trong thực tế chương trình C và C++ chúng ta lưu trữ hầu hết các hằng số, `marco` và biến toàn cục và các nguyên mẫu của hàm trong các Header file và `include` các file này khi bạn cần sử dụng.

Các thư viện chuẩn ANSI C

* `<assert.h>`: Bao gồm macro assert dùng để hỗ trợ trong việc phát hiện các lỗi lô-gíc và các kiểu lỗi khác trong các phiên bản dùng để tìm lỗi của một chương trình.
* `<complex.h>`: Một tập hợp các hàm dùng để điều chỉnh các số phức (mới có trong chuẩn **C99**).
* `<ctype.h>`: bao gồm các hàm dùng để phân lớp các ký tự bởi các kiểu hay dùng để chuyển đổi giữa chữ viết hoa và viết thường.
* `<errno.h>`: Dùng để thử (hay hiển thị) các lỗi được báo cáo từ các hàm thư viện.
* `<fenv.h>`: Dùng để kiểm soát môi trường chấm động (mới có trong **C99**).
* `<float.h>`: Bao gồm định nghĩa các hằng mà nêu ra các đặc tính xây dựng của thư viện chấm động, như là sự khác nhau nhỏ nhất của hai số chấm động (có thể có) qua `_EPSILON`, số *lớn nhất của các chữ số của độ chính xác qua `_DIG` và khoảng cách của các số mà có thể biểu thị được qua `_MIN` và `_MAX`.
* `<inttypes.h>`: Dùng cho việc chuyển đổi kiểu chính xác giữa các kiểu nguyên (mới có trong **C99** ).
* `<iso646.h>`: Để lập trình trong `ISO 646` cho các bộ ký tự khác nhau (mới có trong `NA1`).
* `<limits.h>`: Chứa định nghĩa các hằng có đặc tính đặc biệt của các kiểu nguyên, như là khoảng cách của các số mà có thể biểu thị quan `_MIN`, `_MAX`.
* `<locale.h>`: Dùng cho `setlocale()` và các hằng có liên quan. Việc này được dùng để lựa chọn địa phương cần thiết.
* `<math.h>`: Cho việc tính các hàm số thông dụng.
* `<setjmp.h>`: Khai báo `setjump/longjump` đưuợc dùng trong việc thoát ra của nơi không có tính địa phương.
* `<signal.h>`: Để kiểm soát các điều kiện ngoại lệ.
* `<stdarg.h>`: Để truy cập số lượng khác nhau của các đối số được chuyển vào hàm.
* `<stdbool.h>`: Dùng cho khiểu dữ liệu `Bool` (mới có trong **C99** ).
* `<stdint.h>` : Dùng trong việc định nghĩa các kiểu nguyên khác nhau (mới có trong **C99** ).
* `<stddef.h>`: Cung cấp nhiều kiểu và `macro` hữu dụng.
* `<stdio.h>`: Cung cấp cốt lõi của những khả năng nhập trong C. Tập tin này bao gồm họ hàm `printf()`.
* `<stdlib.h>`: Dùng để xúc tiến nhiều phép toán, bao gồm sự chuyển đổi, các số giả ngầu nhiên, cấp phát vùng nhớ, kiểm soát quá trình, môi trường, tín hiệu, tìm kiếm, và xếp thứ tự.
* `<string.h>`: Để điều chỉnh nhiều loại dãy ký tự.
* `<tgmath.h>`: Dùng cho các hàm toán kiểu thông dụng (mới có trong **C99** ).
* `<time.h>`: Để chuyển đổi giữa các định dạng khác nhau về thì giờ và ngày tháng.
* `<wchar.h>`: Để điều chỉnh độ rộng của các dòng (dữ liệu) và nhiều loại dãy ký tự sử dụng nhiều (loại) ký tự có độ lớn (Unicode chẳng hạn). -- Đây là chìa khóa để hỗ trợ nhiều ngôn ngữ (mới có trong `NA1` ).
* `<wctype.h>`: Để phân lớp các ký tự có độ lớn (mới có trong `NA1` ).

#### Cú pháp include header file trong C

```c
// Syntax to include a header file in C:
#include
```

#### Khai báo hàm chính

Phần tiếp theo của một chương trình C là khai báo hàm chính (hay còn được gọi là hàm `main()`. Cú pháp định nghĩa hàm `main()` là:

```c
// Syntax to Declare main method:
int main()
{}
```

#### Khai báo biến

Phần kế tiếp của bất cứ chương trình C nào đó chính là khai báo biến. Nó đề cập đến các biến sẽ được sử dụng trong hàm. Xin lưu ý rằng trong chương trình C, không có biến nào có thể được sử dụng mà không được khai báo. Ngoài ra trong một chương trình C, các biến sẽ được khai báo trước bất kỳ hoạt động nào trong hàm.

```c
int main()
{
    // Variable Declaration
    int a;
.
.
```

#### Phần thân

```c
 int main()
 {
    int a;

    // Body
    printf("%d", a);
.
.
```

#### Trả giá trị

Phần cuối cùng trong bất kỳ chương trình C nào là câu lệnh `return`. Câu lệnh `return` đề cập đến việc trả về các giá trị từ một hàm. Câu lệnh trả về và giá trị trả về này phụ thuộc vào kiểu trả về của hàm. Ví dụ, nếu kiểu trả về là `void`, thì sẽ không có câu lệnh trả về. Trong bất kỳ trường hợp nào khác, sẽ có một câu lệnh trả về và giá trị trả về sẽ thuộc loại kiểu trả về được chỉ định.

```c
int main()
{
    int a;

    printf("%d", a);

    // Return
    return 0;
}
```

## Chương trình đầu tiên

Sau đây là chương trình đầu tiên trong C

```c
#include `<stdio.h>` 
int main(void) 
{ 
    printf("C-For-Beginners"); 
    return 0; 
}
```

Hãy cùng tôi phân tích chương trình từng dòng.

### Dòng 1: `#include `<stdio.h>`

Trong chương trình C, tất cả các dòng bắt đầu bằng `#` đều được xử lý bởi [bộ tiền xử lý - preprocessor](https://en.wikipedia.org/wiki/C_preprocessor) là một chương trình được gọi bởi trình biên dịch. Trong một thuật ngữ rất cơ bản, [bộ tiền xử lý](https://en.wikipedia.org/wiki/C_preprocessor) lấy một chương trình C và tạo ra một chương trình C khác. Chương trình đã tạo không có dòng nào bắt đầu bằng `#`, tất cả các dòng như vậy đều được xử lý bởi bộ tiền xử lý. Trong ví dụ trên, bộ xử lý trước sao chép mã được xử lý trước của `stdio.h` vào tệp của tôi. Các tệp `.h` được gọi là tệp tiêu đề (header file) trong C. Các tệp tiêu đề này thường chứa khai báo các hàm. Các tệp `.h` được gọi là tệp tiêu đề (header file) trong C. Các tệp tiêu đề này thường chứa khai báo các hàm. Ta cần `stdio.h` cho hàm `printf()` đã được sử dụng trong chương trình trên.

### Dòng 2: `int main(void)`

Điểm bắt đầu từ nơi bắt đầu thực thi chương trình C đã biên dịch. Trong C, việc thực thi thường bắt đầu bằng dòng đầu tiên của `main ()`. Khoảng trống được viết trong ngoặc cho biết rằng main không nhận bất kỳ tham số nào .`main ()` cũng có thể được viết để nhận các tham số. Chúng tôi sẽ đề cập đến vấn đề đó trong các bài viết trong tương lai.

`int` được viết trước main cho biết kiểu trả về của` main () `. Giá trị được trả về (return) bởi `main` cho biết trạng thái kết thúc chương trình. 

### Dòng 3 và 6: `{and}`

Trong ngôn ngữ C, một cặp dấu ngoặc nhọn xác định phạm vi và chủ yếu được sử dụng trong các hàm và câu lệnh điều khiển như vòng lặp `if`, `else`, ... Tất cả các hàm phải bắt đầu và kết thúc bằng dấu ngoặc nhọn.

### Dòng 4: `printf("C-For-Beginners")`

[`printf()`](http://www.cplusplus.com/reference/cstdio/printf/) là một chức năng thư viện tiêu chuẩn để in thứ gì đó trên đầu ra tiêu chuẩn. Dấu chấm phẩy ở cuối `printf` cho biết kết thúc dòng. Trong C, dấu chấm phẩy luôn được sử dụng để biểu thị kết thúc câu lệnh.

### Dòng 5: `return 0;`

Inorder để thực thi chương trình trên, chúng ta cần có một trình biên dịch để biên dịch và chạy các chương trình của mình. Có một số trình biên dịch trực tuyến nhất định như [http://ideone.com/](http://ideone.com/) hoặc [http://codepad.org/](http://codepad.org/) có thể được sử dụng để khởi động C mà không cần cài đặt trình biên dịch.

#### Windows:

Có rất nhiều trình biên dịch có sẵn miễn phí để biên dịch các chương trình C như Code Blocks, Dev-CPP hay VS Code. Tôi thường xử dụng VS Code cho công việc của mình.

#### Linux:

Dành cho Linux, [gcc](https://en.wikipedia.org/wiki/GNU_Compiler_Collection) comes bundled with the linux, Code Blocks can also be used with Linux.

