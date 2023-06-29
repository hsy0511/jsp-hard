# jsp-hard
강의 : IT핥기(jsp)

url : https://www.youtube.com/playlist?list=PLpzDq-W37heSMxWj0XEVfM1rUcHBDjhm3										

## 제 1강, 동적서비스와 정적서비스

### 정적 서비스

정적(static)은 외부 환경에 관계 없이 일정한 결과값을 제공해주는 걸 의미합니다.

![image](https://github.com/hsy0511/rest-api/assets/104752580/f6c5486b-d1ad-4e18-94a9-a97adba342dd)

정적 서비스는  웹 서버와 통신해서 이미 저장되어 있던 HTML, CSS, JS 파일을 다운 받는다.  

여기서 웹 서버는 HTML, CSS, JS 저장소 역할을 한다.

따로 데이터베이스가 필요하거나 복잡한 비즈니스 로직이 필요하지 않다.


### 동적 서비스

동적(dynamic)은 외부 환경에 따라 다른 결과값을 제공해주는 걸 뜻해요. 

![image](https://github.com/hsy0511/rest-api/assets/104752580/f0e2a99f-46ed-4f43-976d-e91b62398462)

동적 서비스는 클라이언트의 요청에 따라 다양한 화면을 제공해 준다.

웹 어플리케이션 서버와 직접 통신을 한다.

웹 어플리케이션 서버(WAS)는 복잡한 비즈니스 로직, 데이터 베이스와 통신 등을 책임진다.

웹 서버는 WAS와 통신해서 얻은 결과 값을 바탕으로 가공 작업을 거친다. 

최종적으로 만들어진 동적인 웹 파일을 클라이언트에게 전달해 준다. 

기본적으로 동적 웹은 정적 웹에 비해 복잡한 로직들과 리소스를 필요로 한다.

### 참고

웹 어플리케이션 서버는 일종의 API 서버라고 볼 수도 있다.

왜냐하면 데이터베이스와 통신하며 데이터를 가공하고 전달해주는 역할도 하기 때문이다.

## 제 2강, 첫 번째 프로젝트를 이용하여 동적서비스 개념 잡기

- jsp 설명

jsp는 http 웹 서비스하기 위한 프로그램을 만든다.

http는 request와 response로 이루어져있다.

![image](https://github.com/hsy0511/jsp-hard/assets/104752580/1a6d5c12-85b7-4047-8599-3e1a9693e4b3)

jsp 파일 하나가 아닌 전체 프로젝트를 서버(tomcat 8.0)로 실행 시킨다.

![image](https://github.com/hsy0511/jsp-hard/assets/104752580/832ae3f5-b70e-4a15-a032-570832957fe7)

프로젝트의 실행은 클라우드에서 받은 정보를 처리 한 후 서버로부터 시작된다.

![image](https://github.com/hsy0511/jsp-hard/assets/104752580/171d3314-46b8-49cc-8dfe-63603021da01)


- 첫번째 예제 프로젝트

```jsp
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>현재시간</title>
</head>
<body>
첫번째 예제 <br>
현재 시간은 <%= new java.util.Date() %>
</body>
</html>
```

![image](https://github.com/hsy0511/jsp-hard/assets/104752580/bda051ff-80e0-4de5-93fa-6ca41b3dbdf4)

웹 서버에서 리로드를 할 때마다 정보가 달라지는 것을 볼 수 있다.

즉, 클라이언트의 요청에 따라 서버가 응답하여 다양한 화면을 제공하는 것이 동적 페이지라고 볼 수 있다.

## 제 3강, 동적서비스 개념 이해하기

