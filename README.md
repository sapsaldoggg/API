# API 정리
method   -  uri   -   data form(example)  순서

## ---------------------LOGIN--------------------------
post - /login - {"loginId":"sad", "password":"sad"}

## ---------------------JOIN---------------------------
### * 회원가입
post - /join - 
{
    "nickname":"날아라슛돌이",
    "loginId":"xoals4340",
    "password":"111",
    "sex":"male",
    "email":"xoals@aslsa",
    "university":"한신대",
    "dept":"컴공",
    "sno":17
}

### * 아이디 중복검사
post - /duplicate-loginId - abc123(문자열)

### * 닉네임 중복검사
post - /duplicate-nickname - 날아라슛돌이(문자열)

### * 이메일 인증 (전송하기)
post - /mail-auth - xoals@hs.ac.kr(문자열)

### * 이메일 인증 (인증코드검증)
post - /mailcode-auth - 212144(문자열 or int형)






