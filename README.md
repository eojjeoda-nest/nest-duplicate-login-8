# 미션 - 중복 로그인 방지 구현 미션

## 🎯 서버 세팅 방식
- setup.sh 스크립트를 실행하여 서버를 세팅한다.
- setup.sh 스크립트는 다음과 같은 작업을 수행한다.
  - orm `typeorm, prisma`, 패키지 매니저 `npm, yarn, pnpm` 선택
  - npm install | yarn | pnpm install 실행

```bash
./setup.sh
```

## 🔍 진행 방식

- 미션은 **기능 요구 사항, 프로그래밍 요구 사항, 과제 진행 요구 사항** 세 가지로 구성되어 있다.
- 세 개의 요구 사항을 만족하기 위해 노력한다. 특히 기능을 구현하기 전에 기능 목록을 만들고, 기능 단위로 커밋 하는 방식으로 진행한다.
- 기능 요구 사항에 기재되지 않은 내용은 스스로 판단하여 구현한다.

## 📮 미션 제출 방법

- 미션 구현을 완료한 후 GitHub PR 요청을 통해 제출합니다.

---

## 🚀 기능 요구 사항

중복 로그인 방지 기능을 구현한다.
하나의 계정에 A 유저가 로그인하고 있을 때, 현재 접속 클라이언트와 다른 클라이언트에서 B 유저가 로그인을 시도하면, 기존 유저의 로그인을 강제로 로그아웃시킨다.

### 구현 Tip!
- Socket.IO, GateWay를 이용하여 구현할 수 있다.


### 공통 필수 예외처리 사항

- API에 요청받은 Body 값의 타입을 검증하여 올바르지 않은 타입일 경우 `400 BadRequest` 에러를 리턴해야한다.
- API에 요청받은 Body 값의 필수 값이 누락되거나/빈 값인 경우 `400 BadRequest` 에러를 리턴해야한다.


### API 요청/응답 요구 사항
1. 모든 API의 요청/응답은 DTO를 통해 TypeSafe하게 이루어져야한다.
2. DTO의 타입은 `class-validator`를 이용하여 검증한다.
3. DTO 내부 요소의 명칭은 `camelCase`로 작성한다.

## 🎯 프로그래밍 요구 사항

- **Javascript 코드가 아닌 Typescript 코드로만 구현해야 한다.**
- **Swagger**를 이용하여 API 명세를 작성한다.
- **package.json**에 명시된 라이브러리만을 이용하여 구현한다.
- **eslint**, **prettier** 등의 코드 포맷팅 라이브러리를 이용하여 제공된 코드 컨벤션에 맞추어 코드를 작성한다.
- `node`, `npm` 버전은 `package.json`에 명시된 버전을 사용한다. [Volta를 이용하여 node 버전을 관리한다.](https://docs.volta.sh/guide/getting-started)
---

## ✏️ 과제 진행 요구 사항

- 미션은 [nest-duplicate-login-8](https://github.com/eojjeoda-nest/nest-duplicate-login-8) 저장소를 Fork & Clone 하고 시작한다.
- **기능을 구현하기 전 `README.md`에 구현할 기능/예외처리를 목록으로 정리**해 추가한다.