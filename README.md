# jsp-hard
강의 : IT핥기(jsp)

url : https://www.youtube.com/playlist?list=PLpzDq-W37heSMxWj0XEVfM1rUcHBDjhm3										

## 제 1강, 첫 번째 프로젝트를 이용하여 동적서비스 개념 잡기

- jsp 설명

jsp는 http 웹 서비스하기 위한 프로그램을 만든다.

http는 request와 response로 이루어져있다.

![image](https://github.com/hsy0511/jsp-hard/assets/104752580/1a6d5c12-85b7-4047-8599-3e1a9693e4b3)

jsp 파일 하나가 아닌 전체 프로젝트를 서버(tomcat 8.0)로 실행 시킨다.

![image](https://github.com/hsy0511/jsp-hard/assets/104752580/832ae3f5-b70e-4a15-a032-570832957fe7)

프로젝트의 실행은 클라우드에서 받은 정보를 처리 한 후 서버로부터 시작된다.

![image](https://github.com/hsy0511/jsp-hard/assets/104752580/b30f6763-996a-4db4-a8e7-cf56fa7d06dc)

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



리로드 할 때 마다 결과가 바뀐다.

즉, 특정 파일을 실행하지 않고 클라우드로부터 요청받은 정보를 서버에서 응답을 해주면서 서버 페이지에 정보를 나타내는 것이다. 

이렇게 클라이언트의 요청에 따라 서버가 응답하여 다양한 화면을 제공하는 것이 동적 페이지라고 볼 수 있다.

## 제 2강, 프로젝트(Dynamic Web Project) 구조와 동적서비스 개념 이해하기

