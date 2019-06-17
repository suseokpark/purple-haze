# [Quasar](https://quasar.dev/introduction-to-quasar) App


## 주요디렉토리 구조

- src
    - assets : 컴포넌트 구성에 필요한 이미지 등의 리소스. webpack에서 참조 함
    - boot : 초기 기동 시 import 되어야 하는 외부 js 라이브러리
    - components : 개별적으로 동작 가능한 컴포넌트
    - css : 전체 컴포넌트에서 사용하거나 다른 프로그래밍 적으로 핸들링이 필요한 스타일
    - layouts : 화면 레이아웃
    - pages : 페이지 구성 컴포넌트 
    - router : 라우팅 설정 관련
    - statics : webpack을 통하지 않고 그대로 배포 됨
    - store : 상태 관리


## 주요 명령어
1. 로컬 서버 실행
`qusar dev`

2. [프로덕션 빌드](https://quasar.dev/quasar-cli/developing-spa/build-commands)
`quasar build`


## [아이콘 관련](https://quasar.dev/options/quasar-icon-sets#Full-Example)

## 퀘이사 컴포넌트 추가 방법
quasar.conf.js 파일 상에 사용하는(화면 표시 시 오류 발생하는 컴포넌트 명 어레이 상 추가)

## class 스타일에 todo 로 준 것 위주로 작업할 것
## 샘플은 Coupon 관련해서 볼 것
## 크롬 플러그인 [Vue.js devtools](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?utm_source=chrome-ntp-icon) 설치할 것