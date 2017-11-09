---
layout: post
title: "apache zeppelin의 dynamic form 정리"
description: "활용법은 무궁무진"
tags: [apache-zeppelin, data visualization, Database]
image:
  feature: "zeppelin-notebook.png"
---

> 참조. [http://zeppelin.apache.org/docs/0.6.2/manual/dynamicform.html](http://zeppelin.apache.org/docs/0.6.2/manual/dynamicform.html)

- dynamic form을 이용하면 충분히 쓸만한 custom dashboard를 만들 수 있다.

# 1. Text input form

<center><img src="../images/zeppelin-dynamic-form/1.png" width="600"></center>

&nbsp;

- 기본 형태: `${formName}`
- default value 지정 형태: `${formName=defaultValue}`
  - 기본값을 지정하는 경우 첫 실행시 default value로 input이 들어가서 실행된다.

# 2. Select form

<center><img src="../images/zeppelin-dynamic-form/2.png" width="600"></center>

&nbsp;

- 기본 형태: `${formName=,option1|option2...}`
- default value 지정 형태: `${formName=defaultValue,option1|option2...}`
- 선택값과 출력값을 다르게 지정한 형태: `${formName=defaultValue,option1(DisplayName)|option2(DisplayName)...}`

# 3. Checkbox form

- 쿼리 사용할 때 유용하다.
- in 뒤의 () 안에 string 값들이 들어갈 땐 `'`기호가 필요한데 이럴땐 delimiter를 `','` 형태로 주고 전체 dynamic form을 `'`로 감싸주면 된다.

<center><img src="../images/zeppelin-dynamic-form/3.png" width="600"></center>
&nbsp;
<center><img src="../images/zeppelin-dynamic-form/4.png" width="600"></center>
&nbsp;

<center><img src="../images/zeppelin-dynamic-form/5.png" width="600"></center>

&nbsp;

- 기본 형태: `${checkbox:formName=,option1|option2...}`
- default value 지정 형태: `${checkbox:formName=defaultValue1|defaultValue2...,option1|option2...}`
- delimiter 지정 형태: `${checkbox(delimiter):formName=,option1|option2...}`
