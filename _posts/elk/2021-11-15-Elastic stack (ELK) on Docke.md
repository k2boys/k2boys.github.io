---
title: 'Elastic stack (ELK) on Docker'
slug: Elastic stack (ELK) on Docker
excerpt: Docker 및 Docker Compose를 사용하여 Elastic 스택의 최신 버전을 실행합니다.
date: '2021-12-13'
last_modified_at: '2021-11-15T11:52:46.438Z'
draft: true
tags: null
categories: ElasticSearch
---

## 도커로 최신버전 엘라스틱 스택 실행하기

[Elastic stack (ELK) on Docker](https://github.com/deviantony/docker-elk) 저장소에서 다운로드

해당 강좌에서 사용한 것들에 대해 간략하게 리뷰해보려 한다.

### 1. 다운로드 및 압축 풀기

저장소에서 clone 또는 zip파일을 다운받아 압축을 푼다

#### 1 - 1. docker-compose 실행

```bash
$ docker-compose up
```


### 2. 설정

#### 2 - 1. Elastic Search 설정 (elasticsearch/config/elasticsearch.yml)

```yml
elasticsearch:

  environment:
    network.host: _non_loopback_
    cluster.name: my-cluster
```

#### 2 - 1. Kibana 설정 (kibana/config/kibana.yml)

```yml
elasticsearch:

  environment:
    network.host: _non_loopback_
    cluster.name: my-cluster
```

