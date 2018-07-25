## step 1

### 요구사항
* iOS 프로젝트 Single View App 템플릿으로 하고 프로젝트 이름을 "CardGameApp"으로 지정하고, 위에 만든 로컬 저장소 경로에 생성한다.
* 기본 상태로 아이폰 8 Plus 시뮬레이터를 골라서 실행한다.
* readme.md 파일을 자신의 프로젝트에 대한 설명으로 변경한다.
	* 단계별로 미션을 해결하고 리뷰를 받고나면 readme.md 파일에 주요 작업 내용(바뀐 화면 이미지, 핵심 기능 설명)과 완성 날짜시간을 기록한다.
	* 실행한 화면을 캡처해서 readme.md 파일에 포함한다.

### 프로그래밍 요구사항
* 앱 기본 설정을 지정해서 StatusBar 스타일을 LightContent로 보이도록 한다.
* ViewController 클래스에서 self.view 배경을 다음 이미지 패턴으로 지정한다. 이미지 파일은 Assets에 추가한다.
* 다음 카드 뒷면 이미지를 다운로드해서 프로젝트 Assets.xcassets에 추가한다.
* ViewController 클래스에서 코드로 아래 출력 화면처럼 화면을 균등하게 7등분해서 7개 UIImageView를 추가하고 카드 뒷면을 보여준다.
* 카드 가로와 세로 비율은 1:1.27로 지정한다.

![step1](images/step1.png)

### 학습꺼리
* 화면 크기에 따라 코드로 View를 생성하고 화면에 추가하는 방식을 학습한다.
* 앱 기본 설정(Info.plist)을 변경하는 방식에 대해 학습한다.


## step 2
### 프로그래밍 요구사항
* 레벨2 CardGame 미션의 Main, InputView, OutputView를 제외하고 전체 클래스를 프로젝트로 복사한다.
* 기존 코드들은 MVC 중에서 대부분 Model의 역할을 담당한다.
* 다음 링크에서 카드 이미지를 다운로드 받아서 Assets에 추가한다. 파일이름을 바꾸지말고 그대로 활용한다.

`https://www.dropbox.com/s/5xbznqbjfq3tn7v/card_decks.zip?dl=0`

* Card 객체에 파일명을 매치해서 해당 카드 이미지를 return 하는 메소드를 추가한다.

* Card 객체가 앞면, 뒷면을 처리할 수 있도록 개선한다.
* CardDeck 인스턴스를 만들고 랜덤으로 카드를 섞고 출력 화면처럼 보이도록 개선한다.
* 화면 위쪽에 빈 공간을 표시하는 UIView를 4개 추가하고, 우측 상단에 UIImageView를 추가한다.
	* 상단 화면 요소의 y 좌표는 20pt를 기준으로 한다.
	* 7장의 카드 이미지 y 좌표는 100pt를 기준으로 한다.
* 앱에서 Shake 이벤트를 발생하면 랜덤 카드를 다시 섞고 다시 그리도록 구현한다.

![step2](images/step2.gif)

### 학습꺼리
* Assets 으로 이미지를 관리하는 방법에 대해 학습한다.
* 디바이스 종류에 따라 화면 크기에 대한 처리를 학습한다. [관련 자료](https://www.paintcodeapp.com/news/ultimate-guide-to-iphone-resolutions)