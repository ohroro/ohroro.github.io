---
title: Edu 페이지 만들기
categories:
  - 'wordpress'
  - ''
tags:
  - 'wordpress'
  - 'avada'
  - 'pages'
  - 'posts'
  - '워드프레스'
date: 2020-04-02 10:46:38
---
## 홈페이지에 교육용 페이지 만들기

Wordpress에 Avada 테마를 사용중이다.

![wordpress 01](https://user-images.githubusercontent.com/53321666/78202802-3a65ef80-74d0-11ea-8553-416f87ec871f.png)

### Toggle

toggle을 사용하여 한 페이지안에 자료를 모아보았다. 

가장 깔끔할것이라 생각하여 만들었다.

![wordpress 02](https://user-images.githubusercontent.com/53321666/78203584-566a9080-74d2-11ea-8102-32a0687cfac3.png)

토글 선택시 해당 내용만 펼쳐지는 형태이다.
깔끔한 모습은 좋으나 검색 시에 모든 내용이 이 페이지 안에 있다보니......

이 페이지안에서 다시 수동으로 찾아야하는 불편함이 발생...

### Posts 작성으로 변경

위젯과 메뉴를 섞어서 토글안에 넣으려 하였다. 제목만 나오게 하고 싶은데 그 간격이 원하는 것보다 넓어서 간단하게 표시되는 플러그인을 검색하던 중 'List Category Posts'라는 플러그인 발견. 

![wordpress 04](https://user-images.githubusercontent.com/53321666/78204035-7fd7ec00-74d3-11ea-9fc3-335281c71fbc.png)

이 플러그인을 위젯에 추가한 후 토글안에 이 위젯을 추가

![wordpress 03](https://user-images.githubusercontent.com/53321666/78204041-81a1af80-74d3-11ea-9b95-71986ee5c1c0.png)

오호! 원하는 모습이다!!!

원하는 포스트 제목을 선택하면 내용을 볼수 있게 되고 검색 시에도 개별적으로 포스트가 있어서 해당 검색이 된다.

### 위의 두가지를 함께 사용할 수는 없을까??

![wordpress 02](https://user-images.githubusercontent.com/53321666/78203584-566a9080-74d2-11ea-8102-32a0687cfac3.png)

각 토글에 포스트를 하나씩 넣을 수 있다면 이 페이지 안에서 모두 해결되겠는데! 다시 수정..

![wordpress 05](https://user-images.githubusercontent.com/53321666/78205111-51a7db80-74d6-11ea-91ff-c682452f59c2.png)

'Post in Page' 

간단한 코드로 페이지안에 포스트를 넣을 수 있다하여 사용

![wordpress 07](https://user-images.githubusercontent.com/53321666/78205344-db57a900-74d6-11ea-9747-0f82fdcfd5cd.png)

이미지가 안 나오고 내용도 전체가 나오지를 않는다.... 아바다 설정에서 포스트 내용이 전체가 나오게 설정을 변경하여도 계속 이 상태... 이러면 안되는데... 다시 검색

![wordpress 06](https://user-images.githubusercontent.com/53321666/78205116-52407200-74d6-11ea-9f09-c460164d4ae2.png)

'Insert Pages' 플러그인으로 변경

![wordpress 08](https://user-images.githubusercontent.com/53321666/78205562-6638a380-74d7-11ea-92fd-91723b1602ef.png)

엇! 이건 되네!!! 그런데.....

![wordpress 09](https://user-images.githubusercontent.com/53321666/78205566-69339400-74d7-11ea-9389-d7d7e2fe9c1f.png)

한글 내용은 이렇게 나온다.... 아... 다시 고민...