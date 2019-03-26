﻿# LostArkPad

### ** 로스트 아크의 불법 프로그램 사용을 지양합니다. 개발진 측에서 이 프로그램을 불법 프로그램으로 판단할 경우 메일로 연락주시면 프로그램을 삭제하도록 하겠습니다. (* 이 프로그램은 편의 기능 외에 밸런스에 영향을 주는 매크로 기능은 추가하지 않습니다.)

## ◈ 목적
- 키보드 신호를 XBox360 컨트롤러 신호로 에뮬레이션 해주는 프로그램.
- [마우스 모드] 로스트 아크의 기본 조작 체계를 따라가면서 편의 기능을 추가한 모드.
- [패드 모드] 정교한 전투를 위해 캐릭터 이동을 키보드의 WASD키로 하고 스킬을 마우스로 사용하는 모드.

## ◈ 사용 라이브러리
1. Interception
   - Site : https://github.com/oblitum/Interception
   - 키보드, 마우스 신호를 받기 위한 라이브러리.
2. ScpVBus
   - Site : https://github.com/nefarius/ScpVBus, https://github.com/shauleiz/vXboxInterface
   - XBox360 컨트롤러 신호를 발생시키기 위한 에뮬레이터.

## ◈ 설치 순서
1. 아래 링크에서 최신 버전을 다운로드한다.
   - https://github.com/artgramsoft/LostArkPad/releases
2. Interception 드라이버 설치
   - Install\Interception\install.bat 파일을 관리자 권한으로 실행한다.
3. ScpVBus 드라이버 설치
   - Install\ScpVBus\install.bat 파일을 관리자 권한으로 실행한다.
4. 재부팅한다.
5. LostArkPad.exe로 프로그램 실행.
   - 처음 실행시 XBox 360 가상 드라이버를 설치하는데, 패드 모드에서 WASD키로 캐릭터가 움직이지 않을 경우, 한번 더 재부팅을 한다.

## ◈ 기 능
### ※ [ 모드 공용 ] 
```
▶ 마우스 모드와 패드 모드에 상관없이 항상 사용가능한 단축키.
```
|기능           |기본 단축키   |변경 가능|설정 항목     |설명                                 |
|:---           |:---         |:---:   |:---         |:---                                 |
|모드 전환      |CapsLock      |O       |change_mode  |마우스 모드와 패드 모드 사이를 전환.   |
|스크롤 업      |Home          |O       |wheel_up     |휠 스크롤 업 기능.                    |
|스크롤 다운    |End           |O       |wheel_down   |휠 스크롤 다운 기능.                  |
|디바이스 선택  |Alt + S       |X       |             |키보드 마우스 다시 선택.               |
|프로그램 토글  |Alt + Z       |O       |pause        |LostArkPad 일시 정지.                 |
|프로그램 종료  |Alt + Q       |X       |             |LostArkPad 종료.                     |
    
### ※ [ 마우스 모드 ]
```
▶ 기본 컨트롤 방식을 최대한 유지하면서 편의 기능을 추가한 모드.
```
|기능           |기본 단축키        |변경 가능|설정 항목     |설명                                 |
|:---           |:---              |:---:   |:---         |:---                                 |
|키보드 패드    |화살표 키          |O       |pad           |키보드로 캐릭터 이동.                 |
|              |                  |O       |- type        |ARROW 또는 WASD (기본값 ARROW)        |
|              |                  |O       |- skill_dir   |스킬이 나가는 방향 설정 (기본값 PAD)   |
|              |                  |O       |- move_mouse  |패드 사용시 마우스 이동 (기본값 true)  |
|              |                  |O       |- move_length |마우스 이동 거리 (기본값 300 pixel)    |
|              |                  |O       |- trans_length |마우스 이동 거리 2 (기본값 500 pixel)    |
|              |                  |O       |- trans_key_code |마우스 이동 거리 2 조작 키 (기본값 Shift) |
|자동 달리기    |더블 클릭          |X       |run           |마우스 따라 이동.                    |
|              |                  |        |- use         |true: 사용, false: 사용 안함.        |
|              |                  |        |- delay       |더블 클릭 인식 시간(ms)               |
|직선 달리기    |트리플 클릭        |X       |run           |인게임에서 T키 기능. (On/Off 가능.)   |
|대쉬          |이동 중 Wheel Down |X       |              |인게임에서 Space키 기능.              |
|상호 작용      |Wheel Down        |O       |act           |인게임에서 G키 기능.                  |
|말타기         |Wheel Up          |O       |ride          |인게임에서 F3키 기능.                 |
|물약 먹기      |Shift + Wheel Up  |O       |potion        |인게임에서 F1키 기능.                 |
|배틀 아이템 1  |Shift + Wheel Down|O       |battle_1      |인게임에서 1키 기능.                  |
|배틀 아이템 2  |2                 |O       |battle_2      |인게임에서 2키 기능.                  |
|배틀 아이템 3  |3                 |O       |battle_3      |인게임에서 3키 기능.                  |
|배틀 아이템 4  |4                 |O       |battle_4      |인게임에서 4키 기능.                  |
|스크롤 업      |Attack + Wheel Up |X       |              |마우스 공격 버튼 클릭상태에서 스크롤.  |
|스크롤 다운    |Attack + Wheel Down|X      |              |마우스 공격 버튼 클릭상태에서 스크롤.  |
|제스처 스킬    |아래 항목 참조     |X       |gesture_skill |제스처로 스킬 사용.                   |
|              |                  |        |- use         |true: 사용, false: 사용 안함.         |
|              |                  |        |- drag_length |드래그 인식 거리(pixel)               |
|              |                  |        |- time_out    |드래그 인식 시간(ms)                  |
|제스처 액션    |아래 항목 참조     |O       |gesture_action|제스처로 단축키 사용.                 |
|              |                  |        |- use         |true: 사용, false: 사용 안함.         |
|              |                  |        |- drag_length |드래그 인식 거리(pixel)               |
|              |                  |        |- time_out    |드래그 인식 시간(ms)                  |
|              |                  |        |- up          |↑ 드래그 변환 키코드: 60(F2)          |
|              |                  |        |- down        |↓ 드래그 변환 키코드: 48(B)           |
|              |                  |        |- left        |← 드래그 변환 키코드: 1(ESC)          |
|              |                  |        |- right       |→ 드래그 변환 키코드: 15(TAB)         |
|제스처 액션 2  |아래 항목 참조     |O       |gesture_action|제스처로 단축키 사용.                 |
|              |                  |        |- use         |true: 사용, false: 사용 안함.         |
|              |                  |        |- drag_length |드래그 인식 거리(pixel)               |
|              |                  |        |- time_out    |드래그 인식 시간(ms)                  |
|              |                  |        |- up          |↑ 드래그 변환 키코드: 21(Y)          |
|              |                  |        |- down        |↓ 드래그 변환 키코드: 22(U)           |
|              |                  |        |- left        |← 드래그 변환 키코드: 23(I)          |
|              |                  |        |- right       |→ 드래그 변환 키코드: 50(M)         |
|스킬 Q        |Q                 |O       |skill_q       |인게임에서 Q키 기능.                  |
|스킬 W        |W                 |O       |skill_w       |인게임에서 W키 기능.                  |
|스킬 E        |E                 |O       |skill_e       |인게임에서 E키 기능.                  |
|스킬 R        |R                 |O       |skill_r       |인게임에서 R키 기능.                  |
|스킬 A        |A                 |O       |skill_a       |인게임에서 A키 기능.                  |
|스킬 S        |S                 |O       |skill_s       |인게임에서 S키 기능.                  |
|스킬 D        |D                 |O       |skill_d       |인게임에서 D키 기능.                  |
|스킬 F        |F                 |O       |skill_f       |인게임에서 F키 기능.                  |
|스킬 Z        |Z                 |O       |skill_z       |인게임에서 Z키 기능.                  |
|스킬 X        |X                 |O       |skill_x       |인게임에서 X키 기능.                  |
|스킬 V        |V                 |O       |skill_v       |인게임에서 V키 기능.                  |
> ### 키보드 패드 ▶ 키보드 신호를 XBox360 조이스틱 신호로 변경해주는 기능.
> 
> * type은 ARROW 또는 WASD로 설정할 수 있다.
> * skill_dir은 MOUSE 또는 PAD로 설정할 수 있다.  
> (* PAD: 패드 방향으로 스킬을 사용한다.)  
> (* MOUSE: 마우스 방향으로 스킬을 사용한다.)
> * move_mouse의 값이 true이면, 패드 사용시 마우스가 패드 방향으로 같이 이동한다.
> * move_mouse의 값이 true일 경우, 이동하는 마우스의 기본 거리는 move_length 이며, trans_key를 누르면 trans_length 만큼 이동한다.
> * `*** move_mouse 기능은 LostArkPad를 관리자 권한으로 실행해야만 작동한다.***`
>  
> ### 제스처 기능 ▶ 귀차니즘을 위한 기능으로 한손으로 키보드 없이 마우스를 이용해 스킬과 단축키를 사용할 수 있다.
>
> #### # 제스처 스킬
> |스킬|드래그 방향|드래그 길이|제한 시간|사용 방법|
> |:---:|:---:|:---:|:---:|:---|
> |Q|←|70px|0.1초|이동 키를 클릭한 상태에서 드래그.|
> |W|↑|70px|0.1초|이동 키를 클릭한 상태에서 드래그.|
> |E|↓|70px|0.1초|이동 키를 클릭한 상태에서 드래그.|
> |R|→|70px|0.1초|이동 키를 클릭한 상태에서 드래그.|
> |A|←|70px|0.1초|이동 키와 공격 키를 모두 클릭한 상태에서 드래그.|
> |S|↑|70px|0.1초|이동 키와 공격 키를 모두 클릭한 상태에서 드래그.|
> |D|↓|70px|0.1초|이동 키와 공격 키를 모두 클릭한 상태에서 드래그.|
> |F|→|70px|0.1초|이동 키와 공격 키를 모두 클릭한 상태에서 드래그.|
>
> #### # 제스처 액션
> |기본 단축키|드래그 방향|드래그 길이|제한 시간|사용 방법|
> |:---|:---:|:---:|:---:|:---|
> |ESC (취소)|←|50px|0.2초|마우스 가운데 버튼을 클릭한 상태에서 드래그.|
> |F2 (연주)|↑|50px|0.2초|마우스 가운데 버튼을 클릭한 상태에서 드래그.|
> |B (Hud변경)|↓|50px|0.2초|마우스 가운데 버튼을 클릭한 상태에서 드래그.|
> |TAB (미니맵)|→|50px|0.2초|마우스 가운데 버튼을 클릭한 상태에서 드래그.|
>
> #### # 제스처 액션 2
> |기본 단축키|드래그 방향|드래그 길이|제한 시간|사용 방법|
> |:---|:---:|:---:|:---:|:---|
> |I (인벤토리)|←|50px|0.2초|마우스 뒤로 가기 버튼을 클릭한 상태에서 드래그.|
> |Y (감정표현)|↑|50px|0.2초|마우스 뒤로 가기 버튼을 클릭한 상태에서 드래그.|
> |U (친구)|↓|50px|0.2초|마우스 뒤로 가기 버튼을 클릭한 상태에서 드래그.|
> |M (월드맵)|→|50px|0.2초|마우스 뒤로 가기 버튼을 클릭한 상태에서 드래그.|

### ※ [ 패드 모드 ]
```
▶ 키보드로 캐릭터를 움직이고 마우스로 스킬을 사용하기 위한 모드. (전투에 특화된 모드)
```
|기능           |기본 단축키       |변경 가능|설정 항목  |설명                                   |
|:---           |:---             |:---:   |:---      |:---                                   |
|키보드 패드    |WASD 키           |O       |pad              |키보드로 캐릭터 이동.                 |
|              |                  |O       |- type           |ARROW 또는 WASD (기본값 WASD)        |
|              |                  |O       |- skill_dir      |스킬이 나가는 방향 설정 (기본값 MOUSE)   |
|              |                  |O       |- move_mouse     |패드 사용시 마우스 이동 (기본값 false)  |
|              |                  |O       |- move_length    |마우스 이동 거리 (기본값 300 pixel)    |
|              |                  |O       |- trans_length   |마우스 이동 거리 2 (기본값 500 pixel)    |
|              |                  |O       |- trans_key_code |마우스 이동 거리 2 조작 키 (기본값 Shift) |
|마우스 기능    |Alt + Mouse      |X       |           |마우스 클릭 & 우클릭에 사용.            |
|자동 달리기    |Q                |O       |run        |이동키를 누르면 캔슬.                   |
|상호 작용      |E                |O       |act        |인게임에서 G키 기능.                    |
|말타기         |R                |O       |ride       |인게임에서 F3키 기능.                   |
|물약 먹기      |F                |O       |potion     |인게임에서 F1키 기능.                   |
|기본 공격      |MButton          |O       |attack     |인게임에서 C키 기능.                    |
|공격 캔슬      |아래 항목 참조    |O       |attack_cancel|설정에서 On/Off 가능.                 |
|스킬 Q        |LButton           |O       |skill_q    |인게임에서 Q키 기능.                    |
|스킬 W        |Wheel Up          |O       |skill_w    |인게임에서 W키 기능.                    |
|스킬 E        |Wheel Down        |O       |skill_e    |인게임에서 E키 기능.                    |
|스킬 R        |RButton           |O       |skill_r    |인게임에서 R키 기능.                    |
|스킬 A        |Shift + LButton   |O       |skill_a    |인게임에서 A키 기능.                    |
|스킬 S        |Shift + Wheel Up  |O       |skill_s    |인게임에서 S키 기능.                    |
|스킬 D        |Shift + Wheel Down|O       |skill_d    |인게임에서 D키 기능.                    |
|스킬 F        |Shift + RButton   |O       |skill_f    |인게임에서 F키 기능.                    |
|스킬 Z        |XButton1(뒤로가기) |O       |skill_z    |인게임에서 Z키 기능.                    |
|스킬 X        |Shift + XButton1  |O       |skill_x    |인게임에서 X키 기능.                    |
|스킬 V        |Shift + MButton   |O       |skill_v    |인게임에서 V키 기능.                    |
> ### 키보드 패드 ▶ 키보드 신호를 XBox360 조이스틱 신호로 변경해주는 기능. (설명은 마우스 모드 참조.)
> 
> ### 공격 캔슬 기능 ▶ 기본 공격을 이동키로 캔슬하여 조금 더 빠르게 사용하기 위한 기능.
> 
> * 공격 캔슬 기능을 끄려면 설정 파일의 attack_cancel 항목의 값을 0으로 설정한다.
> * 사용 방법은 기본 공격키(MButton, 마우스 가운데 버튼)를 누르고 있으면 된다.
> * 값이 1000일 경우, 마우스 방향으로 이동하면서 1초에 한번씩 기본 공격을 자동 수행한다.
> * 설정 파일에 있는 기본값 430은 아르카나에 최적화된 수치이다.
> * 캐릭터마다 가장 빠르게 기본 공격을 할 수 있는 수치는 모두 다르므로 자기 직업에 맞게 값을 변경하여 적용해야 한다.

## ◈ 설정 파일 작성법.
### ※ 단축키 항목 설명. (* 단축키를 사용하지 않을때는 code값을 0으로 설정한다.)
|항목|사용 가능한 값|설명|
|:---|:---|:---|
|type|"K" 또는 "M"|단축키 타입: "K"이면 키보드, "M"이면 마우스|
|code|숫자|단축키 지정(예, type이 "K"일때 code가 16이면, 키보드 Q키를 의미)|
|state|숫자|단축키 상태(예, type이 "K"일때 code가 16이고 state가 0이면, 키보드 Q키를 눌렀을 때라는 의미)|
|alt|true 또는 false|Alt 조합키와 함께 눌러야 하는지 여부.|
|ctrl|true 또는 false|Ctrl 조합키와 함께 눌러야 하는지 여부.|
|shift|true 또는 false|Shift 조합키와 함께 눌러야 하는지 여부.|
|block|true 또는 false|단축키 신호를 게임으로도 보낼것인지 지정.|

### ※ 단축키 code 및 state 값 구하기.
1. InterceptorKeyCode.exe 파일을 실행한다.
2. 단축키로 사용하려는 키를 누른다.
3. 화면상에 나오는 Code값과 State값을 기억한다. 
4. 설정파일에서 변경하기 원하는 단축키의 code와 state값을 위의 값으로 설정한다.

### ※ 키보드 예제.
|예제 1|설명|예제 2|설명|
|:---|:---|:---|:---|
|키보드 Q키를 눌렀다 떼었을 때.||키보드 Alt + J키를 눌렀을 때.||
|"type": "K",|키보드|"type": "K",|키보드|
|"code": 16,|Q키|"code": 36,|J키|
|"state": 1,|눌렀다 떼었을 때|"state": 0,|눌렀을때|
|"alt": false,||"alt": true,|Alt 조합|
|"ctrl": false,||"ctrl": false,||
|"shift": false,||"shift": false,||
|"block": true|신호 차단|"block": false|신호 통과(에포나 의뢰창 열림)|

### ※ 마우스 예제. (마우스는 code에 state까지 포함되어 있다.(휠 스크롤 예외))
|예제 1|설명|예제 2|설명|
|:---|:---|:---|:---|
|마우스 휠 버튼을 눌렀을 때.||마우스 휠 버튼을 눌렀다 떼었을 때.||
|"type": "M",|마우스|"type": "M",|마우스|
|"code": 16,|휠 버튼 눌렀을 때|"code": 32,|휠 버튼 눌렀다 떼었을 때|
|"state": 0,||"state": 0,||
|"alt": false,||"alt": false,||
|"ctrl": false,||"ctrl": false,||
|"shift": false,||"shift": false,||
|"block": true|신호 차단|"block": true|신호 차단|

## ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) 주의 사항
> ### # 마우스 기능 사용.
> * 온전한 마우스 기능 사용을 위해서는 일시 정지(Alt + Z) 기능을 사용하도록 권장한다.
> * 패드 모드는 마우스 기능에 불편함이 많으므로 전투 외에서는 마우스 모드로 변경하여 사용을 권장한다.

> ### # 패드 모드 사용 중 캐릭터 끼임 현상.
> * 캐릭터가 오브젝트나 몬스터와 겹칠 경우 움직이지 못하는 끼임 현상이 종종 발생한다. 
> * 해당 버그는 물리적인 XBox360 컨트롤러를 사용할때도 동일하게 발생하는 LostArk의 물리엔진 버그이다.
> * 이를 벗어나기 위해서는 마우스 이동 기능인 Q 버튼 또는 Alt + 마우스 클릭으로 이동해야만 한다.

## ◈ 연락처
- 문의 사항이 있을 경우, 메일(aurabunny@uzoo.in)로 연락주세요.
- 디스코드 서버를 개설했습니다. 여러분들의 의견을 남겨 주세요.
  (https://discord.gg/WcRQzK)

## ◈ 라이센스
- This software is licensed under CC-BY-NC-ND license. © 2018 aurabunny contributors
- 이 프로그램은 개인에게만 무료로 제공이 되며, 상업적 또는 영리적 이용은 제한됩니다.