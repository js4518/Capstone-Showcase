## 캡스톤디자인I / 사이버펑크+디스토피아 로그라이트 액션 게임 개발

<img src="https://github.com/user-attachments/assets/2ecc832f-2e67-4414-80a4-abcab8d6ef33" width="75%">

<img src="https://github.com/user-attachments/assets/298eccf7-b442-477a-b031-0730cba74608" width="65%">


**📆 진행 기간:** 2025.03 ~ 2025.06  

**📘 위키:** [캡크래프트 프로젝트 위키](http://cscp2.sogang.ac.kr/CSE4186/index.php/%EC%BA%A1%ED%81%AC%EB%9E%98%ED%94%84%ED%8A%B8)  

**🕹️ STOVE 스토어:** [https://store.onstove.com/ko/games/101515](https://store.onstove.com/ko/games/101515)  

**▶️ 전체 플레이 영상:** [https://youtu.be/UVl7yaMmQIA?si=dm9YSfIsRDznCu49](https://youtu.be/UVl7yaMmQIA?si=dm9YSfIsRDznCu49)

## 🔷 개발 목표

본 프로젝트는 사이버펑크 디스토피아 세계관을 배경으로, 플레이어가 **탐사 로봇을 조작하여 월드를 반복 탐사**하고 진실에 접근해나가는 **2D 로그라이트 액션** 게임을 개발하는 것을 목표로 한다.

플레이어는 탐사기지의 주인공으로서, 탐사 로봇을 원격 조종해 각 월드를 탐사하고, 탐색률 100% 달성을 목표로 하며, **반복적인 플레이 속에서 무기와 스킬, 능력치를 점진적으로 강화**해 나가야 한다.

## 🔷 개발 범위

### 🔹 탐사 기반 스테이지 구조
- 탐사기지 → 월드 반복 탐사 구조 설계  
- 각 월드는 **무작위 룸 단위 맵**으로 구성  
- 탐색률(%)로 진행도 표시, 100% 달성 시 완료

### 🔹 플레이어 성장 시스템
- **장신구 슬롯 시스템**을 통한 무기 강화  
- **부품(재화)** 소비로 영구 능력치 강화  
- 반복 플레이로 점진적 성장 유도

### 🔹 전투 시스템
- 무기 4종 + 각 무기별 스킬 2종  
- 히트스톱, 카메라 셰이크 등 타격감 연출
- 해킹으로 **군중 제어/데미지 보조** 효과

### 🔹 시스템 및 UI
- 이동, 점프, 회피, 공격, 무기 전환 등 기본 액션
- UI : 체력, 스킬, 탐색률 등 표시
- 데이터 저장/로드 기능

### 🔹 데이터 중심 구조 설계
- **ScriptableObject 기반 관리**로 확장성 확보  
  (무기, 스킬, 장신구, 적, 해킹 등)

## 🔷 사용 기술 스택

| 분류 | 내용 |
|------|------|
| **Engine** | Unity 6 (6000.0.43f1) |
| **Version Control** | Git / GitHub |
| **Build Target** | Windows (.exe) -> STOVE 스토어 및 itch.io 배포 |
| **협업 툴** | Trello, Discord |

## 🔷 프로젝트 세부사항

### 🔹 역할 분담

|이름	|개발 측면|	프로젝트 관리 측면|
|------|---|---|
|**송종서**|	**에너미, 룸 시스템, 탐사 기지 시스템 등 설계/구현, 월드 디자인 및 제작**|	**팀장, 일정/위키 관리**|
|김*림|	플레이어 행동, 무기 및 스킬 시스템, 장신구 시스템, 보스 패턴 설계/구현|깃허브 관리|
|최*혁|	해킹 시스템, 보스 시스템 설계/구현, 타이틀 디자인|발표, 멘토 컨택|
|이*은|	자원, 인벤토리, 장비 강화, 상점 시스템 등 설계/구현, 애니메이션 적용|회의 관리|

## 🔷 담당 파트

### 🔹 RoomManager

<img src="https://github.com/user-attachments/assets/67c96f93-aac0-4d80-88e4-098ac0edb883">

<img src="https://github.com/user-attachments/assets/a5d04a4f-f496-4978-bdb5-98f14e53c7bb">
<img src="https://github.com/user-attachments/assets/6816eb3d-b77b-4aa2-b6c6-aa2e9088d256">

<img src="https://github.com/user-attachments/assets/96116942-7703-41fc-bd38-b06782f90142" width="60%">

- **룸 프리팹 구조 설계** (**Prefab Variant**를 이용한 다중 상속 구조)  
- **룸 이동, 포탈, 선택 시스템 및 UI 구현**  
- 룸 타입 : Enemy / Reward / Event  

### 🔹 EnemyManager

<img src="https://github.com/user-attachments/assets/079e1fc8-e08a-49e8-9dde-9a5716dec923" width="30%">
<img src="https://github.com/user-attachments/assets/572bbaf9-b658-479d-abc1-f8d78777c35d" width="50%">

<img src="https://github.com/user-attachments/assets/1f827d01-b3c4-4c18-94a2-c268fa498b3a">

- **ScriptableObject 기반 에너미 데이터 구조화**  
- **에너미 패턴 구현** (돌진, 점프, 자폭, 은신형 원거리)  
- **스폰 처리를 위한 EnemyManager 구현** / 룸 클리어 조건 연동

### 🔹 GameManager (Singleton)

<img src="https://github.com/user-attachments/assets/752774b6-7d92-46b8-8553-f878dd6299a9" width="30%">

- **전역 데이터 및 매니저 통합 관리**  
- 씬 로드시의 초기화 순서 제어로 의존성 문제 해결

### 🔹 PoolManager

<img src="https://github.com/user-attachments/assets/20153cc3-92e6-4399-82f6-8ea1e3686145" width="30%">

- **투사체, 이펙트 풀링 구조 구현**  
- 오브젝트 재활용으로 성능 개선

### 🔹 UI Manager

<img src="https://github.com/user-attachments/assets/9ab9dd50-08ab-44f2-9332-53b9b4f5a71e" width="30%">
<img src="https://github.com/user-attachments/assets/88ce0b61-36e7-4474-ab06-1f9446513842" width="30%">

- **ScreenUI, WorldUI 관리 구조 구현**
- CanvasGroup을 통한 페이드 효과 구현 -> 룸/씬 이동 간 부드러운 화면 전환

### 🔹 UI

<img src="https://github.com/user-attachments/assets/6a345298-225a-4b10-abc7-4389c089ffed" width="60%">
<img src="https://github.com/user-attachments/assets/b6f0096a-aed7-44ee-8e64-ea7d0780437b" width="35%">

- **일시 정지, 설정 시스템 및 UI 구현**
- Time.unscaledDeltaTime 및 WaitForSecondsRealTime의 사용으로, Time.timescale 조정에 따른 UI 정지 문제 해결  
- BGM/SFX 볼륨 개별 조절 및 저장 기능 구현

### 🔹 SaveSystem, SaveData

<img src="https://github.com/user-attachments/assets/38174cc4-c7dc-48b6-94df-414cd67c1192" width="50%">
<img src="https://github.com/user-attachments/assets/9744197b-9332-41b9-a56d-a20c04e2bd8e" width="50%">

- **JSON 직렬화 기반 게임 저장/로드 구현**  
- Scriptable Object 인스턴스를 직접 저장하지 않고, ID를 기반으로 데이터를 저장하여 오류 해결 

### 🔹 SoundManager

<img src="https://github.com/user-attachments/assets/a3742ca2-8bdd-4ec9-8afc-956d93a571ff" width="50%">

- **AudioMixer 그룹(BGM/SFX)을 분리한 구조로 사운드 시스템 구현**
- 에너미, 이벤트 관련 사운드 적용

### 🔹 이벤트 상호작용 시스템

<img src="https://github.com/user-attachments/assets/ed0fa7ee-aab5-4e5c-b2bd-905c205876ba" width="60%">
<img src="https://github.com/user-attachments/assets/03ec6242-1369-4b96-8955-3750f4b222af" width="25%">

- `IInteractable` 인터페이스 설계  
- NPC, 오브젝트, 이벤트 등 상호작용이 필요한 대상에 공통 적용

### 🔹 탐사 기지 시스템

<img src="https://github.com/user-attachments/assets/136daef7-5b21-40c8-9d27-96e552512218" width="60%">

- **탐사 이전에 플레이어가 월드 선택, 강화, 자원 확인 등을 수행할 수 있게 구현**
- 씬 이동시 GameManager(싱글톤)과 다른 매니저 컴포넌트(싱글톤 X) 간 연결 구조 재설정 구현

### 🔹 월드 디자인 및 제작

<img src="https://github.com/user-attachments/assets/9b6b485a-05c8-4097-9402-7027bf23311f" width="60%">

- **1월드 제작** (Enemy/Reward/Event 룸 15개 제작)  
- Y축 구조 및 적 조합 다양화
