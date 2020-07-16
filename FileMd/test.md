# Tạo Project Spring Boot Hello World (intelji)
 Trên thanh menu bar chọn *File > New > Module*

 Hoặc click vào biểu tượng module trên màn hình:


 ![Figure 1-1](https://stackjava.com/wp-content/uploads/2020/06/intellij-spring-boot-0.jpg) 

 ![Figure 1-1](https://stackjava.com/wp-content/uploads/2020/06/intellij-spring-boot-1.jpg) 

Ở phần bên trái chọn loại module là Spring Initializr. Ở phần bên phải chọn bản jdk mà bạn cài trên máy.
![Figure 1-1](https://stackjava.com/wp-content/uploads/2020/06/intellij-spring-boot-2.jpg) 

Nhập các thông tin của module
![Figure 1-1](https://stackjava.com/wp-content/uploads/2020/06/intellij-spring-boot-3.jpg) 

Ở đây mình làm ví dụ hiển thị trang html với nội dung hello world nên sẽ dùng 2 thư viện là Spring Web và Thymeleaf để hiển thị
![Figure 1-1](https://stackjava.com/wp-content/uploads/2020/06/intellij-spring-boot-4.jpg) 

Chọn nơi lưu trữ module

![Figure 1-1](https://stackjava.com/wp-content/uploads/2020/06/intellij-spring-boot-5.jpg)

Kết quả:

![Figure 1-1](https://stackjava.com/wp-content/uploads/2020/06/intellij-spring-boot-6.jpg)

##Import xml


##FIle HelloworldApplication.java được tự động tạo.
*package stackjava.com.helloworld;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
@SpringBootApplication
public class HelloworldApplication {
    public static void main(String[] args) {
        SpringApplication.run(HelloworldApplication.class, args);
    }*

Spring Boot cung cấp SpringApplication class để khởi động cho ứng dụng Spring từ hàm main() sử dụng static method SpringApplicaiton.run:

@SpringBootApplication là một annotation tiện ích, nó tương đương với việc ta thêm các annotation sau:

@Configuration gán class này thành một bean của application context.
@EnableAutoConfiguration
@EnableWebMvc.
@ComponentScan.
Kể từ khi spring-boot-starter-web thêm Tomcat và Spring MVC, auto-configuration sẽ giả sử rằng bạn phát triển một ứng dụng web và sẽ setup Spring phù hợp.

 Tạo file controller.
 package stackjava.com.helloworld.controller;
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;
@Controller
public class BaseController {
    @RequestMapping("/")
    public String welcome() {
        return "index";
    }


Annotation @Controller và @RequestMapping annotations (Xem lại @Controller, @RequestMapping trong Spring MVC): sẽ tự động mapping đường dẫn / tới file index.html trong folder resources

##Tạo file view
######Tạo file index.html trong folder resources
hello word

##Chạy module
Click chuột phải vào file HelloworldApplication.java và chọn run.

*Mặc định spring web sẽ chạy trên port 8080.
Mở trình duyệt và truy cập địa chỉ localhost:8080*
![Figure 1-1](https://stackjava.com/wp-content/uploads/2020/06/intellij-spring-boot-7.jpg)
