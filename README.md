# ExtraInk 유니티 이야기 게임 템플릿
이야기 게임을 텍스트 만으로 쉽게 만들 수 있도록.
[ExtraInk 문서](https://icecreampie-dev.github.io/ExtraInk/)
Inkle의 Ink에 비주얼 게임에 사용할 수 있도록 래핑한 패키지 입니다.

# 기능
- 자체 DB(소리, 캐릭터, 이미지, ink관리)
- 스프라이트 캐릭터와 애니메이터 캐릭터를 지원합니다.
- ink EXTERNAL 함수와 TAG를 활용해 비 개발자도 쉽게 스토리 작성

### 스크립트 예시
```C#
// === Variables ===
VAR player_name = "레티샤"

// === External Functions ===
// 외부 기능
// 사용법 예시: ~ 캐릭터_표시(파이, 기본, 오른쪽, 기본)
EXTERNAL 캐릭터_표시(이름, 감정, 위치, 효과)
EXTERNAL 캐릭터_숨김(이름, 효과)
EXTERNAL 캐릭터_이동(이름, 위치)
EXTERNAL 캐릭터_플립(이름)
EXTERNAL 감정_변경(이름, 감정)
EXTERNAL 스킨_변경(이름, 스킨)
EXTERNAL 순서_설정(이름, 순서)
EXTERNAL 형제_인덱스_설정(이름, 인덱스)

EXTERNAL 대사(이름, 텍스트)

EXTERNAL 텍스트_애니메이션(타입)
EXTERNAL 텍스트_속도(속도)
EXTERNAL 텍스트_페이드_속도(속도)

EXTERNAL 소리(이름)

EXTERNAL 배경_표시(이름, 효과)
EXTERNAL 배경_숨김(이름, 효과)
EXTERNAL 배경_변경(이름, 효과)
EXTERNAL 팝업_표시(이름, 효과)
EXTERNAL 팝업_숨김(이름, 효과)

// === Main Story ===
# TITLE: 전투튜토리얼
# AUTHOR: 

~ 소리("펑키치킨") 
<>
~ 캐릭터_표시("레티샤","기본", "왼쪽", "기본") 
<>
{player_name}: <바운스>길을 잃었다.</바운스>
레티샤: <바운스>길을 잃었다.</바운스>

// 선택지 예시
* 와 센즈! -> 센즈
* 와 파피루스 -> 파피루스

== 센즈
레티샤: <>센즈는 여기 있었다.

-> END

== 파피루스
레티샤: 파피루스를 찾았다.

-> END

~캐릭터_숨김("레티샤", "기본")
<>
-> END

```

[이전 프로젝트](https://github.com/IceCreamPie-dev/Univ_ShootMaster_summ)
