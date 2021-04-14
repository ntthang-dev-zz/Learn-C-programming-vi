---
description: "Độ khó - Dễ \U0001F31E"
---

# 1.4 - void main\(\) hay main\(\) trong C 😵

Định nghĩa :

```cpp
void main()
{ /* ... */ }
```

Không phải hoặc chưa phải bao giờ là `C++`, thậm chí chưa phải là `C`. Xem tiêu chuẩn [ISO C++ 3.6.1]() hoặc tiêu chuẩn [ISO C 5.1.2.2.1](). Một kiểu triển khai tuân thủ theo 

```cpp
int main ()
{ /* ... */ }
```

và 

```cpp
int main(int argc, char* argv[])
{ /* ... */ }
```

Việc triển khai theo quy tắc có nhiều phiên bản của `main()`, nhưng tất cả chúng đểu có kiểu trả về là `int`. Giá trị `int` được trả về bởi `main()` là một cách để chương trình trả về một giá trị cho *hệ thống* gọi nó. Trên các hệ thống không cung cấp các phương thức như vậy, gía trị trả về sẽ bị bỏ qua, nhưng điều đó không làm cho `void main()` hợp pháp trong `C++` hoặc `C`.

***Ngay cả khi trình biên dịch của bạn chấp nhận `void main()`, hãy tránh nó hoặc rủi ro bị các lập trình viên `C` và `C++` coi là ngu dốt. Trong `C++`, `main()` không cần phải chứa câu lệnh trả về rõ ràng. Trong trường hợp đó, giá trị trả về bằng 0, nghĩa là thực hiện thành công.***

## 🎨 Ví dụ

```cpp
#include <iostream>
int main()
{
    std::cout
        << "This program returns the value integer value 0\n";
}
```

Cũng lưu ý rằng cả `ISO C++` và `C99` đầu không cho phép bạn bỏ loại khai báo. Nghĩa là, trái ngược với `C89` và `ARM C++`, `int` không được giải định khi thiếu một kiểu trong khai báo.

Hệ quả là :

```cpp
#include <iostream>

main()
{ /* ... */ }
```

Đoạn mã trên không có lỗi. Nếu bạn viết các 