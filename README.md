# X-process-work-schedule

### 조건 설명
- 근무방식 : 
- 조건1 : 근무는 총 4개 타임으로 0612시, 1218시, 1800시, 00~6시 4개의 타임으로 하루 근무가 돌아감. 
- 조건2 : 각 근무 1개 타임별로 2명씩 짝지어서 두팀으로 한 타임에 총 4명이 근무에 투입됨.
- 조건4 : '매칭되지 않을 특수관계자'칸에 '이름-이름' 형식으로 입력할시 서로 매칭되지않음.
- 조건5 : '특별사유 열외자'칸에 '이름' 형식으로 입력할시 근무 열외자로 따로 구분하고, 구분은 쉼표로 함.
- 조건6 : 하루에 총 4개의 근무타임이 존재하게 되는데, 한명이 하루에 근무를 1번이상 들어가면 안됨.
- 조건7 : 휴가자가 있는 경우 그 사람을 제외하고 근무공정시스템이 작동해야하므로, 휴가자를 입력할 수 있어야함. 입력 형식은 '이름-휴가기간'으로 함.
- 특이조건 : 1800시 근무 후 다음날 0006시, 012시 근무 불가. 0006시 근무후 근무취침으로 인해 다음날 0612시, 1218시 근무 불가.
- 제시 되어 있는 모든 사람이 모두 공평하게 한번씩 들어갔다면, 다음번에는 초기화 후 새롭게 또다시 공평하게 한번씩 들어가야함. 
- 근무표를 엑셀로 저장할 수 있어야하며, 각각의 사람별로 근무 횟수가 표기되어야함.
- 사용코드 HTML, Javascript 
- 코드를 실행시킬 수 있는 환경이 메모장과 크롬뿐이라  html코드와 자바스크립트 코드가 따로 구분되어 있는 형식이 아닌, 두개가 하나의 코드에 합쳐지도록 짜야함. 즉, html파일과 script.js파일이 따로따로 분류되어있으면 안됨.
- 사용 가능한 사람 이름 : 1소대-장현호, 김동환, 홍정빈, 변준규, 김진수1, 장민교, 김종훈, 윤예성, 김정한, 송수영, 이정안, 박지한 / 2소대-이세진, 김효준, 김형민, 박세준, 이정욱, 성시우, 장혜민, 한창윤, 손재훈, 서민수, 김진수2 / 3소대-허진솔, 정 준, 김민규, 홍원기, 박준서, 정민수, 정현욱, 안태균, 주성찬 / 포반본부-유동규, 반정호, 신호섭, 유태종, 황승민, 김현묵, 김민수, 김성민, 윤세종, 김영호


## 테스트 결과
- Ver 1.1 : 세부 조건에 부합하는 코드를 포함시키지 않았기때문에 기초모델이 되는 코드
- Ver 1.2 : 세부 조건에 부합하는 코드를 포함하였지만 일부 공정성 문제와 몇몇 인원이 난수 내에서 누락되는 경우 발생
- Ver 1.3 : 1.2버전과는 다른 형식의 모델링을 했지만 작동안됨.
- Ver 1.4 : 1.3버전 기반 수정본. 작동안됨. 개발자도구-콘솔에 오류 표기조차 안됨.
- Ver 1.5 : save함수에서 tavle요소의 rows속성을 읽을때 오류 발생. (table요소가 공백인 경우에 발생됨. 즉, table요소가 아직 생성되지 않았거나, 이미 제거된 상태로 추측)
- Ver 1.6 : rewult요소의 첫번째 자식 요소인 table요소를 참조하나, generate함수를 호출하여 근무표를 생성하기 전에 save함수를 호출하면, table요소가 아직 생성되지 않았으므로 공백발생.
- Ver 1.7 : save함수 호출이전에 generate함수를 먼저 호출하는 것을 보장하기 위해 save함수에서 table요소의 존재를 확인하는 코드를 추가함. 작동됨.
- Ver 1.8 : 하루에 2번 근무. 0006이후에 0612근무 경우 발생.

업데이트 날짜 | Ver. | 작동여부 | 콘솔 오류코드 | 발생문제
| :---: | --- | --- | --- | :---: |
23.09.09 | Main | Broken Camera <br> Crack Camera | Strat Project. | A3
23.09.11 | Serve | Readme.md | MCT-A | WS / TC1
23.10.17 | Main | Broken Camera | BCF-M | WS / TC2
23.10.17 | Main | Broken Camera | BCF-M | WS / TC1,2
23.10.18 | Main | Crack Camera | RCF-M | WS / TC1
23.10.18 | Main | Broken Camera | BCF-F | WS / TC1,2
23.10.18 | Main | Crack Camera | RCF-F | WS
23.10.19 | Simul. | 1 - Beta Test | KAMASF AndroidOS BetaTest 1.0 : Fale | WS
23.10.19 | Simul. | 2 - Beta Test | KAMASF AndroidOS BetaTest 1.1 : Fale | WS
23.10.19 | Simul. | 3 - Beta Test | KAMASF AndroidOS BetaTest 1.2 : Succ | WS
23.10.19 | Simul. | 4 - Beta Test | KAMASF AndroidOS BetaTest 1.3 : Fale | WS
23.10.19 | Simul. | 5 - Beta Test | KAMASF AndroidOS BetaTest 1.4 : Succ | WS
23.10.19 | Simul. | 6 - Beta Test | KAMASF AndroidOS BetaTest 1.5 : Succ | WS
23.10.20 | Simul. | 7 - Beta Test | KAMASF AndroidOS BetaTest 1.4 : Succ | WS
23.10.19 | Simul. | 1 - Alpha Test | KAMASF AndroidOS AlphaTest 2.0 : Succ | WS
23.10.19 | Serve | Readme.md <br> PRIVACY_POLICY.md | MCT-A <br> PRIV.-A | WS
23.11.06 | BUGFIX | 1 - Release | 
