## 게임 클라이언트 개발자 장진혁

> 문제를 감으로 고치지 않고, 원인을 확인한 뒤에 고칩니다.

UE와 Unity에서 클라이언트 개발을 담당하고 있습니다. 현재는 라이브 서비스 중인 플랫폼에서 클라이언트 1인 담당으로 신규 콘텐츠와 레거시 구조 개선을 맡고 있습니다.

## 👨‍💻 About Me

UE5와 Unity 양쪽에서 실무 경험을 쌓은 게임 클라이언트 프로그래머입니다. 레거시 구조 개선, 성능 최적화, 반복 작업 자동화를 중심으로 개발해왔습니다.

Unity 클라이언트 개발자로 커리어를 시작했습니다. 교육용 미니게임 플랫폼의 레거시를 리마스터로 넘기는 마이그레이션을 1인 전담으로 맡아 미니게임 6종을 4개월 내 전량 납품했고, 설계 문서 없이 남은 레거시 코드를 직접 읽어 동작 규칙을 추출한 뒤 MVP 구조로 재작성했습니다. 다국어 조회 경로 버그를 원인까지 추적해 해결했고, 200개가 넘는 사운드 에셋의 반복 등록 작업은 에디터 도구 2종으로 자동화했습니다.

현재는 UE 5.6 기반 라이브 서비스에서 클라이언트 프로그래머 1인 체제로 신규 콘텐츠 개발과 구조 개선을 병행하고 있습니다. 미니 골프 게임을 기획부터 폴리싱까지 2주 만에 단독 구현했고, 상점 시스템의 프레임 스파이크를 Unreal Insights로 분석해 2단계 비동기 프리로딩으로 완전히 해소했습니다. 전임자가 착수만 해둔 상호작용 리팩토링 브랜치를 인수해 범용 서브시스템으로 재설계했고, 반복되는 좌표 등록 작업은 Python과 Editor Utility Widget으로 자동화했습니다. 서버 개발자와는 패킷 사양을 직접 협의하며 개발하고 있습니다.

## 💼 경력 사항

### 주식회사 셔블 · Unreal 클라이언트 개발자 (정직원) `2025.12 ~ 재직 중`

> **Synthoria** — UE 5.6 기반 라이브 서비스 인터랙티브 월드(메타버스) 플랫폼
> 클라이언트 프로그래머 1인 담당으로, 서버 개발자와 패킷 사양을 직접 협의하며 개발했습니다.

- **미니 골프 게임 클라이언트 단독 개발 (약 2주)** — 2주 제약에서 18개 스테이지 제작에 필요한 시간을 역산해, 미니게임 공용 상태 머신(4상태)을 상속하고 골프 고유 규칙인 강제 종료·이어하기·결과 판정만 추가하는 방향으로 범위를 좁혔습니다. 기획·아트를 제외한 클라이언트 구현 전반(물리 기반 퍼팅 조작, 인게임 UMG UI, 18개 스테이지 구성, 출시 전 폴리싱)을 담당했습니다.

- **상점 진입 프레임 스파이크 개선** — 상점을 열 때마다 발생하는 프레임 드랍을 Unreal Insights로 계측했습니다. 처음에는 썸네일 텍스처를 원인으로 보고 프리로딩을 적용했으나 효과가 없었고, 그 결과로 병목이 아이템 정의의 동기 로딩임을 트레이스에서 특정했습니다. 340ms대 스파이크에 대해 아이템 정의를 1차·썸네일을 2차로 나눈 비동기 프리로딩과 로딩 완료 후 UI를 여는 구조로 전환했고, 장착 아이템의 스폰 대상을 소프트 레퍼런스로 바꿔 정의 로드 시 따라오던 연쇄 로딩을 끊었습니다.

- **상호작용 시스템 범용화** — 선행 리팩토링 브랜치를 인수해, 상호작용 타입이 늘어날 때마다 전용 서브시스템이 함께 늘어나는 구조를 문제로 정리했습니다. 각 Action 직접 등록안·범용 서브시스템안·Multicast 델리게이트안을 확장 비용과 서버 검증 가능성 기준으로 비교해 WorldSubsystem 기반 `InteractionSubsystem`을 채택하고, 개별 동작을 `InteractionAction` 계층으로 분리했습니다. 식별을 정수 ObjectId 체계로 재설계해 서버 검증 기준과 오브젝트 확장성을 확보했으며, 착석 패킷 크기도 6byte에서 5byte로 줄었습니다.

- **상점 통신 게임서버 전환** — HTTP REST 기반 상점 통신을 게임서버 TCP 패킷으로 전환했습니다. 아이템 최대치를 4,680개로 산정해 고정 크기 배열을 나눠 받는 안을 탈락시키고, uint16 길이 헤더 기반 가변 길이 단일 패킷으로 서버 개발자와 사양을 확정했습니다.

- **반복 등록 작업 자동화** — 좌표를 손으로 옮기면 오타가 반복될 구조라고 판단해, 스테이지의 코인·기믹 배치 좌표를 Unreal Python API로 추출해 DataTable·CSV에 동기화했습니다. 누락이 잦던 상호작용 오브젝트의 ObjectId 부여·좌표 등록은 Editor Utility Widget으로 레벨을 스캔해 일괄 등록하도록 만들었습니다.

- **외부 앱 연동 (암호화폐 지갑 MetaMask)** — 연동 방식 3종을 비교 검토해 문서화하고 UE 5.5용 플러그인을 5.6에 포팅했으며, PC(QR 코드)·모바일(딥링크) 이중 연결 구조로 PC/iOS/Android에 대응했습니다.

`UE 5.6` `C++` `Blueprint` `UMG` `Python` `Enhanced Input` `Editor Utility Widget` `DataTable` `Unreal Insights` `TCP 바이너리 프로토콜`

### 롤링씨드 · Unity 클라이언트 개발자 (프리랜서 계약직) `2025.08 ~ 2025.11 (약 4개월)`

> **RollingSeed** — 17개 로케일을 지원하는 영어 단어 학습용 미니게임 모음집
> 레거시 프로젝트의 리마스터 마이그레이션을 1인 전담했습니다.

- **미니게임 6종 마이그레이션 전량 납품** — RollingPop·Orchard·Zoo·Zookeeper·Doctor·FarmersMarket 6종을, 게임별 레거시 구조를 먼저 분석해 이관 순서와 범위를 정한 뒤 약 4개월 내 1인 전담으로 납품했습니다.

- **동작 규칙 재현 및 게임별 구현 이관** — 설계 문서가 없어 레거시 코드만 보고 각 게임의 동작 규칙을 추출한 뒤, UI·로직·입력·데이터가 한 클래스에 뒤섞인 코드를 View-Presenter 경계에 맞춰 재작성했습니다. 공통 게임 루프의 `Init-Ready-Play-End-Cleanup` 규약 위에서 게임별 `RoundController`·`InitParams`를 구현해 6종의 차이를 흡수했습니다.

- **다국어 조회 경로 버그 규명** — 명시적으로 전달한 언어 키가 무시되고 사용자 언어로 번역이 반환되던 문제에서, 처음에는 조회 필터를 좁히는 방식을 적용했으나 후보 자체가 사라져 원복했습니다. 이후 I2 Localization의 2차 조회 경로가 현재 언어에 의존하는 구조임을 특정하고 term 직접 조회로 교체했습니다.

- **Additive Scene 전환 후 UI 입력 유실 원인 규명** — 게임 단독 실행은 정상이고 로비를 경유할 때만 버튼이 반응하지 않는 재현 조건을 분리해, 전환 뒤에도 활성 상태로 남은 로비 Canvas의 GraphicRaycaster가 포인터 이벤트를 가로챈 것을 원인으로 특정했습니다.

- **에디터 자동화 도구 2종 제작** — 사운드 에셋 등록이 언어 수만큼 손으로 반복되는 구조를 보고, dictionary 엔트리 생성·Addressables 그룹 등록·GUID 할당을 도구로 옮겼습니다. 두 번째 도구로 확장할 때는 폴더 구조와 키 네이밍 규칙을 먼저 정의해, 언어를 파일명에서 빼고 17개 로케일 명시 매핑으로만 구분하도록 바꿨습니다. (신체 키 50종 × 17개 로케일)

- **비동기·리소스 안정화** — 코루틴 흐름을 UniTask + CancellationToken으로 전환해 이전 연출을 취소하고, DOTween 정리 경로와 Addressables 주소 사전 검증을 추가했습니다.

`Unity 2021.3 LTS` `C#` `UniTask` `Addressables` `I2 Localization` `DOTween` `EditorWindow`

## 🚀 Unreal Projects

> 상세 내용은 **Pinned** 저장소 또는 경력 기술서에서 확인하실 수 있습니다.

### [이세계 휴식일지](https://github.com/Jangjinhyeok/ProjectISG-Client)

- **AI 개발팀**과 협업해 제작한 **멀티플레이** 힐링 게임입니다. (최종 프로젝트 우수상 수상)
- GAS 기반 농사·시간·수면 등 핵심 생활 콘텐츠와 스팀 멀티플레이 세션 시스템을 개발했습니다.
- 클라이언트 소유가 아닌 액터에서 RPC가 전달되지 않는 문제를, 플레이어 캐릭터를 중개자로 두는 구조로 바꿔 해결했습니다.

### [Rider](https://github.com/Jangjinhyeok/ProjectR)

- **멀티플레이** 캐주얼 레이싱 게임입니다.
- RPC/Replication 기반 아이템 동기화와 DataTable 기반 아이템 시스템을 담당했습니다.

### [Vertical](https://github.com/Jangjinhyeok/Project_V)

- 거대 보스와의 전투를 구현한 3인칭 싱글 액션 게임입니다.
- Behavior Tree 대신 State 패턴 기반 FSM을 택해 보스 AI와 게임 플로우를 개발했으며, AI Perception과 벡터 내적을 이용해 플레이어의 전후방을 판정하고 패턴을 분기했습니다.

### [LostGPU](https://github.com/Jangjinhyeok/LostGPU)

- 블루프린트와 머티리얼 시스템을 깊이 있게 활용한 쿼터뷰 액션 게임입니다.
- 보스 일리아칸과 레벨 체인저를 담당했습니다.

## 🚀 Unity Projects

### [Arcade Idle Prototype](https://github.com/Jangjinhyeok/Arcade-Idle-Prototype)

- 채굴 → 가공 → 판매 → 업그레이드로 이어지는 코어 루프를 5일(유효 약 30시간) 안에 완성한 아케이드 아이들 하이퍼캐주얼 프로토타입입니다. (1인 개발)
- 9개 시스템을 개별 구현하면 일정을 넘긴다고 판단해 재사용 축이 되는 추상화 3종(`InteractionZone` / `StackContainer` / `GameSettingsSO`)을 첫날 확정하고 그 위에서 조립했으며, NavMeshAgent 기반 FSM NPC 3종과 오브젝트 풀링을 개발했습니다.
- 설계 판단과 스코프 컷 사유는 ADR 문서로, 스펙 이탈은 deviation으로 남겼습니다.
- **AI 코딩 도구(Claude Code)를 적극 활용해 개발한 프로젝트**입니다. 도구에 맡긴 영역과 사람이 판단한 지점을 [`docs/ai-usage.md`](https://github.com/Jangjinhyeok/Arcade-Idle-Prototype/blob/main/docs/ai-usage.md)에 정리했습니다.

### 그 외

- [**Last Mechanic**](https://github.com/Jangjinhyeok/LastMechanic) — 인간과 메카 상태를 전환하며 싸우는 3인칭 액션 슈팅 게임 (1인 개발). 슈팅·스킬 시스템과 Behavior Tree 기반 보스 AI를 개발했습니다.
- [**Cursed Ruins**](https://github.com/Jangjinhyeok/CursedRuins) — 유물 수집과 미니게임으로 폐허를 탈출하는 3D 쿼터뷰 공포 게임. NavMeshAgent 기반 귀신 AI와 랜덤 미니게임 생성을 개발했습니다.
- [**Infinite Dungeon**](https://github.com/Jangjinhyeok/InfiniteDungeon) — 자동 공격과 스킬 강화로 생존하는 탑뷰 서바이벌 게임. 레벨업 난이도 시스템과 랜덤 3택 강화 시스템을 구현했습니다.

## 🛠 Skills

![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white) ![Unreal Engine](https://img.shields.io/badge/Unreal%20Engine-0E1128?style=for-the-badge&logo=unrealengine&logoColor=white) ![Blueprint](https://img.shields.io/badge/Blueprint-2E72C0?style=for-the-badge&logo=unrealengine&logoColor=white) ![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white) ![Unity](https://img.shields.io/badge/Unity-100000?style=for-the-badge&logo=unity&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white) ![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white) ![Confluence](https://img.shields.io/badge/Confluence-172B4D?style=for-the-badge&logo=confluence&logoColor=white) ![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white)

## 📬 Contact

[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:zero9936@gmail.com)
[![Portfolio PDF](https://img.shields.io/badge/Portfolio-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/17JJFBNAEJHLfHY7qsOgjl_QebOcX6-wx/view?usp=sharing)

![Visitor Count](https://komarev.com/ghpvc/?username=Jangjinhyeok&repo=Jangjinhyeok)