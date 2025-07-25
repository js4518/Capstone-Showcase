## 캡스톤디자인I / 사이버펑크+디스토피아 로그라이트 액션 게임 개발

![LOGO](https://github.com/user-attachments/assets/2ecc832f-2e67-4414-80a4-abcab8d6ef33)

![Fight](https://github.com/user-attachments/assets/ba218ed6-a561-4169-8db0-66ddc1a8bf83)

![9 -ezgif com-video-to-gif-converter (1)](https://github.com/user-attachments/assets/298eccf7-b442-477a-b031-0730cba74608)

내부 에셋 저작권으로 인한 파일 제외

직접 작성한 스크립트 중 일부만 업로드

프로젝트 진행 기간 : **2025.03 ~ 2025.06**

프로젝트 위키 : http://cscp2.sogang.ac.kr/CSE4186/index.php/%EC%BA%A1%ED%81%AC%EB%9E%98%ED%94%84%ED%8A%B8

STOVE 스토어 : https://store.onstove.com/ko/games/101515

전체 플레이 영상 : https://youtu.be/UVl7yaMmQIA?si=dm9YSfIsRDznCu49

<h2>개발 목표</h2>

본 프로젝트는 사이버펑크 디스토피아 세계관을 배경으로, 플레이어가 탐사 로봇을 조작하여 월드를 반복 탐사하고 진실에 접근해나가는 2D 로그라이트 액션 게임을 개발하는 것을 목표로 한다. 

플레이어는 탐사기지의 주인공으로서, 탐사 로봇을 원격 조종해 각 월드를 탐사하고, 탐색률 100% 달성을 목표로 하며, 반복적인 플레이 속에서 무기와 스킬, 능력치를 점진적으로 강화해 나가야 한다.

<h2>개발 범위</h2>

<h3>탐사 기반 스테이지 구조 구현</h3>

 탐사기지에서 시작하여 월드를 반복 탐사하는 구조 설계

 각 월드는 무작위로 구성된 룸 단위 맵으로 탐색 진행

 각 월드는 탐색률(%)로 진행도를 기록하며, 100% 달성 시 완료

<h3>플레이어 성장 시스템 구현</h3>

 장신구 슬롯 시스템으로 무기 강화 기능 개발

 부품(재화) 소비를 통한 능력치(체력, 이속, 쿨타임 등) 영구 강화 기능 구현

 반복 탐사를 통해 점진적인 성장 가능 구조 구현

<h3>무기 및 전투 시스템 구현</h3>

 4종의 무기와 각 무기별 고유 스킬 2종 구현

 적 피격 시 타격 이펙트, 히트스톱, 카메라 셰이크 등 연출 요소 구현

 두 개의 무기를 장착하고 전투 중 전환 가능

<h3>탐사 실패 리스크 및 게임 오버 시스템 구현</h3>

 탐사 중 사망 시 ‘악성코드 추적도’ 증가

 일정 수치 이상 누적 시 게임 오버 처리 시스템

 게이지 시각화 및 상태 표현 UI 구현

<h3>해킹 기반 궁극기 시스템 구현</h3>

 해킹 효과는 전투를 보조하는 형태(군중제어, 딜링 등)로 구성

<h3>기본 시스템 및 UI 구현</h3>

 탐사 로봇 조작: 이동, 점프, 회피, 공격, 무기 전환

 적 AI, 피격 판정, 보스 패턴 등 전투 구성 요소

 HUD: 체력, 스킬, 탐색률, 악성코드 상태 등 게임 정보 표시

 게임 데이터 저장/로드 시스템

<h3>확장 가능한 데이터 중심 구조 설계</h3>

 무기, 스킬, 장신구, 해킹, 적 등을 ScriptableObject 기반으로 관리하여 유지보수성과 확장성 확보

<h2>프로젝트 세부사항</h2>

<h3>역할 분담</h3>

|이름	|개발 측면|	프로젝트 관리 측면|
|------|---|---|
|**송종서**|	에너미, 룸 시스템, 탐사 기지 시스템 등 설계/구현, 월드 디자인 및 제작|	팀장, 일정/위키 관리|
|김택림|	플레이어 행동, 무기 및 스킬 시스템, 장신구 시스템, 보스 패턴 설계/구현|깃허브 관리|
|최준혁|	해킹 시스템, 보스 시스템 설계/구현, 타이틀 디자인|발표, 멘토 컨택|
|이송은|	자원, 인벤토리, 장비 강화, 상점 시스템 등 설계/구현, 애니메이션 적용|회의 관리|

<h3>진행 사항</h3>

|기간	|내용|
|------|---|
|3.17~3.23|협업 툴, 사용할 엔진 결정|
|3.24~3.30|프로젝트 제안서 작성, 장르 결정|
|3.31~4.6|기초적 기능 설계 및 구현|
|4.7~4.13|기본 무기, UI, 맵 시스템 설계 및 구현 / asset 결정|
|4.14~4.20|맵 디자인 / 무기, 해킹 시스템 설계 및 구현|
|4.21~4.27|무기, 해킹 추가 구현 / 적, 기본 애니메이션 구현|
|4.28~5.4|월드 제작, 에셋 적용|
|5.5~5.11|적 추가 구현, 강화 부품 시스템 설계 및 구현|
|5.12~5.18|탐사 기지, 보스 패턴, 상점 시스템 설계 및 구현|
|5.19~5.25|이벤트 및 보상 방, 장신구, 인벤토리 시스템 설계 및 구현|
|5.26~6.1|타이틀 씬 제작, 세이브 로드 구현|
|6.2~6.8|사운드 디자인, 튜토리얼, 게임오버 구현 / 내부 테스트|
|6.9~6.15|베타 테스트 / 게임 출시|

<h2>담당 파트</h2>

<h3>RoomManager 제작 – 룸, 룸 관리, 룸 이동 시스템</h3>

![image](https://github.com/user-attachments/assets/67c96f93-aac0-4d80-88e4-098ac0edb883)

![image](https://github.com/user-attachments/assets/a5d04a4f-f496-4978-bdb5-98f14e53c7bb)
![image](https://github.com/user-attachments/assets/6816eb3d-b77b-4aa2-b6c6-aa2e9088d256)

![맵이동](https://github.com/user-attachments/assets/96116942-7703-41fc-bd38-b06782f90142)

한 번의 탐사는 5개의 룸으로 구성된다. 이렇게 등장하는 각 룸의 구조를 설계/구현하였다. 각 룸은 프리팹의 형태로 처리되고, 배경/지형 타일맵/에너미 스폰 위치 등 정보를 저장하게 하였다.

에너미 룸 / 보상 룸 / 이벤트 룸의 세 타입의 룸 시스템을 구현하였다. 에너미 룸에서는 각각의 설정된 위치에, 지정된 에너미 종류 중 하나가 소환되게 하였다. 소환된 에너미를 전부 처치하면 룸을 클리어할 수 있게 조건을 설정하였으며, UI와 연동하여 플레이어가 룸 클리어 여부를 인지할 수 있게 하였다. 룸이 클리어되면 룸 우측의 포탈이 활성화되게 하였고, 포탈 쪽으로 카메라를 이동시키는 컷씬을 구현하여, 룸이 클리어될시 포탈이 활성화된다는 것을 인지할 수 있게 하였다.

보상 룸에서는 많은 양의 자원을 얻거나, 체력을 회복할 수 있게 구현하였다. 이벤트 룸에서는 특정 상황 이벤트를 주고, 플레이어가 이벤트를 수행할지 선택할 수 있게 하였다. 이후 이벤트 수행시 확률에 따라 긍정/부정적인 효과가 발생하게 하였다. 또한 상점 이벤트 또한 구현하여, 이벤트 룸 중 하나에서 등장하게 하였다. 

룸 프리팹은 Prefab Varient를 이용한 다중 상속 구조를 따른다. 모든 룸의 기본이 되는 Default 프리팹이 있고, EnemyDefault/RewardDefault/EventDefault 프리팹은 Default 프리팹을 상속한 구조를 가진다. 이후 각 타입의 룸들은 각 룸 타입의 Default 프리팹을 상속한다. 이와 같은 구조를 통하여 룸 타입마다 가져야 할 특수한 요소들을 공통 적용하고, 기초 구조가 바뀌면 이를 상속하는 하위 구조들도 동시에 변경될 수 있다.

이러한 룸 시스템을 이용하여, 플레이어가 속한 룸의 관리/룸의 생성 및 제거/클리어 처리/룸 이동을 담당하는 RoomManager 컴포넌트를 정의하였다.

RoomManager를 통해 플레이어가 룸 클리어시 등장하는 포탈에 들어가면, 다음 룸으로 이동할 수 있는 UI를 출력하였다. UI에서는 양자택일의 분기 구조를 바탕으로 플레이어가 두 개의 룸 중 하나의 룸을 선택할 수 있게 하였다. 등장하는 룸 선택지는 지정된 확률로 각 룸 타입의 룸이 등장하게 설정하였다. 또한 4개의 룸 클리어시 보스 룸이 등장하게 하였다.

또한 룸 이동시, 기존에 있던 룸 제거/플레이어 위치 재지정을 처리하였다.

주요 이슈 및 해결 :

룸 구조 설계 초기에는, 각 룸 프리팹이 개별적인 구조를 가지고 있었다. 이에 따라 각 룸에서 룸의 크기 등 설정 요소에 변경이 생기면, 다른 룸에도 모두 직접 변경해줘야 하는 수고가 있었다. 따라서 이를 개선하기 위해 Prefab Varient를 이용한 다중 상속 구조를 사용하였다.

<h3>EnemyManager 제작 – 에너미, 에너미 스폰, 에너미 데이터 저장 구조 구현</h3>

![image](https://github.com/user-attachments/assets/079e1fc8-e08a-49e8-9dde-9a5716dec923)
![image](https://github.com/user-attachments/assets/1f827d01-b3c4-4c18-94a2-c268fa498b3a)

![image](https://github.com/user-attachments/assets/572bbaf9-b658-479d-abc1-f8d78777c35d)

에너미의 행동 패턴, 로직, 애니메이션을 구현하였다. 우선 Scriptable Object를 이용하여 각 에너미의 데이터(에너미 ID, 이동 속도, 공격 속도 등)을 저장하였고, 이 데이터를 이용하여 EnemyManager가 에너미의 초기 설정을 초기화하게 하였다. 모든 에너미는 같은 프리팹을 공유하며 초기화에 의해서 각 에너미 종류로써의 특성을 가지게 하였다. 또한 자신의 ID에 따라 다른 행동 패턴을 사용하여 설정하였다.
차징 후 돌진/차징 후 점프/돌진 후 자폭/은신 후 원거리 공격의 4가지 행동 패턴을 구현하였다. 에너미는 플레이어가 공격 범위 안에 들어올시 자신의 행동 패턴에 따라 행동하고, 그렇지 않다면 룸의 배회하게 구현하였다. (다른 팀원이 구현한 기초 에너미 2종을 기반으로 제작하였다)

또한, 에너미의 피격/플레이어와의 충돌/사망 처리를 구현하였다.

이와 같이 구현한 에너미의 스폰/디스폰 처리를 담당하는 EnemyManager 컴포넌트를 정의하였다. EnemyManager는 RoomManager 등에서 에너미 스폰 요청이 들어오면, 에너미 데이터를 이용하여 입력받은 위치에 에너미를 스폰하거나, 디스폰한다. 또한, 스폰된 에너미의 숫자를 카운트하며 RoomManager에 룸 클리어 조건 달성 여부를 전달하게 하였다.

주요 이슈 및 해결 :

에너미 컴포넌트에서의 에너미 이동 처리와, Unity 자체의 중력/마찰 시스템 사이에 충돌이 발생하여 에너미가 계속 정지하는 문제가 발생했다. 따라서 에너미의 위치를 일정 시간마다 위쪽 방향으로 조금씩 이동시켜줬고, 지형 타일맵의 Collider material에서 마찰을 제거하였으며, 에너미가 바닥에 붙어있는 경우에만 중력을 적용하였더니 해결되었다.

<h3>월드 디자인 및 제작</h3>

![image](https://github.com/user-attachments/assets/9b6b485a-05c8-4097-9402-7027bf23311f)

![image](https://github.com/user-attachments/assets/1d96046c-0dd2-4576-9b86-d51ff254d3c2)
![image](https://github.com/user-attachments/assets/6dc4bebc-2ed6-4752-b954-30d0f8dcd560)
![image](https://github.com/user-attachments/assets/b94e4e4b-6c3e-44ca-9d62-f05f9d5293ab)

이번 데모 버전에 포함된 1월드(사막 월드)를 디자인하고 제작하였다. 에너미 룸/보상 룸/이벤트 룸 각 타입 당 8개/3개/4개의 룸을 제작하였다. 각 룸의 지형, 배경 요소 디자인, 에너미 스폰 위치 및 등장 종류 지정을 통해 플레이어가 다양한 룸 구조를 경험하며 재미를 느낄 수 있게 하였다. 또한, 보상 룸과 이벤트 룸에서 등장할 이벤트들을 구상하고 구현하였다.

주요 이슈 및 해결 :

룸의 구조가 비슷하게 반복되면, 플레이어가 지루함을 느낄 것이라는 생각이 들었다. 따라서 Y축과 관련된 요소(사다리, 언덕) 등을 많이 사용하였고, 등장하는 에너미의 종류를 룸의 구조에 따라 다채롭게 지정하였다.

<h3>GameManager 제작 - 싱글톤 패턴 적용</h3>

![image](https://github.com/user-attachments/assets/752774b6-7d92-46b8-8553-f878dd6299a9)

객체지향적 설계를 통해 제작한 각 Manager 컴포넌트들의 접근을 처리하며 게임 실행 중 씬의 변경과 관련 없이 유지되어야 하는 데이터를 보존하기 위해, 싱글톤 패턴을 적용한 GameManager 컴포넌트를 정의하였다. 이를 통해 컴포넌트 간 복잡한 연결 구조 없이 각 Manager 컴포넌트에 접근할 수 있게 하였다. 또한, 장착한 장비, 해킹 등의 주요 요소들을 중앙에서 관리할 수 있게 하였다.

주요 이슈 및 해결 :

GameManager는 씬이 처음 실행될 때(Awake() 함수) 자신의 인스턴스를 전역적으로 선언하는데, 다른 컴포넌트에서도 씬이 처음 실행될 때 GameManager에 접근하여 특정한 처리를 해야하는 경우가 있었다. 이 경우 인스턴스에 접근하는 것을 실패하여 오류가 발생하였다. 이러한 구조적 문제를 해결하기 위해, GameManager가 내부적으로 초기 처리를 마친 후에 다른 컴포넌트들에 대해 각각 Initialize 처리를 해주는 방식으로 개선하였다.

<h3>PoolManager 제작 - 오브젝트 풀링 구현</h3>

![image](https://github.com/user-attachments/assets/20153cc3-92e6-4399-82f6-8ea1e3686145)

Unity의 기본적인 오브젝트 생성/제거 방식을 사용하면, 투사체와 같은 다수의 오브젝트를 생성/제거해야 하는 경우 overhead가 발생한다. 따라서 오브젝트 풀링을 적용한 PoolManager 컴포넌트를 정의하였다. PoolManager에서는 오브젝트를 제거해야 할 때, 실제로 제거하지 않고 비활성화 처리를 한다. 이후 오브젝트를 새로 생성해야 할 때, 해당 오브젝트와 같은 종류의 비활성화된 오브젝트를 가져와서 활성화하고 재사용한다. 이를 플레이어/에너미의 공격 투사체 생성에 적용하여 효율성을 향상시켰다.

<h3>Parallax background 적용</h3>

![image](https://github.com/user-attachments/assets/8192ffb6-2bdf-4c15-8212-8f4b3db54742)

게임의 배경을 여러 개의 분할된 이미지 레이어로 제작하여, 배경 이미지 위치가 플레이어의 이동에 따라 변화하는 정도를 각 레이어마다 다르게 하였다. 멀리 있는 배경은 느리게, 가까이 있는 배경은 빠르게 움직이게 하여 배경의 입체감과 생동감을 주었다.

<h3>상호작용(이벤트) 시스템 구현</h3>

![image](https://github.com/user-attachments/assets/03ec6242-1369-4b96-8955-3750f4b222af)

![image](https://github.com/user-attachments/assets/ed0fa7ee-aab5-4e5c-b2bd-905c205876ba)

상호작용 시스템을 구현하였다. 상호작용 가능한 요소들에 공통으로 적용되는 IInteractable 인터페이스를 정의하고, 각 요소에 적용하였다. 플레이어는 이 인터페이스가 적용된 요소들에 대해 F키를 눌러 상호작용할 수 있게 구현하였다. 보상 룸과 이벤트 룸에서 공통적으로 사용되는 이벤트 또한 이를 통해 구현하였다. 탐사 기지에서의 월드 선택 UI, 장비 강화 UI, 탐사에서의 이벤트 UI 등 다양한 UI들이 상호작용을 통해 출력될 수 있게 하였다.

<h3>탐사 기지 씬 제작 / 시스템 구현</h3>

![ExploreBase](https://github.com/user-attachments/assets/136daef7-5b21-40c8-9d27-96e552512218)

탐사 기지 씬을 제작하고 시스템을 구현하여, 다른 팀원들이 구현한 인벤토리 시스템/장비 강화 시스템을 플레이어가 탐사 전에 사용할 수 있게 구현하였다. 또한 탐사 기지에서 ‘월드 탐색률’과 ‘악성코드 추적도’를 확인할 수 있게 하였으며, 월드 선택 및 탐사 시작을 구현하였다. 또한 ‘월드 탐색률’ 및 ‘악성코드 추적도’에 따른 게임 클리어 및 게임오버를 구현하였다.

주요 이슈 및 해결 : 

탐사 기지 씬과 탐사 씬간의 이동 시에 GameManager와 다른 Manager 컴포넌트들의 연결 관계가 사라져, 게임 시스템에 버그가 발생하는 문제가 생겼다. 싱글톤 패턴을 적용한 GameManager만 씬 이동시에 유지되고, 다른 컴포넌트들은 제거된 뒤 새 씬에서 새로 생성되는 것이 원인이였다. 따라서 씬 이동 시에 각 Manager 컴포넌트들이 자체적으로 GameManager에 자신을 등록하게 하는 방식으로 문제를 해결하였다.

<h3>ScreenUI, WorldUI (Manager) 제작 – UI 구현 및 관리</h3>

![image](https://github.com/user-attachments/assets/9ab9dd50-08ab-44f2-9332-53b9b4f5a71e)
![image](https://github.com/user-attachments/assets/88ce0b61-36e7-4474-ab06-1f9446513842)

ScreenUI, WorldUI 컴포넌트를 정의하여, Screen Space-Overlay UI 및 World Space UI의 관리를 처리하였다. 게임 내에서 사용되는 무기/스킬/체력/월드 선택/룸 선택/일시정지/설정 등 UI를 구현하였고, 룸/씬 이동 간 부드러운 화면 전환을 위하여 코루틴을 이용한 페이드인/페이드아웃 효과를 적용하였다. 이를 적용하기 위해 UI의 visibility의 활성화/비활성화 처리 또한 구현하였다.

주요 이슈 및 해결 :

초기 UI 구조에서는 UI 오브젝트 자체를 활성화/비활성화하는 방식으로 visibility를 설정하였는데, 비활성화하니 해당 오브젝트의 다른 컴포넌트에 접근하는 때에 문제가 발생하였다. 이를 해결하기 위해, 기존 활성화/비활성화 방식을 각 UI 오브젝트에 CanvasGroup 컴포넌트를 추가하여 UI의 투명도 값을 조정하는 방식으로 변경하였다.

<h3>SaveSystem, SaveData 제작 - 세이브/로드 시스템 및 세이브 데이터 저장 구조 구현</h3>

![image](https://github.com/user-attachments/assets/38174cc4-c7dc-48b6-94df-414cd67c1192)
![image](https://github.com/user-attachments/assets/9744197b-9332-41b9-a56d-a20c04e2bd8e)

static 클래스인 SaveSystem를 정의하여 씬의 종류와 관계없이 작동하는 세이브/로드 시스템을 구현하였다. 저장 데이터를 구성하는 SaveData 클래스를 정의하였고, 이를 System.Serializable로 선언하여 클래스 인스턴스 자체가 Json 파일 형식으로 상호 전환될 수 있게 하였다. SaveData에서는 월드 탐색률/악성코드 추적도/보유 자원/장착 무기/장착 해킹 데이터를 저장하게 하였다. SaveSystem에서는 GameManager에서 저장이 필요한 데이터를 가져와서 SaveData의 인스턴스에 저장하고, 이 인스턴스를 Json string 형태로 변환한 뒤 이를 로컬 드라이브에 저장하게 하였다. 또한 저장 데이터의 로드가 필요한 경우 해당 파일을 다시 읽어와서 SaveData의 인스턴스에 읽어온 데이터들을 저장하고, 이를 GameManager에 넘겨줘서 GameManager가 필요한 데이터를 직접 가져갈 수 있게 구현하였다. (보유 무기, 장신구, 장비 강화 수치 등의 데이터 저장은 다른 팀원이 추가적으로 구현)

주요 이슈 및 해결 :

게임의 기존 데이터 구조에서는 장착 무기, 해킹 데이터를 Scriptable Object로 관리하였는데, SaveData에 Scriptable Object가 포함될 시 데이터의 직렬화가 올바르게 되지 않는 문제가 발생하였다. 원인은 Unity 내부에서 Scriptable Object를 처리하는 구조에 있었다. Unity에서는 Scriptable Object로 사전에 정의한 데이터를, 게임 실행시 인스턴스로 생성하여 게임 실행동안 유지한다. 따라서 이렇게 생성된 인스턴스를 SaveData에 포함하여 저장하면 임시 인스턴스 ID가 저장되었고, 게임 재실행 후 데이터를 로드하려고 하면 현재 존재하는 Scriptable Object의 인스턴스의 ID와 SaveData에 포함된 인스턴스의 ID가 일치하지 않아 로드에 실패하였다. 이러한 문제를 해결하기 위해 Scriptable Object를 직접 저장하지 않고 무기, 해킹 ID를 대신 저장하였으며, 구조적인 데이터를 저장해야 하는 경우 일반 클래스를 선언해서 사용하는 방식으로 대체하였다.

<h3>일시정지, 설정 시스템 및 UI 구현</h3>

![image](https://github.com/user-attachments/assets/6a345298-225a-4b10-abc7-4389c089ffed)
![image](https://github.com/user-attachments/assets/b6f0096a-aed7-44ee-8e64-ea7d0780437b)

게임 중 ESC 키를 눌러 게임을 일시 정지하고, 게임 저장/설정/탐사 포기(탐사 중일시)/게임 종료를 선택할 수 있게 구현하였다. 또한 설정 UI에서 배경음/효과음의 소리 크기를 각각 지정하고 저장할 수 있게 구현하였다.

주요 이슈 및 해결 :

처음에 게임의 Time.timescale(시간의 진행 속도를 지정하는 Unity의 변수, 0 <= value <= 1)을 0으로 변경하는 방식으로 일시정지를 구현하였는데, 이에 따라 동적으로 나타낸 UI(좌우로 펼쳐지는 애니메이션이 포함된 UI)의 코루틴 처리에서도 동작이 멈춰버리는 문제가 발생하였다. 따라서 timescale에 영향을 받아야 하는 대상과 그렇지 않은 대상을 구분하고, 그렇지 않은 대상에서는 Time.unscaledDeltaTime과 WaitForSecondsRealTime을 사용하여 Time.timescale에 영향을 받지 않고 실제 시간에 따라 작동할 수 있게 설정하여 해결하였다.

<h3>타이틀 씬 제작</h3>

![Title](https://github.com/user-attachments/assets/ec21f8d0-281b-49b2-8210-beb5bb24f0f6)

게임의 타이틀 씬을 제작하여, 새로운 게임을 시작하거나 SaveSystem을 통해 기존 저장 데이터를 로드하여 이전 게임을 이어서 할 수 있게 하였다. 또한 앞에서 구현한 설정 시스템 또한 사용할 수 있게 했다.

<h3>튜토리얼 씬 제작</h3>

![image](https://github.com/user-attachments/assets/20b912f0-4a7e-4e09-9788-ada5f994e72b)

게임의 튜토리얼 씬을 제작하였다. 최초 시작시 플레이어에게 게임의 배경 스토리를 설명하고, 조작 키에 대한 설명과 실제로 해당 키를 사용해야 하는 상황을 부여하여 플레이어가 게임의 기초 조작과 규칙을 쉽게 이해할 수 있게 하였다.

<h3>SoundManager 제작 - 사운드 관리 및 재생 / 에너미 사운드 적용</h3>

![image](https://github.com/user-attachments/assets/a3742ca2-8bdd-4ec9-8afc-956d93a571ff)

SoundManager 컴포넌트를 정의하여 사운드 종류별로 분류하여 관리하고, 재생할 수 있게 구현하였다. 기본이 되는 AudioMixer의 하위 그룹으로 BGM(배경음) 그룹과 SFX(효과음) 그룹을 두고, 기존에 플레이어가 설정 시스템에서 지정한 소리 크기로 각 그룹의 소리 크기를 지정한 뒤 각 사운드를 재생할 수 있게 하였다. 이 구조를 통해 팀원들이 동일한 사운드 재생 방식을 적용하게 하며 게임의 모든 사운드를 관리하였다.
또한 SoundManager를 이용하여 에너미 사운드/플레이어 피격 사운드/이벤트 사운드를 적용하였다. 에너미 피격/사망 시의 사운드는 공통으로 적용하였고, 에너미 종류별 인지/공격 상황에 대한 사운드를 적용하였다. 이벤트 사운드로는 긍정/부정적 이벤트 발생 시의 사운드를 각각 적용하였다. 이를 통해 플레이어가 더욱 생동감 있는 플레이 경험을 가질 수 있게 했다.

<h3>구현 내용 병합 및 버그 수정</h3>

팀원들이 각자 구현한 파트를 하나의 씬으로 합치고, 그 과정에서 발생하는 버그 수정을 담당하여 처리하였다.

주요 이슈 및 해결 :

구현한 기능 간 호환이 되지 않는 부분에 의해 생기는 버그의 발생 원인을 파악하고 수정하기 위해 다른 팀원들이 구현한 기능의 개별적으로 어떻게 작동하는지, 어떻게 기능끼리 연동되는지를 이해해야 했다. 따라서 회의를 진행할 때 팀원들이 매주 구현한 기능을 파악하고 어떻게 작동하는지 물어보며 지속해서 전체 구조에 대한 이해도를 쌓았다.

<h3>게임 업로드 및 베타 테스트 피드백 설문 진행</h3>

![스토브스토어](https://github.com/user-attachments/assets/506dc19d-9666-4b5e-956d-f4332c3c92f8)
![잇치](https://github.com/user-attachments/assets/7b02c5e8-edbd-4dfe-af66-75313101413f)

![설문](https://github.com/user-attachments/assets/157dabd7-4159-4800-a1f1-935b6508e0ff)

완성한 데모 버전 게임을 스마일게이트 STOVE 스토어, Itch.io 두 개의 인디 게임 플랫폼에 업로드하였다. 또한 베타 테스트 설문을 제작하여 게임 실행 파일과 함께 전달하였고, 이를 통해 플레이어 피드백을 수집하였다.
