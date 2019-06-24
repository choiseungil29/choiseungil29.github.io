---
layout: single
author_profile: true
---
최 승일  
생년월일 : 1996. 11. 03  
연락처 : 010-9034-5202  
이메일 : choiseungil29@gmail.com

## 개발 환경

* 언어: Python, Javascript, C/C++, Java
* 웹 프레임워크 : Flask, Node, Koa
* 웹 프론트 : Vue, Jinja
* 웹 서버 : Nginx
* 데이터베이스 : MySQL, PostgreSQL, Redis, Memcached, SQLite, SQLAlchemy
* 개발 도구 : Vim, Git, tmux, zsh, ...
* 그 외 : AWS(EC2, RDS, Lambda, S3, ...), Puppeteer, BeautifulSoup4, ...

## 썸머 (2018.07 - 2019.04)
<details><summary>주문완료 페이지 트래픽 재활용 프로젝트 Loopsum의 API 서버 및 백오피스 개발 (2018.11)</summary>
<div markdown="1">
> 개발 인원 : 2인  
> 클라이언트 환경 : vue  
> 백엔드 환경 : flask, postgresql  
> 관련 기사 : [썸머코퍼레이션, 백엔드 쇼핑 플랫폼 ‘루프썸(loopsum)’ 베타 론칭 블랭크 5,000만 페이지뷰, e커머스와 나눈다](http://blankcorp.kr/bbs/board.php?bo_table=41&wr_id=124)

기존 쇼핑몰들의 주문 완료 페이지에는 별도의 광고를 삽입하지 않고 있었습니다. 하지만 여기에 자사제품을 다시한번 노출시켜 재구매로 이어지게 해보자는 아이디어에서 출발해 프라이빗 몰까지 제공했던 서비스입니다.  

회원사 A의 주문 완료 페이지에 loopsum 자체 몰에 대한 광고를 노출시키고, loopsum에서는 A사의 제품 + 그 외의 제품을 최저가로 판매하도록 하는 정책으로 이미 1번 구매 이력이 있는 소비자가 다시 제품에 노출되는 방식의 광고 플랫폼 + 프라이빗 몰 서비스입니다.  

회원사 내에서 테스트했을 때 유저의 몰 진입 대비 주문 전환율이 10%정도로 나타나기도 했습니다.  

해당 서비스의 기획 및 서버와 백오피스 클라이언트를 개발하였습니다. 프라이빗 몰 클라이언트는 Cafe24 서비스를 활용했습니다.  
</div>
</details>

<details><summary>AWS 비용 최적화 (2018.10)</summary>
<div markdown="1">

 사내 AWS계정의 월간 비용이 400만원을 넘는 시점이 있었습니다. EC2와 RDS이 과하게 사용되어지는 부분을 조사하여 스펙을 조정함으로써 비용을 절감했습니다. S3에서도 CloudFront를 붙여 월간 비용을 200만원가량 절감했습니다.
</div>
</details>

<details><summary>쇼핑몰 플러그인 프로젝트 1mm 클라이언트/백엔드 개발</summary>
<div markdown="1">
> 개발 인원 : 3인  
> 클라이언트 환경 : vue, nuxt  
> 백엔드 환경 : koa, mysql  

 개인 쇼핑몰 운영자들이 필요로 하는 플러그인들을 개발하고 무료로 배포하여 초기 트래픽을 확보하겠다는 목표를 가진 프로젝트입니다. 트래픽에 포커스가 맞춰져 있었고 그만큼 다양한 니즈를 맞추기 위해 작고 다양한 플러그인을 빠른 속도로 개발해야하는 프로젝트였습니다.  

 그러나 프로젝트의 구성이 플러그인 클라이언트, 플러그인 어드민 & 플러그인 렌더링 서버(nuxt client), 플러그인 api서버(koa)와 cafe24데이터를 가져오기 위해서 cafe24 api server까지 사용하며 개발해야했습니다.  

작은 플러그인을 개발하는데 있어 스케일 대비 큰 컨텍스트에 대한 이해가 필요했기 때문에 해당 구조를 풀어내는 과정을 제안하고 진행하였습니다.
 
1. nuxt client를 vue로 대체하고, api서버만 남겨두어 nuxt서버와 api서버 사이에서 어느곳에 작성해야할지에 대한 고민비용을 줄였습니다.
2. cafe24 api만들 처리하고 돌려주는 공용 cafe24 api서버를 만들었습니다. 플러그인을 만들때마다 중복적으로 작성해야 하는 코드들을 작성할 필요가 없게 되었습니다.
</div>	
</details>

## 블루홀 (2017.11 - 2018.02)
<details><summary>Android/iOS 방치형 게임 '포켓 크루' API 개발 및 서버 환경 구축</summary>
<div markdown="1">
> 개발 인원 : 클라이언트 개발자 3명, 서버 개발자 1명  
> 클라이언트 환경 : Unity, C# Protobuf  
> 백엔드 환경 : Python, Flask, PostgreSQL, SQLAlchemy + Alembic, nginx, uwsgi, Celery, Protobuf, Jenkins, Docker, ELK, Amazon Web Service : [[EC2](https://aws.amazon.com/ec2), [ES](https://aws.amazon.com/elasticsearch-service), [ElastiCache Redis](https://aws.amazon.com/elasticache), [S3](https://aws.amazon.com/s3), [Lambda](https://aws.amazon.com/lambda), [RDS](https://aws.amazon.com/rds), [ECS](https://aws.amazon.com/ecs)]

 방치형 게임 ‘포켓 크루’의 서버 API를 개발하였습니다.

1. protobuf로 패킷 데이터를 소스코드로 모델링함으로써 기존 api docs에 대한 니즈를 자연스럽게 해결할 수 있도록 하였습니다.
2. 기존 환경은 기획자가 개발중인 기능을 확인하고 피드백하기 어려운 환경이었습니다. 그래서 jenkins와 codedeploy를 도입하여 CI/CD 환경을 구축했고 결과적으로 배포와 테스트, 피드백이 용이해지게 되었습니다.
3. 게임 내 정보를 excel to csv로 변환하여 사용하던것을 excel to json으로 변환하도록 수정하여 타입 관련 에러를 조기에 발견할 수 있도록 하였습니다.
4. 클라이언트에서 재화 발생 event나 등등의 event가 발생하면 클라이언트에서는 선 반영을 하고, event list를 서버 요청마다 request header에 실어 보내는 방법을 제안하고 적용하였습니다. 이것으로 기존 방치형 게임들의 문제였던 재화 버그 & 스피드핵과 같은 문제를 해결할 수 있게 되었습니다.	
</div>
</details>
	
## 이노스파크 (2016.11 - 2017.11)
<details><summary>Android/iOS 방치형 게임 '환생기사단' API 개발</summary>
<div markdown="1">
> 개발 인원 : 클라이언트 개발자 3명, 서버 개발자 2명  
> 클라이언트 환경 : Unity, C#  
> 백엔드 환경 : Python, Flask, PostgreSQL, SQLAlchemy, nginx, uwsgi, Amazon Web Service : [[EC2](https://aws.amazon.com/ec2), [S3](https://aws.amazon.com/s3/)]

 마켓에서 라이브중이었던 게임 ‘환생기사단’의 서버 개발자로서 API를 작성하였습니다.

 기존 서버개발자가 퇴사한 이후 오랜 기간동안 클라이언트 개발자분이 직접(copy & paste -> server restart) 서버 배포 & API 개발을 하면서 코드 버전, 서버 환경 및 배포 환경이 관리되지 않던 문제들이 있었습니다.  

 게임이 빠르게 제작되어 런칭된 이후라 버그 + 업데이트가 잦았고 따라서 배포 오버헤드가 큰 상황이었습니다.  

1. api마다 테스트하고 docstring을 남겨두었습니다. 그리고 이를 뽑아주는 코드를 작성하고 클라이언트 개발자분들과 공유하여 가벼운 api 문서 역할을 할 수 있도록 하였습니다.
2. 클라이언트 개발자마자 local server를 띄워주는 shell script를 작성하여 공유하였습니다. 기존 develop서버에 문제가 있으면 클라이언트 개발자 전원의 작업이 홀드되는 문제를 없앴고 이로써 클라이언트 개발자들의 모든 이슈의 테스트 기간이 줄어들게 되었습니다.
</div>
</details>

## 포트폴리오 (개인)
<details><summary>웹 유머 게시물 뷰어 서비스 쓰끄롤 (2019.04-)</summary>
<div markdown="1">
> 개발 인원 : 1인  
> 클라이언트 환경 : vuejs  
> 백엔드 환경 : flask, postgresql, sqlalchemy + alembic, Amazon Web Service : [[EC2](https://aws.amazon.com/ec2), [S3](https://aws.amazon.com/s3), [RDS](https://aws.amazon.com/rds), [Route53](https://aws.amazon.com/route53), [CloudFront](https://aws.amazon.com/cloudfront), [CloudFlare](https://www.cloudflare.com/)]  
> 크롤러 환경 : python, bs4    
> 서비스 주소 : http://www.sscroll.net  

  기존 커뮤니티들의 유머 게시물들을 모바일에서 보기가 어렵다는점에서 아이디어가 떠올랐습니다. 기본적인 데이터는 웹 게시물들을 크롤링해서 DB에 쌓아두고, 이미지들은 S3에 저장하여 클라이언트에서 참조하는 방식으로 개발하였습니다.
</div>
</details>

<details><summary>가상화폐 재정관리 봇 (2017.11-2018.04)</summary>
<div markdown="1">
> 개발 인원 : 1인  
> 개발 환경 : python  

  개인의 가상화폐를 관리하고 거래하는 봇을 만들었습니다.  
  이때 당시 거래소들이 API를 별도로 지원하지 않았기 때문에 직접 API들을 따고, 문서화하여 기능을 구현하였습니다.
</div>
</details>

<details><summary>무료 음원 스트리밍 서비스 워터멜론 서버 개발 (2012)</summary>
<div markdown="1">
> 개발 인원 : 2인  
> 개발 환경 : Flask, Jinja  

 Youtube API와 Music Metadata API를 매쉬업하여 무료 음원 스트리밍 웹서비스 워터멜론을 기획 및 개발하였습니다.  
</div>
</details>

## 학력
세종대학교 컴퓨터공학과 휴학 (2014.03 -)  
한국 애니메이션 고등학교 컴퓨터 게임제작과 졸 (2011.03 - 2014.02)  

## 대외활동
NHN NEXT (2014-2015)  
청년 프론티어 창업지원사업 선정 (2012)  
새싹기업 우수팀 선정 및 미국 연수 (2012)  
소프트웨어 마에스트로 3기 멘티 (2012)  

## 수상
<details open><summary>이매진컵 한국 파이널 라운드 진출 (2015)</summary>
<div markdown="1">
Windows 데스크탑과 모바일에서 OCR 기술을 활용해 사용자의 일상에서 주로 사용되는 컨텐츠에 기반해 맞춤형 언어 학습 기능을 제공하는 Wordpedia를 기획 및 개발하였습니다.  
</div>
</details>

<details open><summary>KWC 동상 수상 (2013)</summary>
<div markdown="1">
Android SDK를 사용하여 안드로이드 앱 작곡 서비스 DRUZIC을 기획 및 개발하였습니다.  
</div>
</details>

<details open><summary>smarteen app challenge 우수상 (2013)</summary>
<div markdown="1">
Android SDK를 사용하여 안드로이드 앱 작곡 서비스 DRUZIC을 기획 및 개발하였습니다.  
</div>
</details>