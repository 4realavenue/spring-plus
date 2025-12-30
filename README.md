# 프로젝트 명 : Spring 플러스 주차 개인 과제

# 사용 기술 스택 / 버전
- Java 17
- Spring Boot '3.3.3'

# 사용법
  
## Auth

### Auth
- 회원가입
[POST] /auth/signup
```
{
   "nickname" : "String",
   "email" : "String",
   "password" : "String",
   "userRole" : "userRole"
}
```

- 로그인
[POST] /auth/signin
```
{
   "email" : "String",
   "password" : "String"
}
```

## User (users)
- id (GenerationType.IDENTITY) : 유저의 고유 식별자
- nickname : 유저의 닉네임
- email : 유저의 이메일
- password : 유저의 비밀번호
- userRole (enum : USER / ADMIN) : 유저의 권한

### UserAdmin
- 유저의 권한 변경
[PATCH] /admin/users/{userId}

### User
- 유저 단건 조회
[GET] /users/{userId}

- 유저 비밀번호 수정
[PUT]


## Todo (todos)
- id (GenerationType.IDENTITY) : 일정의 고유 식별자
- title : 일정 제목
- contents : 일정 내용
- weather : 일정 작성 당시 날씨

### Todo
- 일정 생성
[POST] /todos
```
{
   "title" : "String",
   "contents" : "String"
}
```

- 일정 전체 조회 (유저의)
[GET] /todos

- 일정 단건 조회 (유저의)
[GET] /todos/{todoId}

## Comment (comments)
- id (GenerationType.IDENTITY) : 댓글의 고유 식별자
- contents : 댓글의 내용

### Comment
- 댓글 생성
[POST] /todos/{todoId}/comments
```
{
   "contents" : "String"
}
```

- 댓글 조회
[GET] /todos/{todoId}/comments


















