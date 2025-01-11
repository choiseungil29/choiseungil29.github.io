---
layout: single
author_profile: true
---

최 승일  
연락처 : 010-9034-5202  
이메일 : choiseungil29@gmail.com

## 개발 환경

- 언어: Python, Javascript, C/C++, Java
- 웹 프레임워크 : Django, FastAPI, Flask, Node, Koa
- 웹 프론트 : Vue, React
- 웹 서버 : Nginx
- 데이터베이스 : MySQL, PostgreSQL, Redis, Memcached, SQLite

## 언박서즈 (2024.03 - 2024.05)

<details><summary>AI 프로필 서비스 Concept 개발</summary>
<div markdown="1">
> 개발 인원 : 프론트 2인, 서버 2인
> 클라이언트 환경 : Flutter
> 백엔드 환경 : FastAPI, PostgreSQL

FastAPI를 이용한 서버 개발
비용 최적화 관점에서의 AWS 인프라 최적화를 담당했습니다

</div>
</details>

## 비바 리퍼블리카 (2019.07 - 2024.02)

<details><summary>노션 컨텐츠 to static page 서비스 TCS 서버 및 어드민 개발 (2022.07-)</summary>
<div markdown="1">
> 개발 인원 : 프론트 2인, 서버 2인
> 클라이언트 환경 : React
> 백엔드 환경 : Django, mysql

회사 내에서 생성되는 각종 컨텐츠들의 발행에는 항상 프론트엔드 개발자의 도움이 필요했습니다. 규모가 커질수록, 지면이 넓어질수록 기여해야하는 프론트엔드 개발자의 숫자는 늘어나고 컨텐츠 작성자와 프론트엔드 개발자, 그리고 디자이너의 크로스체크는 복잡도를 점점 올려나가면서 지면의 확장이 컨텐츠 생산속도와 각 개발자의 업무 효율성을 해치는 수준에 이르게 되어 팀 내에서 개발하기 시작한 서비스입니다.

토스 앱 내 `오늘의 머니팁`, 토스뱅크의 `뱅크 새소식`, 토스증권의 `투자는 이렇게`, `약관` 그리고 [토스 블로그](https://blog.toss.im/), [토스 커리어 아티클](https://toss.im/career/article) 등등 각종 토스 내에서 발행되는 컨텐츠들을 모두 노션으로 작성한 뒤 TCS 어드민을 거쳐 저장하고 api로 notion의 데이터와 서비스에 필요한 메타데이터를 함께 실어줘 프론트에서 json 데이터를 파싱해 프론트엔드 화면을 그려내는 방식으로 동작하고 있습니다.

이 과정에서 아래 서술된 기술 관점에서의 의사결정과 구현을 진행해왔습니다.

1. 노션의 데이터를 순수하게 저장할것인가? 아니면 우리만의 문법으로 가공해서 저장할 것인가?
2. 노션의 데이터와 메타데이터를 합쳐서 하나의 Resource로써 API를 작성할것인가? 아니면 둘을 구분할것인가?
3. 여러 법인에서 사용할 수 있어야하는데, 그럼 각 법인별 인프라 환경에 별도의 서버와 DB, 인프라 컴포넌트를 띄울 것인가? 중앙집중형으로 선택할 것인가?
4. `오늘의 머니팁`, `토스 블로그` 같은 경우는 기존의 컨텐츠들이 있고, 각자의 형태로 이미 서비스가 돌아가고 있는 중인데 배포전략을 어떻게 구성함으로써 달리는 차의 바퀴를 갈아 끼울 것인가?
5. `오늘의 머니팁` 은 이미 70만의 구독자가 사용중인 서비스인데 어떻게 신규 서버에서 트래픽을 계측해서 적정 수의 서버를 배치해둘 것인가?
6. 각종 프론트 서비스들이 더 붙게 되었을 때 어떻게 서버 인스턴스의 증설만으로 늘어난 트래픽을 감당해낼 수 있도록 할것인가? (다른 인프라 컴포넌트의 증설 없이)
7. 캐시 레이어는 어떻게 배치해야 앞으로의 유지보수성을 해치지 않을 수 있을것인가?

위 고민의 결과로 현재는 기본적인 트래픽 외에도 분당 3만의 푸시를 200만명에게 발생했을 때, 20%정도의 전환율이 일어나는데 이 때에도 cpu와 memory의 부하 없이 견뎌낼 수 있는 환경을 구성할 수 있게 되었습니다.

</div>
</details>

<details><summary>토스 공지사항과 약관 동의문 관리를 위한 FAQ에디터 개발 (2021.03-2021-07)</summary>
<div markdown="1">
> 개발 인원 : 1인
> 클라이언트 환경 : React
> 백엔드 환경 : Django, mysql

TCS이전 토스 내 각 서비스들(약 100개)의 공지사항 그리고 약관과 동의문 관리를 위해서는 프론트엔드 개발자의 옮겨적기와 배포 그리고 보안팀, 디자이너의 크로스체크가 항상 필요했던 시절이 있었습니다. 해당 과정의 비효율을 제거하고자 시작한 프로젝트입니다.

3개월의 개발과 1개월의 이터레이션 과정을 거치면서 서비스가 개발되었고, 어드민에서는 개별 서비스를 구분하는 Workspace 안의 faq 들을 froala editor를 통해 html로 저장하도록 하고, api를 각 서비스 전담 프론트엔드 개발자분들에게 전달해 html without style의 형태로 전달해 각자의 서비스 형태에 맞게 스타일링 할 수 있도록 제공하게 되었고, 이후 전사 약관 변경 공지사항에도 적용되어 분당 3만 2천만명 대상 발송의 트래픽을 경험해본 바 있습니다.

이 과정에서는 제품 관점과 기술적 관점의 고민들이 함께 있었는데

1. 우리의 api는 응답으로 스타일이 완성된 html을 줄 것인가 스타일이 없는 html을 줄것인가 (api 호출처의 개발 비용 관점)
2. 캐시 정책은 어떻게 해야 할 것인가
3. 프론트엔드의 상태 관리는 어떻게 해야하는가 (이때당시 redux, react-query, recoil 등 다양한 상태관리 도구들이 있었음)

</div>
</details>

<details><summary>그 외 약 30가지의 서비스의 유지보수 (2019.07 -)</summary>
<div markdown="1">
> 개발 인원 : 1인
> 클라이언트 환경 : React, Jinja2
> 백엔드 환경 : Django, mysql

입사 직후 8명의 풀스택 엔지니어가 사내 제품의 상당수를 개발하고, 유지보수를 해야하는 상황이었습니다. 이 상황 안에서 사내 공지사항, 마이페이지, 계약관리, 서비스 에디터 등 다양한 제품의 유지보수를 진행했습니다.

</div>
</details>

## 썸머 (2018.07 - 2019.04)

<details><summary>주문완료 페이지 트래픽 재활용 프로젝트 Loopsum의 API 서버 및 백오피스 개발 (2018.11)</summary>
<div markdown="1">
> 개발 인원 : 2인  
> 클라이언트 환경 : vue  
> 백엔드 환경 : flask, postgresql  
> 관련 기사 : [썸머코퍼레이션, 백엔드 쇼핑 플랫폼 ‘루프썸(loopsum)’ 베타 론칭 블랭크 5,000만 페이지뷰, e커머스와 나눈다](http://blankcorp.kr/bbs/board.php?bo_table=41&wr_id=124)

기존 쇼핑몰들의 주문 완료 페이지에는 별도의 광고를 삽입하지 않고 있었습니다. 하지만 여기에 자사제품을 다시한번 노출시켜 재구매로 이어지게 해보자는 아이디어에서 출발해 프라이빗 몰까지 제공했던 서비스입니다.

회원사 A의 주문 완료 페이지에 loopsum 자체 몰에 대한 광고를 노출시키고, loopsum에서는 A사의 제품 + 그 외의 제품을 최저가로 판매하도록 하는 정책으로 이미 1번 구매 이력이 있는 소비자가 다시 제품에 노출되는 방식의 광고 플랫폼 + 프라이빗 몰 서비스입니다.

해당 서비스를 회원사 내에서 테스트했을 때 유저의 프라이빗 몰 진입 대비 주문 전환율이 10%정도로 나타나기도 했습니다.

해당 서비스의 기획 및 서버와 백오피스 클라이언트를 개발하였습니다. 프라이빗 몰 클라이언트는 Cafe24 서비스를 활용했습니다.

</div>
</details>

<details><summary>AWS 비용 최적화 (2018.10)</summary>
<div markdown="1">

사내 AWS계정의 월간 비용이 400만원을 넘는 시점이 있었습니다. EC2와 RDS의 사용중인 인스턴스의 CPU Utilization를 조사하고 스펙을 조정함으로써 비용을 절감했습니다. S3에서도 CloudFront를 붙여 월간 비용을 200만원가량 절감했습니다.

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

## 크래프톤(구 블루홀) (2017.11 - 2018.02)

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
> [서비스 주소](https://www.sscroll.net)

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
