
1. Vai trò và mối quan hệ giữa JDK, JRE và JVM
   JDK (Java Development Kit)

- Bộ công cụ dành cho lập trình viên Java, cung cấp tất cả các công cụ cần thiết để phát triển ứng dụng (bao gồm trình biên dịch javac, trình gỡ lỗi, tài liệu, v.v.).
Thành phần: Bao gồm JRE (môi trường chạy Java) và các công cụ phát triển khác.
Sử dụng: Dành cho nhà phát triển khi viết, biên dịch và gỡ lỗi ứng dụng Java.
JRE (Java Runtime Environment)

- Cung cấp môi trường để chạy các ứng dụng Java.
Thành phần: Gồm có JVM cùng với các thư viện, lớp chuẩn cần thiết để thực thi chương trình Java.
Sử dụng: Dành cho người dùng chỉ cần chạy các ứng dụng Java mà không cần phát triển.
JVM (Java Virtual Machine)

- Là "máy ảo" chịu trách nhiệm chạy bytecode của Java. Nó chuyển đổi bytecode thành mã máy của hệ điều hành cụ thể và quản lý bộ nhớ, xử lý đa luồng, bảo mật,…
Đặc điểm: Là thành phần cốt lõi giúp đạt được tính di động của Java (xem phần “Write once, run anywhere”).

Mối quan hệ: JDK chứa JRE, và JRE lại bao gồm JVM. Khi bạn phát triển ứng dụng Java, bạn cần JDK; khi chạy ứng dụng, máy tính cần có JRE (và do đó là JVM).
2. Khái niệm "Write once, run anywhere" và cơ chế đa nền tảng của Java
   Ý nghĩa:

"Write once, run anywhere" (WORA) có nghĩa là bạn chỉ cần viết mã nguồn Java một lần và sau đó có thể chạy trên bất kỳ hệ điều hành nào có cài đặt JVM mà không cần thay đổi hay biên dịch lại mã nguồn.
Cơ chế hỗ trợ:

Khi biên dịch, mã nguồn Java được chuyển thành bytecode – một dạng mã trung gian không phụ thuộc vào nền tảng.
JVM sẽ giải thích (hoặc biên dịch tại thời điểm chạy bằng JIT – Just-In-Time Compiler) bytecode đó thành mã máy phù hợp với hệ điều hành và phần cứng đang chạy.
Nhờ có lớp trừu tượng của JVM, sự khác biệt về kiến trúc phần cứng và hệ điều hành được ẩn đi, cho phép cùng một bytecode chạy được trên nhiều nền tảng khác nhau.
3. Quy trình cài đặt và chạy chương trình Java đầu tiên bằng IntelliJ IDEA
   Cài đặt môi trường:

Tải và cài đặt JDK:
Truy cập trang chủ Oracle hoặc sử dụng các bản phân phối khác (OpenJDK) để tải phiên bản JDK phù hợp.
Cài đặt IntelliJ IDEA:
Tải IntelliJ IDEA từ trang web của JetBrains và cài đặt theo hướng dẫn.
Tạo dự án Java mới:

Mở IntelliJ IDEA và chọn "New Project".
Chọn "Java" trong danh sách dự án, đảm bảo chọn đúng phiên bản JDK đã cài đặt.
Đặt tên và đường dẫn cho dự án, sau đó nhấn "Finish".
Tạo lớp chứa hàm main:

Trong cửa sổ dự án, chuột phải vào thư mục src → chọn "New" → "Java Class".
Đặt tên cho lớp, ví dụ: Main.
Thêm hàm main vào lớp:
java
Sao chép
Chỉnh sửa

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, Java!");
    }
}

```
Chạy chương trình:

Nhấn chuột phải vào file Main.java → chọn "Run 'Main.main()'".
Kết quả sẽ hiển thị trong cửa sổ Run với thông điệp "Hello, World!".
Kiểm tra và gỡ lỗi:

Sử dụng tính năng Debug (nhấn Shift + F9 trên Windows/Linux hoặc ⌥ + F9 trên Mac) nếu cần gỡ lỗi chương trình.
4. Các phiên bản Java: Java SE, Java EE và Java ME
   Java SE (Standard Edition):

| Phiên bản  | Mục đích sử dụng | Đối tượng hướng đến | Các thành phần chính |
|------------|----------------|------------------|----------------|
| **Java SE** (Standard Edition) | Phát triển ứng dụng Java cơ bản, desktop, console | Ứng dụng độc lập (Standalone), phần mềm máy tính | Core Java (JVM, JDK, JRE), Swing, JavaFX, JDBC, Collection, Multithreading |
| **Java EE** (Enterprise Edition) | Phát triển ứng dụng web, ứng dụng doanh nghiệp | Ứng dụng web, hệ thống doanh nghiệp lớn, dịch vụ web | Servlets, JSP, EJB, JPA, JTA, JMS, REST, SOAP |
| **Java ME** (Micro Edition) | Phát triển ứng dụng trên thiết bị di động, nhúng | Điện thoại cũ, hệ thống nhúng, thiết bị IoT | MIDP, CLDC, CDC, API cho thiết bị di động |


