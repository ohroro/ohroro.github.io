---
title: UI Flow Adobe Invoice PDF 출력
categories:
  - 'Microsoft 365'
  - 'Power Automate'
tags:
  - 'office365'
  - 'power automate'
  - 'ui flow'
date: 2020-04-08 17:02:33
---
* UI Flow를 이용한 Invoice 다운로드 후 발송 자동화

![adobe 03](https://user-images.githubusercontent.com/53321666/78760094-9c849000-79bb-11ea-8e80-67806a49229e.png)
Power Automate에서 Web UI flow로 녹화를 하기 위해 'Edit' 클릭

![adobe 04](https://user-images.githubusercontent.com/53321666/78760381-0d2bac80-79bc-11ea-8b9a-96d51bebdf60.png)

네모로 가린 부분은 아이디와 비밀번호 입력란.
어도비 사이트에 로그인 정보가 남아있어서 지우고 입력하다보니 'Command'라인이 늘어났었다.

이를 줄이기 위해 입력란에 바로 정보를 입력하게 수정.

![adobe 05](https://user-images.githubusercontent.com/53321666/78761178-38fb6200-79bd-11ea-816c-6917854670a7.png)

빨간색 문서 아이콘을 클릭하여 인보이스를 열어야 하는데 테스트만 하면 제대로 찾지를 못하는 현상이 자주 발생.
('입력시간' 초과라는 에러 메세지)

시간을 늘려주어도, 편집에서 위치를 새로 지정해주어도 이 에러는 계속 발생.

위치 지정 후 마우스 클릭이 아닌 키보드 엔터 입력으로 바꿔보니 에러없이 잘 실행됨!

하단의 이미지 처럼 새로운 탭에 인쇄 창이 열린다.

![adobe 01](https://user-images.githubusercontent.com/53321666/78761762-fa19dc00-79bd-11ea-80e7-f59f703e8510.png)

종이 인쇄가 아닌 PDF로 출력을 해야 하는데 여기서 또 문제 발생...

이 인쇄탭에서 'Selenium IDE' 인식이 안된다...
분명히 크롬에서 열려있는데도...

![adobe 02](https://user-images.githubusercontent.com/53321666/78762364-bbd0ec80-79be-11ea-825b-ef2786b11ab2.png)

혹시나하는 마음에 Desktop UI Flow로 시도해 봤으나 역시나 위 이미지처럼 안됨...

