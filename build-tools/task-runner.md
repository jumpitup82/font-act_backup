---
description: 일련의 작업들을 자동화 하기 위한 도구
---

# Task Runner

### NPM Script

* package.json의 script 속성에 작성
* bash기반 명령어에 익숙해야 하며 간단하게 사용하기 좋
* npm 기반의 프로젝트에서 별도 모듈 설치 없이 사용 가능.

### Grunt

* 다양한 Plug-in과 유틸리티
* NPM script보다 더 많고 복잡할 일은 처리하기 좋음

### 결론

현재는 기존 Task Runner에서 수행하던 많은 기능들을 Webpack과 같은 Bundler의 loader, pulg-in등이 흡수하여 단순히 스크립트 실행하는 정도로만 사용되므로 NPM script 사용으로 충분함.

