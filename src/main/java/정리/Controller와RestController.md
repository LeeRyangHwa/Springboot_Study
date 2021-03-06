출처: https://medium.com/devAsterisk/spring-boot-%EA%B8%B0%EB%B0%98-rest-api-%EC%A0%9C%EC%9E%91-2-79c484fcadbe

##Controller와 RestController 차이
전통적인 spring MVC의 컨트롤러인 @Controller와 
Restuful 웹 서비스의 컨트롤러인 @RestController의 차이점 
    
    HTTP Response Body가 생성되는 방식이다


###@Controller
- 주로 View를 반환하기 위해 사용
    1. Client는 URL 형식으로 웹 서비스에 요청을 보낸다.
    2. Mapping되는 Handler와 그 Type을 찾는 DispatcherServlet이 요청을 인터셉트한다.
    3. Controller가 요청을 처리한 후에 응답을 DispatcherServlet으로 반환하고, DispatchetServlet은 View를 사용자에게 반환한다.

- Data를 반환해야하는 경우
    - SpringMVC의 컨트롤러에서는 데이터를 반환하기 위해 @ResponseBody 어노테이션을 활용
    1. Client는 URL 형식으로 웹 서비스에 요청을 보낸다.
    2. Mapping 되는 Handler와 그 Type을 찾는 DispatcherServlet이 요청을 인터셉트한다.
    3. @ResponseBody를 사용하여 Client에게 Json형태로 데이터를 반환한다.


###@RestController
- Spring MVC Controller에 @ResponseBody가 추가된 것
- 주용도는 Json/Xml 형태로 객체 데이터를 반환하는 것  
(VueJS + SpringBoot 프로젝트를 진행할 때 SpringBoot를 API 서버로 활욜 할 때, Android 앱 개발을 하면서 데이터를 반환할 때 사용)



[]: https://medium.com/