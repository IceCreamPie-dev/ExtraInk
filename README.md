# ExtraInk 유니티 이야기 게임 템플릿
이야기 게임을 텍스트 만으로 쉽게 만들 수 있도록.
[ExtraInk 문서](https://icecreampie-dev.github.io/ExtraInk/)

### 스크립트 예시
```C#
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

// === Variables ===
VAR player_name = "Player"

// === Main Story ===
# TITLE: 새 스토리
# AUTHOR: 
-> 시발점
== 시발점

~ 캐릭터_표시("염서", "기본", "오른쪽", "기본")
~ 캐릭터_표시("염서서", "기본", "왼쪽", "기본")
염서: 안녕하세요! 

~ 캐릭터_이동("염서", "왼쪽")
염서: 저는 염서라고 해요. #감정: 화남
염서가 나타났다...

~ 캐릭터_플립("염서")
염서: ......
~ 캐릭터_플립("염서")
염서: ......
~ 캐릭터_이동("염서", "중앙")
~ 캐릭터_플립("염서")
염서: ......
나: .....

* [계속하기] -> continue
* [종료하기] -> ending

== continue ==
여기에 스토리 내용을 작성하세요.
-> END

== ending ==
스토리가 끝났습니다. 읽어주셔서 감사합니다!
-> END
```
