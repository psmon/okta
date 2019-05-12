# PHP Sample with OKTA

Prerequisites
- [Compose 기반 PHP 개발환경](https://github.com/psmon/phpstarter)

## Application LayOut - 권장 레이아웃
    /vendor - 컴포져에의해 생성된 의존성파일(커밋x)
    /public/index.php 
    /src
        /controllers
            UserController - 옥타서비스를 사용한 커스텀한 내부 컨트롤러
        /services
            OktaApiService - 옥타서비스 API 사용 스펙모음
        /views
    bootstrap.php
    .env                - 커밋x
    .env.example        - 환경설정 팁,실제 보안과 관련된 항목은 비워둠    

## 환경구성 
    //옥타 에 구성된 정보를 .env 에서 셋팅
    CLIENT_ID=어플리케이션의 고유아이디
    CLIENT_SECRET=어플리케이션 api를 사용하기위한 보안토큰
    REDIRECT_URI=http://localhost:8080/
    METADATA_URL=https://dev-146811.okta.com/oauth2/default/.well-known/oauth-authorization-server
    API_URL_BASE=https://dev-146811.okta.com/api/v1/
    API_TOKEN=가입및 패스워드초기화등을 할수 있는 토큰 (활용여부는 옵션)

## Local 구성
    //의존성 구성 : 최초한번
    composer install

    //구동
    php -S 127.0.0.1:8080 -t ./public

## 참고링크
- https://developer.okta.com/blog/2018/12/28/simple-login-php


