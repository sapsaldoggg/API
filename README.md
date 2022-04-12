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

## --------------------식당--------------------------
### * 식당목록 조회
get - /user/restaurants 
response =>   
{
        "id": 1,
        "name": "그라찌에 한신대경삼관점\r",
        "category": "카페",
        "address": "경기 오산시 양산동 400",
        "longtitude": 127.0240311,
        "latitude": 37.19410415
        } 
(리스트 형식)
    

## -------------------파티----------------------------
### * 파티목록조회
get - /user/restaurant/{restaurant_id}/parties 

### * 파티 생성
post - /user/restaurant/{restaurant_id}/party

### * 파티 참가
post - /user/restaurant/{restaurant_id}/party/{party_id}

### * 파티 삭제
delete - /user/restaurant/{restaurant_id}/party/{party_id}

### * 파티 수정
put - /user/restaurant/{restaurant_id}/party/{party_id}







