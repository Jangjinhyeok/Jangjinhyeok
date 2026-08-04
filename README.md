## 👋 안녕하세요! 게임 클라이언트 개발자 장진혁입니다.
> "게임은 **재미**로, 개발은 **집요함**으로 완성합니다."

저는 플레이어가 **'한 판만 더!'** 를 외치게 만드는 몰입감 있는 경험을 설계하는 것을 목표로 삼고 있습니다.
'꾸준함'을 무기로 삼아, 복잡한 문제를 해결하고 상상을 현실로 구현하는 과정에서 가장 큰 즐거움을 느낍니다.
저의 **집요한 문제 해결 능력**과 **성장하는 것을 즐기는 태도**는 최고의 게임을 만드는 데 강점이 될 것이라고 믿습니다!

## 👨‍💻 About Me
- **UE 5.6 커스텀 엔진 기반 라이브 서비스**에서 클라이언트 프로그래머 1인 체제로 신규 콘텐츠 개발과 레거시 구조 개선을 담당하고 있습니다.
- 상점 진입 시 발생하던 340ms 프레임 스파이크를 Unreal Insights로 추적해 개선한 것처럼, **UI를 화면 조립이 아니라 로딩·데이터·체감 성능까지 포함한 문제**로 다룹니다.
- 이전에는 Unity에서 17개 언어를 지원하는 미니게임 6종을 4개월 내 납품하며, UI·로직·데이터가 얽힌 레거시를 View-Presenter 구조로 재작성했습니다.
- 엔진과 무관하게 **UI 계층 분리와 계측 기반 최적화**를 같은 방식으로 접근하고, 손으로 반복되는 등록 작업은 에디터 도구로 옮깁니다.

## 💼 경력 사항

### 주식회사 셔블 · Unreal 클라이언트 개발자 (정직원) `2025.12 ~ 재직 중`
> **Synthoria** — UE 5.6 커스텀 엔진 기반 라이브 서비스 인터랙티브 월드(메타버스) 플랫폼
> 클라이언트 프로그래머 1인 체제로 서버 개발자와 패킷 사양을 직접 협의하며 개발했습니다.
- **미니게임 'Putt Putt Golf' 클라이언트 단독 개발 (약 2주)** — 기획·아트를 제외한 클라이언트 구현 전반을 담당했습니다. 미니게임 공용 상태 머신(4상태)을 상속해 게임 흐름과 강제 종료·이어하기 처리를 구현하고, 물리 기반 퍼팅 조작·인게임 UMG UI·18개 스테이지 구성과 출시 전 폴리싱까지 수행했습니다.
- **상점 진입 프레임 스파이크 개선** — 상점을 열 때마다 발생하는 프레임 드랍을 Unreal Insights로 계측해 340ms 스파이크의 원인을 동기 에셋 로딩으로 특정하고, 아이템 정의를 1차·썸네일을 2차로 나눈 비동기 프리로딩과 로딩 완료 후 UI를 여는 구조로 전환했습니다.
- **상호작용 시스템 범용화** — 선행 리팩토링 브랜치를 인수해, 의자 전용으로 만들어져 있던 서브시스템을 WorldSubsystem 기반 범용 InteractionSubsystem으로 대체하고 개별 동작을 InteractionAction 계층으로 분리했습니다. 식별을 정수 ObjectId 체계로 재설계해 서버 검증 기준과 오브젝트 확장성을 확보했습니다.
- **상점 통신 게임서버 전환** — HTTP REST 기반 상점 통신을 게임서버 TCP 패킷으로 전환했습니다. 아이템 최대치를 4,680개로 산정해 고정 크기 배열을 나눠 받는 안을 탈락시키고, uint16 길이 헤더 기반 가변 길이 단일 패킷으로 서버 개발자와 사양을 확정했습니다.
- **반복 등록 작업 자동화** — 18개 스테이지의 코인·기믹 배치 좌표를 Unreal Python API로 추출해 DataTable·CSV에 동기화하고, 누락이 잦던 상호작용 오브젝트의 ObjectId 부여·좌표 등록은 Editor Utility Widget으로 레벨을 스캔해 일괄 등록하도록 만들었습니다.
- **외부 앱 연동 (암호화폐 지갑 MetaMask)** — 연동 방식 3종을 비교 검토해 문서화하고 UE 5.5용 플러그인을 5.6에 포팅했으며, PC(QR 코드)·모바일(딥링크) 이중 연결 구조로 PC/iOS/Android에 대응했습니다.
- **라이브 안정성 운영** — 전 작업을 feature 브랜치에서 격리 개발하고, 영향 범위와 테스트 포인트를 문서화한 뒤 반영했습니다.

`UE 5.6` `C++` `Blueprint` `UMG` `Python` `Enhanced Input` `Editor Utility Widget` `DataTable` `TCP 바이너리 프로토콜`

### 롤링씨드 · Unity 클라이언트 개발자 (프리랜서 계약직) `2025.08 ~ 2025.11 (약 4개월)`
> **RollingSeed** — 17개 언어를 지원하는 교육용 미니게임 플랫폼 (Assets 하위 C# 파일 2,473개)
> 레거시 프로젝트의 리마스터 마이그레이션을 1인 전담했습니다.
- **미니게임 6종 마이그레이션 전량 납품** — RollingPop·Orchard·Zoo·Zookeeper·Doctor·FarmersMarket 6종을 4개월 내 1인 전담으로 납품했습니다.
- **다국어 조회 경로 버그 규명** — 명시적으로 전달한 언어 키가 무시되고 에디터 사용자 언어로 번역이 반환되던 문제를, I2 Localization의 2차 조회 경로가 현재 언어에 의존하는 구조에서 원인 특정하고 term 직접 조회로 교체했습니다.
- **Additive Scene 전환 후 UI 입력 유실 원인 규명** — 게임 단독 실행은 정상이고 로비를 경유할 때만 버튼이 반응하지 않는 재현 조건을 분리해, 전환 뒤에도 활성 상태로 남은 로비 Canvas의 GraphicRaycaster가 포인터 이벤트를 가로챈 것을 원인으로 특정했습니다.
- **View-Presenter 분리 및 게임별 구현 이관** — UI·로직·입력·데이터가 한 클래스에 뒤섞인 코드를 View-Presenter 경계로 재작성하고, 공통 게임 루프의 Init-Ready-Play-End-Cleanup 규약 위에서 게임별 RoundController·InitParams를 구현해 6종의 차이를 흡수했습니다.
- **에디터 자동화 도구 2종 제작** — 언어별 사운드마다 반복되던 dictionary 엔트리 생성·Addressables 그룹 등록·GUID 할당을 도구로 옮기고, 두 번째 도구로 확장할 때 폴더 매핑을 17개 언어 명시 매핑으로 바꿔 누락을 제거했습니다. (신체 키 50종 × 17개 언어)
- **비동기·리소스 안정화** — 코루틴 흐름을 UniTask + CancellationToken으로 전환해 이전 연출을 취소하고, DOTween 정리 경로와 Addressables 주소 사전 검증을 추가했습니다.

`Unity 2021.3 LTS` `C#` `UniTask` `Addressables` `I2 Localization` `DOTween` `EditorWindow`

## 🚀 Unreal Projects Summary
✅ 각 프로젝트의 상세 내용은 **Pinned** 저장소 또는 경력 기술서에서 확인하실 수 있습니다.

### [이세계 휴식일지](https://github.com/Jangjinhyeok/ProjectISG-Client)
- **AI 개발팀과 협업**하여 제작한 **멀티플레이** 힐링 게임입니다. (최종 프로젝트 우수상 수상)
- GAS 기반 농사 시스템, 시간 시스템, 수면 시스템 등 핵심 생활 콘텐츠를 개발하고 RPC 통신 문제를 해결했습니다.
- 스팀 멀티플레이 세션 시스템을 만들었습니다.

### [Rider](https://github.com/Jangjinhyeok/ProjectR)
- **멀티플레이** 캐주얼 레이싱 게임입니다.
- RPC/Replication을 활용한 아이템의 멀티플레이 동기화와 데이터 테이블을 기반한 아이템 시스템을 담당했습니다.

### [Vertical](https://github.com/Jangjinhyeok/Project_V)
- 거대 보스와의 전투를 구현한 3인칭 싱글 액션 게임입니다.
- FSM과 AI Perception을 활용한 보스 AI 시스템 및 게임 플로우를 개발했습니다.

### [LostGPU](https://github.com/Jangjinhyeok/LostGPU)
- 블루프린트와 머티리얼 시스템을 깊이 있게 활용한 쿼터뷰 액션 게임입니다.
- 보스 일리아칸과 레벨체인저를 담당했습니다.

## 🚀 Unity Projects Summary

### [Arcade Idle Prototype](https://github.com/Jangjinhyeok/Arcade-Idle-Prototype)
- 채굴 → 가공 → 판매 → 업그레이드로 이어지는 코어 루프를 5일(유효 약 30시간) 안에 완성한 아케이드 아이들 하이퍼캐주얼 프로토타입입니다. (1인 개발)
- 9개 시스템을 개별 구현하면 일정을 넘긴다고 판단해 재사용 축이 되는 추상화 3종(InteractionZone / StackContainer / GameSettingsSO)을 첫날 확정하고 그 위에서 조립했으며, NavMeshAgent 기반 FSM NPC 3종과 오브젝트 풀링을 개발했습니다.
- **AI 코딩 도구(Claude Code)를 적극 활용해 개발한 프로젝트**입니다. 도구에 맡긴 영역과 사람이 판단한 지점을 [`docs/ai-usage.md`](https://github.com/Jangjinhyeok/Arcade-Idle-Prototype/blob/main/docs/ai-usage.md)에 정리했습니다.

### [Last Mechanic](https://github.com/Jangjinhyeok/LastMechanic)
- 인간과 메카 상태를 전환하며 싸우는 3인칭 액션 슈팅 게임입니다. (1인 개발)
- 1인/3인칭 슈팅 시스템과 스킬 시스템, Behavior Tree 기반 보스 AI를 개발했습니다.

### [Cursed Ruins](https://github.com/Jangjinhyeok/CursedRuins)
- 유물 수집과 미니게임을 통해 폐허를 탈출하는 3D 쿼터뷰 공포 게임입니다.
- NavMeshAgent를 이용한 귀신 AI와 랜덤 미니게임 생성 등 핵심 시스템을 개발했습니다.

### [Infinite Dungeon](https://github.com/Jangjinhyeok/InfiniteDungeon)
- 자동 공격과 스킬 강화를 통해 생존하는 탑뷰 서바이벌 게임입니다.
- 레벨업에 따른 난이도 시스템과 레벨업 시 랜덤 3개 옵션을 제공하는 시스템을 구현했습니다.

## 🛠 Skills
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white) ![Unreal Engine](https://img.shields.io/badge/Unreal%20Engine-0E1128?style=for-the-badge&logo=unrealengine&logoColor=white) ![Blueprint](https://img.shields.io/badge/Blueprint-2E72C0?style=for-the-badge&logo=unrealengine&logoColor=white) ![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white) ![Unity](https://img.shields.io/badge/Unity-100000?style=for-the-badge&logo=unity&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white) ![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white) ![Confluence](https://img.shields.io/badge/Confluence-172B4D?style=for-the-badge&logo=confluence&logoColor=white) ![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white)

## 📬 Contact
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:zero9936@gmail.com)
[![Portfolio PDF](https://img.shields.io/badge/Portfolio-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/17JJFBNAEJHLfHY7qsOgjl_QebOcX6-wx/view?usp=sharing)

![Visitor Count](https://komarev.com/ghpvc/?username=Jangjinhyeok&repo=Jangjinhyeok)

