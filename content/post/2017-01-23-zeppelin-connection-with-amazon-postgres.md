---
layout: post
title: "apache zeppelin에 postgres DB 연결하기"
description: "다른 DB도 가능합니다"
tags: [apache-zeppelin, postgres, aws, Database]
image:
  feature: "zeppelin-notebook.png"
---

<center><img src="../images/connecting-postgres-with-zeppelin/1.png" width="600"></center>

- 제플린 빌드 후 오른쪽 상단에서 Interpreter 클릭

<center><img src="../images/connecting-postgres-with-zeppelin/2.jpg" width="600"></center>

- `jdbc`에서 DB 정보 입력

- `common.max_count`: 한번에 몇개의 row를 조회할 것인지 설정
- `default.driver`: org.postgresql.Driver
- `default.password`: DB 패스워드
- `default.url`: DB 주소. jdbc:postgresql://DNS_ADDRESS:PORT/DBNAME 형태로 입력.
- `default.user`: DB user name 입력

<center><img src="../images/connecting-postgres-with-zeppelin/3.png" width="600"></center>

- notebook에서 첫줄에 `%jdbc`입력 후 테스트 쿼리를 날려보면 잘 되는걸 확인 할 수 있다.
