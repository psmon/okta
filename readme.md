# OKTA with SSO

옥타를 이용한, 커스텀하게 제작된 어플리케이션의 파편화된 로그인을 
플랫폼별로 통합하는 방법입니다. OKTA의 공식문서를 참고하여 작동가능 하고
활용을 검증을 하는 활동의 소스입니다.

## OKTA 사용비용
Link :https://developer.okta.com/pricing/
- 0$ :Up to 1,000 Mau(monthly active users)
- 50$ : 2,500 Mau
- 100$ : 500 Mau

Active Users의 의미는, 해달 일에 한번이라도 사용하면 1이 발생

즉 근무일에, 하루도 빠트리지 않고 꾸준히 사용해야 한달 Maus가 나옴
40명 * 23일 =920Mau
100명 *23 = 2300Mau

50미만의 회사는 공짜라는 의미로 해석될수 있음 
100명 규모에서 한달 50$ 정도의 비용예상할수 있음
전반적으로 로그인 통합/보안강화를 위해 서버를 별도로 구축하고 운영하는 비용보다 저렴함 

## 준비하기

- 개발자 계정 생성 : https://developer.okta.com/signup/
- 데브 계정이 주어짐 : dev-17xxx
- 관리자 페이지가 추가됨 :dev-dev-17xxx-admin.okta.com

## 어플리케이션 생성 - Okta Admin
- 생성 : Applications탭 -> AddApplication(WebApp)
- 주요설정 : baseurl , loginredirect
- 키 : Client ID , Client SecretKey

## 플랫폼별
- [php-here](/php)
- [php-more](https://github.com/oktadeveloper?utf8=%E2%9C%93&q=php&type=&language=)
- [.net core](https://github.com/oktadeveloper/okta-aspnetcore-mvc-example)
- [spring boot](https://github.com/okta/samples-java-spring)