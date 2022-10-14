# Events

Motion 이외에 디바이스에 줄 수 있는 다양한 이벤트들이 모여 있습니다. 예를 들어 세로 화면을 가로 화면으로 바꾸거나  앱 실행 혹은 종료 시키는 등의 이벤트를 발생 시킬 수 있습니다.

### Rotate

디바이스의 스크린 방향을 변경할 수 있습니다.(시계방향 270도로 회전)

#### Rotate Attributes

1. orientation: 회전 방향을 지정합니다.\
   \- PORTRAIT: 디바이스의 화면을 세로 방향으로 회전합니다.\
   \- LANDSCAPE: 디바이스의 화면을 가로 방향으로 회전합니다.

### Wait

다음 스텝을 실행할 때까지 설정한 시간만큼 대기합니다.

#### Wait Attributes

1. value: 대기 시간을 설정할 수 있습니다.\
   \- 기본값: 2000\
   \- 최소값: 500\
   \- 최대값: 5000\
   \- 단위: ms

### Launch

앱을 실행합니다.

#### Launch Attributes

1. Package Name: 실행할 앱이 안드로이드 앱일 경우 앱의 Package Name을 입력합니다.
2. Bundle ID: 실행할 앱이 아이폰 앱일 경우 앱의 Bundle ID를 입력합니다.

두 값 모두 입력했을 경우 테스트가 실행되는 디바이스의 종류에 따라 사용될 값이 정해집니다.

{% hint style="info" %}
안드로이드 Package Name 알아내는 방법

Step1. play.google.com에 접속해서 앱을 검색합니다.

Step2. 상단 주소창 부분에서 패키지 이름을 확인합니다. <mark style="color:red;">**?id=패키지이름**</mark> 형식으로 되어 있습니다.
{% endhint %}

{% hint style="info" %}
아이폰 Bundle ID 알아내는 방법

Step1. apple.com/kr/app-store에 접속해서 앱을 검색합니다.

Step2. 상단 주소창 부분에서 고유번호를 확인합니다. <mark style="color:red;">**/id고유번호**</mark> 형식으로 되어 있습니다.

Step3. 아래 형식의 주소를 브라우저에 입력합니다.

&#x20;           https://itunes.apple.com/lookup?id=공유번호

Step4. txt 형태로 다운로드 된 파일을 열어서 Bundle ID 값을 확인합니다.&#x20;
{% endhint %}

### Terminate

실행중인 앱을 종료합니다.

#### Terminate Attributes

1. Package Name: 실행할 앱이 안드로이드 앱일 경우 앱의 Package Name을 입력합니다.
2. Bundle ID: 실행할 앱이 아이폰 앱일 경우 앱의 Bundle ID를 입력합니다.

두 값 모두 입력했을 경우 테스트가 실행되는 디바이스의 종류에 따라 사용될 값이 정해집니다.

### Activate

백그라운드에서 실행 중인 앱을 디바이스 화면에 띄웁니다.

#### Activate Attributes

1. Package Name: 실행할 앱이 안드로이드 앱일 경우 앱의 Package Name을 입력합니다.
2. Bundle ID: 실행할 앱이 아이폰 앱일 경우 앱의 Bundle ID를 입력합니다.

두 값 모두 입력했을 경우 테스트가 실행되는 디바이스의 종류에 따라 사용될 값이 정해집니다.

### Home

디바이스의 홈 화면으로 이동합니다. (홈 버튼 누르는 것과 동일 동작)

### Lock

디바이스를 잠금 상태로 변경합니다.

### Unlock

디바이스를 잠금 해제 합니다.

### Wake Up

장치가 슬립 상태일 때 슬립 모드를 해제합니다.

### Keycode

다양한 Keycode값을 입력할 수 있습니다. 기본으로 제공되는 Keycode 이외의 값을 Keycode를 직접 입력할 수 있습니다.

_<mark style="color:red;">주의) Keycode 액션은 안드로이드 전용 액션입니다. 아이폰에서는 동작하지 않고 바로 다음 스텝으로 넘어갑니다.</mark>_

#### Keycode Attributes

1. value: 입력할 Keycode값을 설정합니다. 직접 입력할 수도 있고, 클릭하면 나오는 기본 값을 선택할 수 도 있습니다.\
   \- Back(4): 안드로이드 Back 버튼 동작을 수행합니다.\
   \- Enter(66): 키보드 UI의 Go 버튼 동작을 수행합니다.\
   \- Del(67): 키보드 UI의 백스페이스 동작을 수행합니다.\
   \- AppSwitch(187): 안드로이드 앱전환 버튼 동작을 수행합니다.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption><p>Keycode Attributes 예제 </p></figcaption></figure>

