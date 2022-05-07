---
title: Power Automate에서 아웃룩 메일 발송 시 파일첨부
categories:
  - 'Power Automate'
  - ''
tags:
  - 'Power Automate'
  - 'Outlook'
date: 2020-07-14 14:54:01
---

## Power Automate에서 아웃룩에 파일을 첨부하는 방법입니다.
이메일 발송 대한 부분은 [Power Automate 대량 이메일 개별 발송](https://ohroro.github.io/2020/07/07/html-%EC%9D%B4%EB%A9%94%EC%9D%BC-%EB%8B%A8%EC%B2%B4%EB%B0%9C%EC%86%A1/) 이곳을 먼저 확인바랍니다.

![at 01](https://user-images.githubusercontent.com/53321666/87389389-9f59d700-c5e1-11ea-9104-067857753493.png)

현재 Automate 상태입니다.

---

파일을 불러오기 위해 아웃룩 설정 전에 작업 추가를 해줍니다.

![at 02](https://user-images.githubusercontent.com/53321666/87390139-2fe4e700-c5e3-11ea-9ceb-8f11ca48f77f.png)

---

Sharepoint에 파일이 저장되어 있으므로 Sharepoint를 선택합니다.

![at 03](https://user-images.githubusercontent.com/53321666/87390140-31161400-c5e3-11ea-9c64-02a0958381dc.png)

---

검색창에 '경로'까지만 적어주면 나오는 '경로를 사용하여 파일 콘텐츠 가져오기'를 클릭합니다.

![at 07](https://user-images.githubusercontent.com/53321666/87390098-15ab0900-c5e3-11ea-842b-ea6ae7423397.png)

---

사이트 주소 -> 첨부파일이 있는 Sharepoint 사이트를 설정합니다
파일 경로 -> 설정한 Sharepoint 사이트 내에 파일이 위치한 곳을 설정합니다.   
엑셀 표를 가져오기 했던 방법과 동일합니다.

![at 08](https://user-images.githubusercontent.com/53321666/87390414-c5807680-c5e3-11ea-9466-f9dfb74824d4.png)

---

아웃룩 메일 보내기 설정에서 '고급 옵션 표시' 선택 후   
첨부 파일 콘텐츠 위치를 클릭하면 '동적 콘텐츠'창이 나타납니다.
파일 콘텐츠 가져오기에서 '파일 콘텐츠'를 선택합니다.

'경로를 사용하여 파일 콘텐츠 가져오기'에서 설정한 파일을 가져오는 것입니다.

![at 05](https://user-images.githubusercontent.com/53321666/87390143-31aeaa80-c5e3-11ea-9217-60002ee9f269.png)

---

'첨부 파일 이름'란에 파일명을 입력합니다.   
__중요한 부분은 파일 확장자명을 꼭 입력해 주어야 합니다.__   
*(워드일 경우=빈 문서.docx / 엑셀일 경우=빈 문서.xlsx  등)*

![at 06](https://user-images.githubusercontent.com/53321666/87390144-31aeaa80-c5e3-11ea-903a-7141a19256e5.png)

---

이제 Automate 저장 후 발송하면 됩니다.