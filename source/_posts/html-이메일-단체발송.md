---
title: 이메일 개별 대량발송
categories:
  - 'Power Automate'
tags:
  - 'Power Automate'
  - 'Outlook'
  - 'html'

---

## Power Automate 대량의 이메일 개별 발송 

### 아웃룩을 사용하여 이름을 넣어서 ('홍길동님 안녕하세요!') 메일 발송하는 자동화를 만들어 봅니다.

우선 메일을 발송할 사람의 이름, 이메일 정보를 엑셀에 입력합니다.
![Seding Email 01](https://user-images.githubusercontent.com/53321666/87300814-869de280-c549-11ea-8070-e281432bc60e.png)

---

입력한 내용을 '표 서식'으로 만듭니다.
![Seding Email 02](https://user-images.githubusercontent.com/53321666/87300816-87cf0f80-c549-11ea-8dd2-e365b16eadaa.png)

---

꼭 '머리글 포함'을 체크 해줍니다.
![Seding Email 03](https://user-images.githubusercontent.com/53321666/87300818-8867a600-c549-11ea-8fd4-865e5d232645.png)

---

'표'가 만들어 졌습니다.

![Seding Email 04](https://user-images.githubusercontent.com/53321666/87300819-8867a600-c549-11ea-8046-c18c48ffb39b.png)

---

Power Automate 사이트에 접속합니다.   
왼쪽 메뉴에서 '만들기' -> '인스턴트 흐름'을 선택합니다.

![Seding Email 05](https://user-images.githubusercontent.com/53321666/87300822-89003c80-c549-11ea-8e03-63e386e08982.png)

---

'흐름 이름'을 설정하고 '수동으로 Flow 트리거' 선택 후 '만들기'를 클릭합니다.   
내가 직접 자동화 흐름을 실행하겠다는 것입니다.

![Seding Email 06](https://user-images.githubusercontent.com/53321666/87300823-89003c80-c549-11ea-853a-3aeaa3b47a66.png)

---

만들기를 하면 수동으로 Flow 트리거'가 기본으로 만들어져 있습니다.  
+새 단계를 클릭 

![Seding Email 07](https://user-images.githubusercontent.com/53321666/87300824-8998d300-c549-11ea-8a57-e29db3072e4d.png)

---

발송 할 이름과 이메일 주소를 만들어 둔 엑셀 파일을 불러와야 합니다.   
'Excel Online' 을 선택합니다.

![Seding Email 08](https://user-images.githubusercontent.com/53321666/87300825-8998d300-c549-11ea-9720-fc168dc3a505.png)

---

동작 메뉴들 중 '테이블에 있는 행 나열'을 선택합니다.

![Seding Email 09](https://user-images.githubusercontent.com/53321666/87300826-8a316980-c549-11ea-9a67-3f7502c8b530.png)

---

엑셀파일이 있는 위치를 지정합니다.   
내가 만든 테이블이 여러개 일 경우 원하는 이름을 선택하면 됩니다.

![Seding Email 10](https://user-images.githubusercontent.com/53321666/87300827-8aca0000-c549-11ea-82f9-e63067d2d4e0.png)

---

다시 '+새 단계'를 클릭 후   
이메일을 발송하기 위해 Outlook을 선택합니다.

![Seding Email 11](https://user-images.githubusercontent.com/53321666/87300828-8aca0000-c549-11ea-85c3-79583c531cc9.png)

---

'메일 보내기'를 선택합니다.

![Seding Email 12](https://user-images.githubusercontent.com/53321666/87300830-8b629680-c549-11ea-9a7c-d9be72ef7e85.png)

---

받는 사람 입력란 바로 아래 '동적 콘텐츠 추가'를 클릭합니다.

![Seding Email 13](https://user-images.githubusercontent.com/53321666/87300833-8b629680-c549-11ea-8794-ebb70901b564.png)

---

엑셀 파일에 있는 이메일 주소를 가져오기 위해 '테이블에 있는 행 나열'에서 Email을 클릭합니다.

![Seding Email 14](https://user-images.githubusercontent.com/53321666/87300835-8bfb2d00-c549-11ea-8bb0-9522caf76bb6.png)

---

다수의 인원에게 각각 발송하게 되므로 자동으로 '각각에 적용'이 자동으로 설정됩니다.

![Seding Email 15](https://user-images.githubusercontent.com/53321666/87300837-8bfb2d00-c549-11ea-9e25-1a0c814d4fe7.png)

---

메일 제목을 설정하고   
본문에 받는 사람의 이름을 넣기 위해 '동적 콘텐츠 추가'를 클릭합니다.   
테이블에 있는 행 나열에서 'Name'을 클릭합니다.

![Seding Email 16](https://user-images.githubusercontent.com/53321666/87300838-8c93c380-c549-11ea-8ca4-089308d191b8.png)

발송할 메일 내용 입니다.

![Seding Email 17](https://user-images.githubusercontent.com/53321666/87300839-8d2c5a00-c549-11ea-9db1-9416c4d75abf.png)

오른쪽에 보이는 '</>' 메뉴를 클릭하면

---

html로 입력을 할 수 있습니다.

![Seding Email 28](https://user-images.githubusercontent.com/53321666/87300859-91587780-c549-11ea-9799-388dbf7a33c7.png)

---

고급 옵션 표시를 클릭합니다.

![Seding Email 18](https://user-images.githubusercontent.com/53321666/87300841-8d2c5a00-c549-11ea-8e05-06d91a5aedad.png)

---

보낸 사람을 설정할 수 있고   
참조자 설정도 할 수 있습니다.

![Seding Email 18_1](https://user-images.githubusercontent.com/53321666/87300842-8dc4f080-c549-11ea-877f-c0c0f9494c7b.png)

---

Automate를 실행합니다.

![Seding Email 20](https://user-images.githubusercontent.com/53321666/87300844-8e5d8700-c549-11ea-9669-ff665a2b9ef5.png)

---


![Seding Email 21](https://user-images.githubusercontent.com/53321666/87300846-8e5d8700-c549-11ea-8dd5-9740bbb348d2.png)

![Seding Email 22](https://user-images.githubusercontent.com/53321666/87300848-8ef61d80-c549-11ea-98ea-f44a0ebd15b1.png)

![Seding Email 23](https://user-images.githubusercontent.com/53321666/87300850-8ef61d80-c549-11ea-9b20-b4a5f00bee15.png)

Automate 실행이 성공하였다는 메세지가 나왔습니다.

![Seding Email 24](https://user-images.githubusercontent.com/53321666/87300854-8f8eb400-c549-11ea-8768-eb897189ba81.png)

---

엑셀에 만들어 둔 각각의 사람에게 이메일을 발송을 하였습니다.
![Seding Email 25](https://user-images.githubusercontent.com/53321666/87300856-90274a80-c549-11ea-99f0-a75ae26b607a.png)
![Seding Email 26](https://user-images.githubusercontent.com/53321666/87300857-90bfe100-c549-11ea-8964-537c8cb70ae9.png)
![Seding Email 27](https://user-images.githubusercontent.com/53321666/87300858-90bfe100-c549-11ea-8fe4-d215e853b357.png)

