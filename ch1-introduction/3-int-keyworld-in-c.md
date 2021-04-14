---
description: "Độ khó - Dễ \U0001F31E"
---

# 1.3 - Từ khóa int trong C 🤔

Trong ngôn ngữ lập trình C, từ khóa phổ biến nhất `int` được sử dụng để xác định bất kỳ số nguyên dương hoặc số nguyên âm nào. Nhưng có một sự khác biệt giữa số nguyên và các số khác có thể được biểu diễn với sự trợ giúp của từ khóa `int`. 😃

Không phải mọi số nguyên đều có thể đều có thể hiện thị bằng từ khóa `int`. Theo `MinGW` kích thước của một `int` là `4 bytes` bằng `32bit` \(1 bytes = 8 bit\). Nó vẫn là một bí ẩn , ở đâu đó nơi mà `int` có thể đại diện cho một số nguyên hoặc `int` được sử dụng để đại diện cho các số nguyên. Số nguyên là một loại số rất lớn mà `int` có một số lượng bộ nhớ hạn chế và chính xác \(kích thước của `int` là 4 bytes hoặc 32 bit\) để lưu trữ những gì đang được đại diện bới nó. 😨

## 📒 Số nguyên có dấu

Kiểu `int` trong ngôn ngữ lập trình C có thể lưu các số cho đến `2147483647`. Ngoài con số này, `int` không được lưu trữ chính xác và thậm chí không chính xác. `int` là kiểu dữ liệu `32 bit`. Bất cứ khi nào một số được gán cho một biến loại `int`, trước tiên nó được chuyển đổi thành biểu diễn nhị phân của nó với các con số 0 và 1 và nó được lưu trữ trong bộ nhớ tại một vị trí cụ thể. Một `int` thực sự là 1 bit dấu hiệu cộng với 31 bit dữ liệu, đó là `31 bit` có sẵn để lưu trữ số được gán cho biến loại `int` và `1 bit` được dành riêng để gán dấu của số là âm \(-\) hoặc dương \(+\). Dấu cũng được biểu diễn bằng các số nhị phân với 0 là cho dương và 1 là cho âm. 😎

Để hình dung cho vấn đề trên chúng ta hãy xem qua ví dụ sau đây 😀 :

### 🎨 Ví dụ

```c
int num = 2147483647;
```

Tại thời điểm này đầu tiên số `2147483647` sẽ được chuyển đổi thành dạng nhị phân của nó là `1111111111111111111111111111111111111`. 😱

Con số `1111111111111111111111111111111111111` là một dạng nhị phân gồm 31 chữ số và sẽ được gán cho số biến thiên và nhiều nhất là 31 bit và bit thứ 32 sẽ có số `0` vì nó được gán cho biến `num` là một số dương. Nếu ta cố gắng lưu trữ một số nào lớn hơn `2147483647` thì sẽ bị mất thông tin và có thể không được lưu trữ và khi đó trình dịch của bạn có thể sẽ báo lỗi về sai kiểu dữ liệu. 😯

## 📗 Số nguyên không đấu

Trong trường hợp nếu số nguyên không có dấu, chỉ có thể lưu trữ được số nguyên dương. Trong kiểu dữ liệu này tất cả 32 bit đều được dành riêng cho việc lưu trữ dữ liệu. Do đó, giá trị tối đa có thể lưu trữ là `4294967295`. Code dùng để xác định số nguyên không dấu là `%u`.

### 🔎 Tính giá trị tối đa có thể được lưu trữ trong một số nguyên không dấu

```c
(11111111111111111111111111111111)₂ = 
(1 × 2³¹) + (1 × 2³⁰) + (1 × 2²⁹) + (1 × 2²⁸) + (1 × 2²⁷) + (1 × 2²⁶) + (1 × 2²⁵) + (1 × 2²⁴) + (1 × 2²³) + (1 × 2²²) + (1 × 2²¹) + (1 × 2²⁰) + (1 × 2¹⁹) + (1 × 2¹⁸) + (1 × 2¹⁷) + (1 × 2¹⁶) + (1 × 2¹⁵) + (1 × 2¹⁴) + (1 × 2¹³) + (1 × 2¹²) + (1 × 2¹¹) + (1 × 2¹⁰) + (1 × 2⁹) + (1 × 2⁸) + (1 × 2⁷) + 
(1 × 2⁶) + (1 × 2⁵) + (1 × 2⁴) + (1 × 2³) + (1 × 2²) + 
(1 × 2¹) + (1 × 2⁰) = (4294967295)₁₀
```

