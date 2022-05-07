---
title: 'Sharepoint List ID, Power Automate로  임의 생성하기'
categories:
  - 'SharePoint'
  - 'Power Automate'
tags:
  - 'SharePoint List ID'
  - 'Power Automate'
date: 2020-06-02 22:32:50
---


## SharePoint List 생성

![Sahrepoint ID 01](https://user-images.githubusercontent.com/53321666/83518827-ebf7c000-a515-11ea-9ec3-83e9d182f4f5.png)

쉐어포인트에 리스트를 생성하고 내용 입력할 때 마다 쉐어포인트 자체적으로 'ID'를 생성합니다.

그러나 자동 생성 ID값은 숫자로만 이루어져 있어서 문자가 포함 된 ID를 만들어 보겠습니다.

---
![Sahrepoint ID 02](https://user-images.githubusercontent.com/53321666/83518154-12692b80-a515-11ea-8fee-bb916d867b6e.png)

간단하게 리스트 필드를 'Title', 'User ID', 'User Name'으로만 설정하였습니다.   
자동화 흐름을 만들기 위해 Power Automate -> 흐름 만들기를 선택합니다.

---
![Sahrepoint ID 03](https://user-images.githubusercontent.com/53321666/83518156-1301c200-a515-11ea-8ae5-0a948b5b3ace.png)

흐름 만들기를 선택하면 오른쪽에 Power Automate 템플릿이 나옵니다.   
원하는 내용이 없으므로 하단 '흐름 보기'를 선택하여 Power Automate 사이트로 갑니다.  

---
![Sahrepoint ID 04](https://user-images.githubusercontent.com/53321666/83518157-1301c200-a515-11ea-98a0-e4a5ab948176.png)

My flows 에서 

![Sahrepoint ID 05](https://user-images.githubusercontent.com/53321666/83518160-139a5880-a515-11ea-9bf3-eb5144aaef73.png)

상단 ''New' -> 'Autopmate-from blank'를 선택합니다.

---

![Sahrepoint ID 06](https://user-images.githubusercontent.com/53321666/83518162-1432ef00-a515-11ea-82b2-7010e00cd3b0.png)

'Flow name'에 이름을 넣어주고 flow가 자동으로 실행되는 'trigger'로 'SharePoint에 새로운 아이템이 생성 될 때'를 선택합니다.

---

![Sahrepoint ID 07](https://user-images.githubusercontent.com/53321666/83518164-1432ef00-a515-11ea-8e01-8657cb00bf8e.png)

쉐어포인트 사이트 설정   
리스트 이름을 설정합니다.

---
![Sahrepoint ID 08](https://user-images.githubusercontent.com/53321666/83518173-172ddf80-a515-11ea-8396-cf8424664e82.png)

다음 단계로 업데이트 아이템을 설정합니다.

---

![Sahrepoint ID 09](https://user-images.githubusercontent.com/53321666/83521191-d7b5c200-a519-11ea-9090-50527906d272.png)

사이트 주소와 리스트 이름을 트리거와 동일하게 설정해줍니다.   
'id' 쉐어포인트의 기본 값으로 주어지는 id입니다. 1 부터 순차적으로 증가합니다.   
Dynamic content 의 id를 넣어줍니다.

---

![Sahrepoint ID 10](https://user-images.githubusercontent.com/53321666/83521192-d8e6ef00-a519-11ea-86b5-18398e13ea0a.png)

쉐어포인트 입력 시 사용한 'Title' 값을 그대로 넣을 것이므로 Dynamic content 의 'Title'을 넣어줍니다.

---
![Sahrepoint ID 20](https://user-images.githubusercontent.com/53321666/83523518-49433f80-a51d-11ea-8819-6ed42a639ddd.png)

자동화를 사용하여 원하는데로 생성 할 'User ID'란 입니다.   
Id에 'User Name'을 포함한 'ID'를 생성할 것 입니다.   
'Dynamic content'의 'User Name' 선택 후 'Expression'에서 위와 같이 함수를 입력합니다.   
'1000'으로 설정 시 쉐어포인트에서 기본으로 생성하는 id값에 1000을 더한다고 생각하시면 됩니다.   
기본 id값이 2 이면 1002 가 됩니다.

---
![Sahrepoint ID 15](https://user-images.githubusercontent.com/53321666/83524125-1cdbf300-a51e-11ea-8bb5-81edcd6e0a0e.png)

Automate를 시작해 봅니다.   
우측 상단의 'Test'를 클릭합니다.

---

![Sahrepoint ID 16](https://user-images.githubusercontent.com/53321666/83524128-1d748980-a51e-11ea-896d-40efa21ea8b5.png)

직접 트리거를 작동합니다.

---

![Sahrepoint ID 17](https://user-images.githubusercontent.com/53321666/83524131-1d748980-a51e-11ea-9b53-148faa008f2c.png)

Automate가 작동하기 위해 대기중입니다.

---

![Sahrepoint ID 13](https://user-images.githubusercontent.com/53321666/83524405-86f49800-a51e-11ea-8a70-12071cbdb6fc.png)

SharePoint로 돌아가서 아이템 생성을 위해'New'를 선택합니다.   

---

![Sahrepoint ID 14](https://user-images.githubusercontent.com/53321666/83524410-878d2e80-a51e-11ea-9720-a304c81c503d.png)

우측에 입력창이 나타납니다.
내용을 입력하고 'Save'를 합니다.

---

![Sahrepoint ID 19](https://user-images.githubusercontent.com/53321666/83524831-1e59eb00-a51f-11ea-9d50-99b37584dc2b.png)

Power Automate로 돌아가면 flow 성공 메세지가 나타납니다.

![Sahrepoint ID 22](https://user-images.githubusercontent.com/53321666/83525714-53b30880-a520-11ea-8903-a0c7be82f555.png)

쉐어포인트로 다시 가보면 'User ID'란에 이렇게 등록이 됩니다.