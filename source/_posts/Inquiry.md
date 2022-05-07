---
title: Inquiry Automate
categories:
  - 'Microsoft 365'
  - 'Power Automate'
tags:
  - 'Power Automate'
  - 'MS Forms'
  - 'SharePoint'
  - 'Teams'
date: 2020-05-24 22:04:22
---

## 고객 문의 정리 및 알림

문의 내용이 접수 되었을 시 Share Point List를 활용하여 자동입력 및 모든 문의내용을 한곳으로 모이게 하고 바로 알림을 보내어 내용을 공유해보도록 합니다.

![inquiry 02](https://user-images.githubusercontent.com/53321666/82900887-256d8000-9f98-11ea-8aa9-25c7d9a85589.png)

 MS Forms를 이용하여 고객문의 입력 화면을 만들었고 Forms를 Wordpress 안에 넣어놓았습니다.

----------------------

![inquiry 03](https://user-images.githubusercontent.com/53321666/82900889-26061680-9f98-11ea-8b4b-db0509a515e8.png)

고객이 내용 작성 후 '제출'을 클릭하면 이 내용을 자동으로 입력되게 할 것입니다.

------------------------------
![inquiry 01](https://user-images.githubusercontent.com/53321666/82900886-24d4e980-9f98-11ea-8f6a-73da0b4c26c3.png)

우선 문의 접수를 저장하기 위해 Share Point에 새로운 List를 생성합니다.

--------------------
![inquiry 04](https://user-images.githubusercontent.com/53321666/82900891-26061680-9f98-11ea-9c92-973cc0f08750.png)

접수받는 Forms와 연동될 수 있게 동일한 내용으로 만들어줍니다.

---------------------
![inquiry 05](https://user-images.githubusercontent.com/53321666/82900892-269ead00-9f98-11ea-9648-e33f2541dc61.png)

고객과의 진행 상황을 등록할 수 있게 '내용', '진행상황' 등록란을 추가하였습니다.

 ---------------------------

![inquiry 06](https://user-images.githubusercontent.com/53321666/82900894-27374380-9f98-11ea-9398-0820a80250f0.png)

 Share Point보다는 늘 접속해 있는 Teams에서 업무를 처리하기 위해 상단 탭에  '+' 을 클릭합니다.

![inquiry 07](https://user-images.githubusercontent.com/53321666/82900898-27374380-9f98-11ea-8641-974ccda77952.png)

 Share Point를 선택합니다.

![inquiry 08](https://user-images.githubusercontent.com/53321666/82900901-27cfda00-9f98-11ea-9633-d0996c46418a.png)

 'Lists'를 선택하면 Share Point에 만들어 놓은 리스트들이 나오고 사용할 리스트를 선택하면

![inquiry 09](https://user-images.githubusercontent.com/53321666/82900902-27cfda00-9f98-11ea-8c35-2cd2a390022f.png)

 이렇게 Teams 내에 Share Point List가 자동으로 연동되게 됩니다.

 -----------------

## Power Automate

이제 고객이 MS Forms에 문의 내용을 입력 후 '제출'을 하면 Share Point List에 자동으로 입력될 수 있게 Power Automate를 사용하여 자동화 흐름을 만듭니다.

	Power Automate : 프로세스 자동화 설계 https://flow.microsoft.com/

![inquiry 10](https://user-images.githubusercontent.com/53321666/82753185-bdcffd00-9dfe-11ea-97bc-1243844ee1e5.png)


왼쪽 My flows를 선택 '+New' -> 'Automated'를 선택합니다.

---------------

![inquiry 11](https://user-images.githubusercontent.com/53321666/82900905-28687080-9f98-11ea-99fd-f0416f1d22cb.png)

자동으로 실행 할 'Trigger'로 MS Forms를 사용할 것 이므로 첫번째 Forms를 선택합니다.

-------------------------

![inquiry 12](https://user-images.githubusercontent.com/53321666/82900906-29010700-9f98-11ea-86c0-8481480f09f0.png)

어떤 내용의 Forms를 사용할 것 인지 정하기 위해 Forms id를 입력합니다.

본인이 만든 Forms경우 제목이 나타납니다.
그러나 다른 Forms를 가져와야 할 경우 

https://forms.office.com/Pages/DesignPage.aspx?origin=OfficeDotCom&lang=en-US#FormId=RUbEfkw2ZEOC8KVVY743vUdyqq-mxexDgseZYSIL7iVUMVZCWElPQzE0SVdVUUk2WjRKRk&Preview=%7B%22PreviousTopView%22%3A%22None%22%7D&TopView=Preview

Forms URL 전체 주소에서

FormId=RUbEfkw2ZEOC8KVVY743vUdyqq-mxexDgseZYSIL7iVUMVZCWElPQzE0SVdVUUk2WjRKRk

이 부분을 입력해주면 됩니다.   
(이 주소는 편집된 주소입니다. 본인의 URL 주소를 사용하세요.)

---------
![inquiry 13](https://user-images.githubusercontent.com/53321666/82900908-29010700-9f98-11ea-8a52-92c1b18e3fdd.png)

입력 된 Forms 내용을 갖고 오게하는 
'Get response details'를 선택하고 내용을 입력합니다.

------------
![inquiry 14](https://user-images.githubusercontent.com/53321666/82900910-29999d80-9f98-11ea-9c42-3b378cd82fb4.png)

Forms에서 가져온 내용을 입력 할 List를 만들기 위해 SharePoint 의 'Create Item'을 선택하고      'Site Adress'에 해당되는 SharePoint 위치
'List Name' 및 입력해야 될 각 내용을 설정합니다.

---------------

![inquiry 15](https://user-images.githubusercontent.com/53321666/82900912-29999d80-9f98-11ea-887e-0d3ffa1511f1.png)

Share Point List에 내용이 입력되면 Teams의 게시물에 자동으로 내용이 입력되게 
'Post a message'를 설정합니다.

----
![inquiry 16](https://user-images.githubusercontent.com/53321666/82900915-2a323400-9f98-11ea-9ba4-50b4811918ee.png)

담당자가 문의가 온 것을 바로 알 수 있게 이메일 발송을 설정합니다.

---

![inquiry 17](https://user-images.githubusercontent.com/53321666/82900917-2a323400-9f98-11ea-9b4c-63222e0781b4.png)

전체 자동화 흐름의 모습입니다.

---

### 내용 변경 시 알림 설정

문의 내용에 변동 사항이 생길 시 알림을 보내는 자동화 흐름을 만듭니다.

![inquiry 10](https://user-images.githubusercontent.com/53321666/82753185-bdcffd00-9dfe-11ea-97bc-1243844ee1e5.png)

위와 동일하게 새로운 자동화 흐름 만들기를 선택합니다.

![inquiry 19](https://user-images.githubusercontent.com/53321666/82900920-2acaca80-9f98-11ea-97c3-1b5006d6f133.png)

이번에는 자동화 실행 조건을 'Share Point의 'When an item is created or modified'로 설정합니다.

![inquiry 18](https://user-images.githubusercontent.com/53321666/82900919-2acaca80-9f98-11ea-9589-4fb18066c54e.png)

'When an item is created or modified'에서 알림을 받을 Share Point List를 설정합니다.

이메일로 담당자에게 알림을 발송합니다.


---

고객이 문의를 제출하게 되면 쉐어포인트에 내용이 등록되고   
담당자에게 바로 이메일이 발송되어 확인 후 팀즈에서 확인 및 진행상황 정리까지 자동으로 이루어지게 됩니다.