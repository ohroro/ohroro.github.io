---
title: UI Flow KB Card
categories:
  - 'Microsoft 365'
  - 'Power Automate'
tags:
  - 'Power Automate'
  - 'UI Flow'
date: 2020-04-10 19:30:54
---
## KB Card 로그인

페이지 오픈 -> 아이디 입력 -> 비밀번호 입력까지 잘 진행됨.
그러나 비번 입력 후 로그인 버튼을 클릭하면...

![KB 01](https://user-images.githubusercontent.com/53321666/78985003-aac0e080-7b62-11ea-9986-73157ec7f4ad.png)

직접 입력하면 괜찮은데 Selenium IDE 를 사용하면 저 오류 메세지가 계속 발생

수 차례 시도하다보니

![KB 02](https://user-images.githubusercontent.com/53321666/78985007-abf20d80-7b62-11ea-82c5-00c7545aaa48.png)

이 화면을 보게되었는데 아이디 란이 정말 비어있음

분명 입력을 하였지만 로그인 버튼만 누르면 아이디 입력 된 것이 사라지는 현상...
