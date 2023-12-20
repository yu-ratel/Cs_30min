# CI (Continuous Integration) /CD(Continuous Delivery) 🧑🏻‍💻

- CI / CD
  > 하나의 서비스를 위해서 service를 제공 할때 발생하는 문제(Code의 충돌, test의 부재) 등을 해결하고 배포에 이르기 까지의 과정을 강제하여 효과적으로 제공하기 위한 용어

### CI 지속적 통합

- 핵심목표

  - 버그를 신속히 해결, sw의 품질 개선, new update 의 검증 및 release 시간 단축

- Build

  - 웹을 나타낼 수 없는 확장자 등으로 웹을 나타낼 수 있게 하는 과정 ex) webpack

- Test

  - mocha => Test를 위한 대표적인 Framework

  - 단위 테스트
    - 단일 모듈에 대한 테스트
  - 통합 테스트
    - 모듈을 합치는 테스트
  - End_To_End 테스트
    - 실 사용자의 행동을 가정하여 테스트 하는 것 ex) 어떤 라우터에 정보가 입력되면 잘 입력이 되는지 등

- Merge
  - git 같은 tool을 이용하여 code를 합치는 것
  - 충돌을 최소화 해야함
    > 충돌은 대부분 일어나기에 _작은이슈_ 단위를 기반으로 머지를 해야함.

### CD 지속적 서비스, 지속적 배포

- 배포

  - 사용자를 위한 서비스 배포 뿐만이 아닌 내부적으로 QA엔지니어, 관리자페이지를 위한 배포, 백엔드 개발자를 위한 데이터 가공 후 배포 등을 모두 포함함.

- tool
  - github action, genkins, circle, ci, heroku(CI/CD 설정없이 자동가능 간단한 프로젝트시 유용함, git action과 상호가능)

### CI/CD 파이프라인

- 지속적 통합 -> 지속적 서비스 -> 지속적 배포

> build => Test => Merge (Continuous Integration)

> Automatically_Release_To_Repository (Continuous Delivery)

> Automatically_Deploy_To_Production (Continuous Deployment)
