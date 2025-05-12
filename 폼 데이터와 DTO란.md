## 폼 데이터
HTML 요소인 form 태그에 실려 전송되는 데이터를 말한다.

## DTO(Data Transfer Object)
- <form> 태그에 실어 보낸 데이터를 <br>
  서버의 컨트롤러가 객체에 담아 전송하는데<br>
   이때의 객체를 DTO라고 한다.
- DTO로 받은 데이터는 최종적으로 DB에 저장된다.<br>

## 폼 데이터를 DTO로 받아 오기
<img src="https://github.com/user-attachments/assets/52034063-6e08-4717-8cd9-54acdc2a89b1" width="500" /><br><br>
1. 뷰 페이지를 만들고 form 태그의 action 속성으로 데이터를 어디로 보낼지(action="/.../..."),<br>
method 속성으로 데이터를 어떻게 보낼지(method="post") 정의한다.<br>
2. 컨트롤러를 만들고, PostMapping 방식으로 URL 주소를 연결한다.(@PostMapping("/~/~")<br>
3. 전송받은 데이터를 담아 둘 객체인 DTO를 만든다.<br>
4. 컨트롤러에서 폼 데이터를 전송받아 DTO에 담는다. <br>

## JPA(Java Persistence API)
<img src="https://github.com/user-attachments/assets/c40dae66-ae91-4c09-a63f-737b8048449b" width="500" /><br><br>
- 자바 언어로 DB에 명령을 내리는 도구. <br>
- 엔티티: 자바 객체를 DB가 이해할 수 있게 만든 것을로, 이를 기반으로 테이블이 만들어진다.<br>
- 리파지터리: 엔티티가 DB 속 테이블에 저장 및 관리될 수 있께 하는 인터페이스이다.<br>

## DTO2DB
<img src="https://github.com/user-attachments/assets/137ee7cd-9445-4ddc-9f62-771aea0f28b2" width="500" /><br>
-DTO를 엔티티로 변환해서, 리파지터리로 엔티티를 DB에 저장한다. <br>

## CrudRepository 인터페이스 상속 테스트
- articleRepository가 CrudRepository의 기능을 상속받아 사용할 수 있는지 알아보는 방법이 있다.
- .save(article) 부분을 지우고 articleRepository 다음에 점(.)을 찍으면 CrudRepository에서 제공하는 기능이 목록으로 뜬다.
- save 기능을 사용하므로 save를 선택하고 save()안에 article를 넣어 주면 앞서 작성한 코드와 같아진다.


