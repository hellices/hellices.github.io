SI를 진행하며 작성했던 개발 프레임워크 정리(01)
=================
요즘 프로젝트를 진행하면 표준 개발 프레임워크가 지정되어 있지 않다.
매번 새롭게 작성하게 되는데, 할 때마다 고민하는 부분이 정해져 있는 느낌.
한번 시원하게 정리하고 나중에 하면서 업데이트해보자.

- 기본 구조
:   UI / API 서비스 두 종류가 있다고 생각.
:   MSA로 나누더라도 각각 성격에 맞게 프레임워크를 가져다 쓰면 될 듯.
- UI
:   language : javascript(`react`)
:   서버에서 선 로직 처리를 하려면 server-side-rendering 방식이 좋다고 생각. -> Next.js
:   UI도 컴포넌트로 작성하고 싶음 -> material-ui
:   testing tool(optional) -> jest + enzyme(화면개발보다 더 노가다...) / react-test-renderer(안써봄) / mocha(jest와 거의 같은듯?)
- API
:   language : java(`spring boot`)
:   mvc가 가장 익숙하지만, spring webflux도 점차 성숙해지는 듯. mvc랑 webflux를 하나씩 해보면서 비교하자
:   database : mvc(mariadb) / webflux(mongodb)

- 필요 라이브러리를 첨부터 설치하지 말고 필요 기능에 맞춰 하나씩 올려도 됨. 이렇게 해야 빠르게 시작하기 좋은듯

- IDE
:   VS Code
:   extension을 설치하면 STS와 비슷하게 사용 가능

- Proxy
:   kubernetes에 배포되는 환경을 고려하여 비슷하게 proxy를 설치
:   nginx
:   서비스 통합 관점에서 api gateway(`kong`) / service mesh(`istio`) 도입도 고민해 볼 수 있을듯