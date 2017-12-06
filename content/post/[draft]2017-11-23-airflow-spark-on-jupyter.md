---
title: "[airflow] 3. Jupyter에서 Pyspark 사용하기"
metaAlignment: center
date: 2017-11-23 09:52:00+09:00
categories:
- dev
tags:
- data engineering
- data
- airflow
- open source
thumbnailImage: //airflow.apache.org/_images/pin_large.png
thumbnailImagePosition: left
draft: true
---

<!--more-->

- `airflow scheduler`를 실행하는걸 잊지 말자.


```sh
# SPARK shell 실행을 위해 기본적으로 설정해야 하는 부분
export SCALA_HOME=/usr/local/bin/scala
export PATH=$PATH:$SCLAL_HOME/bin
export SPARK_HOME=/usr/local/Cellar/apache-spark/2.2.0/libexecexport PATH=$PATH:$SPARK_HOME
export SPARK_LOCAL_IP=127.0.0.1  # 로컬에서 실행할 경우 설정해줘야함
#export PYTHONPATH=$SPARK_HOME/python:$SPARK_HOME/python/build:$PYTHONPATH
#export PYTHONPATH=$SPARK_HOME/python/lib/py4j-0.10.4-src.zip:$PYTHONPATH


# 아래 부분을 설정할 경우, pyspark 명령어 입력시 기본적으로 jupyter환경에서 실행된다.
# export PYSPARK_DRIVER_PYTHON=jupyter
# export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
```


아래 샘플코드를 실행해서 잘 되는걸 확인해보자.

```py
import pyspark
import random

sc = pyspark.SparkContext(appName="Pi")
num_samples = 100000000

def inside(p):     
  x, y = random.random(), random.random()
  return x*x + y*y < 1

count = sc.parallelize(range(0, num_samples)).filter(inside).count()
pi = 4 * count / num_samples
print(pi)
sc.stop()
```

![](https://i.imgur.com/9ONhgCf.png)



# spark 경로를 찾지 못할 경우.

- findspark의 도움을 받자.
- findspark를 설치한다.(`pip install findspark`)
- 아래 코드를 추가한다.

```py
import os
import findspark
findspark.find()
findspark.init(os.environ.get("SPARK_HOME"))
```