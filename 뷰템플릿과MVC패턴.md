## 뷰 템플릿(View Template)
- 화면을 담당하는 기술
- 웹 페이지(View)를 하나의 틀(Template)로 만들고 <br> 여기에 변수를 삽입해 서로 다른 페이지를 보여준다.
- Spring에서는 뷰 템플릿을 만들기 위한 도구로 머스테치(Mustache) 등이 있다.
- 간단히 '뷰'라고도 한다.

## MVC패턴
<img src="https://github.com/user-attachments/assets/7b5aec7e-c0ad-45db-8def-05b1842f41c5" width="500" /> <br>
`   스프링 부트3 자바 백엔드 개발 입문(Book) 자료  `
- 모델(Model)은 데이터를 관리하는 역할이다.
- 뷰(View)는 컨트롤러와, 모델이라는 두 동료가 있다.
- 컨트롤러(Controller)는 **클라이언트의 요청**에 따라, <br>서버에서 이를 처리하는 역할이다.

# 실습
1. 뷰 페이지 만들기 greetings.mustache
2. 컨트롤러 만들기 FirstController.java
3. 컨트롤러에서 뷰 페이지 반환하기 return "greetings";
4. 뷰 페이지에 변수 삽입하기 {{username}}
5. 컨트롤러에 모델 추가하기 niceToMeetYou(Model model)
6. 모델에서 변수 등록하기 model,addAttribute("username","홍팍");

# /hi 페이지의 실행 흐름
```Java
@Controller //1. 컨트롤러 선언
publlic class FirstController {
  @GetMapping("/hi") //2. URL 요청 접수


  public String niceToMeetYou(Model model) { // 3.메서드 수행, 4. 모델 객체 수행
    model.addAttribute("username", "hongpark"); //5. 모델 변수 등록
    return "greetings"; //뷰 템플릿 페이지 반환
  }
}
```
