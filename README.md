## 👋 안녕하세요! 게임 클라이언트 개발자 장진혁입니다.
> "게임은 **재미**로, 개발은 **집요함**으로 완성합니다."

저는 플레이어가 **'한 판만 더!'** 를 외치게 만드는 몰입감 있는 경험을 설계하는 것을 목표로 삼고 있습니다.
'꾸준함'을 무기로 삼아, 복잡한 문제를 해결하고 상상을 현실로 구현하는 과정에서 가장 큰 즐거움을 느낍니다.
저의 **집요한 문제 해결 능력**과 **성장하는 것을 즐기는 태도**는 최고의 게임을 만드는 데 강점이 될 것이라고 믿습니다!

## 👨‍💻 About Me
- 확장 가능하고 견고한 아키텍처 설계를 지향합니다.
- 복잡한 문제에 부딪혔을 때, 근본 원인을 분석하고 최적의 해결책을 찾아 적용하는 과정을 즐깁니다.

## 🛠 Skills
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white) ![Unreal Engine](https://img.shields.io/badge/Unreal%20Engine-0E1128?style=for-the-badge&logo=unrealengine&logoColor=white) ![Blueprint](https://img.shields.io/badge/Blueprint-2E72C0?style=for-the-badge&logo=unrealengine&logoColor=white) ![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white) ![Unity](https://img.shields.io/badge/Unity-100000?style=for-the-badge&logo=unity&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white) ![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white) ![Confluence](https://img.shields.io/badge/Confluence-172B4D?style=for-the-badge&logo=confluence&logoColor=white) ![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white)

## 💼 경력 사항

### 주식회사 셔블 · Unreal 클라이언트 개발자 (정직원) `2025.12 ~ 재직 중`
> **Synthoria** — UE 5.6 커스텀 엔진 기반 라이브 서비스 인터랙티브 월드(메타버스) 플랫폼
> 클라이언트 프로그래머 1인 체제로 서버 개발자와 패킷 사양을 직접 협의하며 개발했습니다.
- **미니게임 'Putt Putt Golf' 클라이언트 단독 개발 (약 2주)** — GameMode FSM, 물리 기반 조작, UMG UI, 18개 스테이지 구성 및 출시 전 폴리싱까지 단독 수행했습니다.
- **상호작용 시스템 구조 개선** — 의자 전용으로 설계돼 있던 처리를 NPC 등 신규 타입까지 수용하는 WorldSubsystem 기반 공통 구조로 통합하고, 문자열 식별을 정수 ObjectId 체계로 전환했습니다.
- **상점 시스템 게임서버 전환** — HTTP REST 기반 상점 통신을 TCP 가변 길이 패킷 구조로 재설계하고 클라이언트 측 직렬화·수신 처리를 구현했습니다.
- **성능 최적화** — 상점 진입 시 발생하던 540ms 프레임 스파이크의 원인을 Unreal Insights로 규명하고, 2단계 비동기 프리로딩으로 해소했습니다.
- **스테이지 데이터 파이프라인 자동화** — Python + Editor Utility Widget으로 좌표 추출과 DataTable 동기화를 자동화해, 신규 스테이지 추가가 CSV 행 추가만으로 완결되는 구조를 만들었습니다.

`UE 5.6` `C++` `Blueprint` `UMG` `Python` `Enhanced Input` `Editor Utility Widget` `DataTable` `TCP 바이너리 프로토콜`

### 롤링씨드 · Unity 클라이언트 개발자 (프리랜서 계약직) `2025.08 ~ 2025.11 (약 4개월)`
> **RollingSeed** — 17개 언어를 지원하는 교육용 미니게임 플랫폼
> 레거시 프로젝트의 리마스터 마이그레이션을 1인 전담했습니다.
- **미니게임 6종 마이그레이션 전량 납품** — RollingPop·Orchard·Zoo·Zookeeper·Doctor·FarmersMarket 6종을 4개월 내 1인 전담으로 납품했습니다.
- **View-Presenter 구조 재작성** — UI·로직·입력·데이터가 한 클래스에 뒤섞인 코드를 책임 단위로 분리하고, 공통 게임 루프 위에서 게임별 RoundController·InitParams를 구현해 6종의 차이를 흡수했습니다.
- **다국어 조회 경로 버그 규명** — 명시적으로 전달한 언어 키가 무시되던 문제를, I2 Localization의 2차 조회 경로가 현재 언어에 의존하는 구조에서 원인 특정하고 term 직접 조회로 교체했습니다.
- **에디터 자동화 도구 2종 제작** — 언어별 사운드 등록·Addressables 그룹 연결·GUID 할당의 수작업을 자동화했습니다. (신체 키 50종 × 17개 언어)
- **비동기·리소스 안정화** — 코루틴 흐름을 UniTask + CancellationToken으로 전환하고, DOTween 정리 경로와 Addressables 주소 사전 검증을 추가했습니다.

`Unity 2021.3 LTS` `C#` `UniTask` `Addressables` `I2 Localization` `DOTween` `EditorWindow`

## 🏆 Algorithm
[![Solved.ac 프로필](http://mazassumnida.wtf/api/v2/generate_badge?boj=dinner9936)](https://solved.ac/dinner9936)

## 🚀 Unreal Projects Summary
✅ 각 프로젝트의 상세 내용은 **Pinned** 저장소 또는 경력 기술서에서 확인하실 수 있습니다.

### [이세계 휴식일지](https://github.com/Jangjinhyeok/ProjectISG-Client)
- AI 개발팀과 협업하여 제작한 멀티플레이 힐링 게임입니다. (최종 프로젝트 우수상 수상)
- GAS 기반 농사 시스템, 시간 시스템, 수면 시스템 등 핵심 생활 콘텐츠를 개발하고 RPC 통신 문제를 해결했습니다.

### [Rider](https://github.com/Jangjinhyeok/ProjectR)
- 멀티플레이 캐주얼 레이싱 게임입니다.
- RPC/Replication을 활용한 아이템의 멀티플레이 동기화와 데이터 테이블을 기반한 아이템 시스템을 담당했습니다.

### [Vertical](https://github.com/Jangjinhyeok/Project_V)
- 거대 보스와의 전투를 구현한 3인칭 싱글 액션 게임입니다.
- FSM과 AI Perception을 활용한 보스 AI 시스템 및 게임 플로우를 개발했습니다.

### [LostGPU](https://github.com/Jangjinhyeok/LostGPU)
- 블루프린트와 머티리얼 시스템을 깊이 있게 활용한 쿼터뷰 액션 게임입니다.
- 보스 일리아칸과 레벨체인저를 담당했습니다.

## 🚀 Unity Projects Summary

### [Arcade Idle Prototype](https://github.com/Jangjinhyeok/Arcade-Idle-Prototype)
- 채굴 → 가공 → 판매 → 업그레이드로 이어지는 코어 루프를 5일(약 30시간) 안에 완성한 아케이드 아이들 하이퍼캐주얼 프로토타입입니다. (1인 개발)
- InteractionZone·StackContainer 등 재사용 축이 되는 추상화를 먼저 확정해 9개 시스템을 그 위에서 조립했고, FSM 기반 NPC 3종과 오브젝트 풀링을 개발했습니다.

### [Last Mechanic](https://github.com/Jangjinhyeok/LastMechanic)
- 인간과 메카 상태를 전환하며 싸우는 3인칭 액션 슈팅 게임입니다. (1인 개발)
- 1인/3인칭 슈팅 시스템과 스킬 시스템, Behavior Tree 기반 보스 AI를 개발했습니다.

### [Cursed Ruins](https://github.com/Jangjinhyeok/CursedRuins)
- 유물 수집과 미니게임을 통해 폐허를 탈출하는 3D 쿼터뷰 공포 게임입니다.
- NavMeshAgent를 이용한 귀신 AI와 랜덤 미니게임 생성 등 핵심 시스템을 개발했습니다.

### [Infinite Dungeon](https://github.com/Jangjinhyeok/InfiniteDungeon)
- 자동 공격과 스킬 강화를 통해 생존하는 탑뷰 서바이벌 게임입니다.
- 레벨업에 따른 난이도 시스템과 레벨업 시 랜덤 3개 옵션을 제공하는 시스템을 구현했습니다.

## 📬 Contact
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:zero9936@gmail.com)
[![Portfolio PDF](https://img.shields.io/badge/Portfolio-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/17JJFBNAEJHLfHY7qsOgjl_QebOcX6-wx/view?usp=sharing)

![Visitor Count](https://komarev.com/ghpvc/?username=Jangjinhyeok&repo=Jangjinhyeok)

