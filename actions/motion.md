# Motion

스마트폰을 실제로 조작할 때 사용되는 동작들을 모아둔 곳입니다.

### Touch

화면 요소를 터치하는 동작입니다. 스텝을 만들 때 가장 많이 사용되는 액션이며, 스텝을 새로 만들때도 액션의 기본값으로 설정되어 있습니다.

#### Touch Attributes&#x20;

1. UIObject: 터치 액션을 수행할 화면 요소가 출력됩니다.&#x20;

<figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption><p>터치 액션 Attributes 예제</p></figcaption></figure>



### NTimes Touch

화면 요소를 설정한 횟수만큼 터치하는 액션입니다.

#### NTimes Touch Attributes&#x20;

1. UIObject: 여러번 터치 액션을 수행할 화면 요소가 출력됩니다.
2. count: 액션을 수행할 횟수를 설정할 수 있습니다.\
   \- 기본값: 2\
   \- 최소값: 1\
   \- 최대값: 100
3. interval: 액션과 액션 사이에 얼마의 시간동안 쉴지를 설정할 수 있습니다.\
   \- 최소값: 500\
   \- 최대값: 5000\
   \- 단위: ms

<figure><img src="../.gitbook/assets/image (110).png" alt=""><figcaption><p>여러번 터치 액션 Attributes 예제</p></figcaption></figure>



### Double Touch

화면 요소를 두번 터치하는 액션입니다.

#### Double Touch Attributes&#x20;

1. UIObject: 두번 터치를 수행할 화면 요소가 출력됩니다.

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption><p>두번 터치 액션 Attributes 예제</p></figcaption></figure>



### Long Touch

화면 요소를 길게 터치하는 액션입니다.

#### Long Touch Attributes

1. UIObject: 길게 터치를 수행할 화면 요소가 출력됩니다.
2. duration: 터치를 얼마나 오래 유지할지 설정할 수 있습니다.\
   \- 최소값: 1000\
   \- 최대값: 5000\
   \- 단위: ms

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption><p>길게 터치 액션 Attributes 예제</p></figcaption></figure>



### Swipe

스와이프할 수 있는 UIObject를 대상으로 좌우로 스와이프하는 액션입니다.

#### Swipe Attributes&#x20;

1. area: 스와이프가 수행될 영역의 비율입니다. 수치가 작을 수록 적은 면적을 스와이프합니다.\
   \- 기본값: 60\
   \- 최소값: 1\
   \- 최대값: 100\
   \- 단위: %
2. UIObject: 스와이프를 수행하는 화면 요소가 출력됩니다.
3. direction: 스와이프를 왼쪽으로 할지, 오른쪽으로 할지 설정할 수 있습니다.\
   \- 기본값: LEFT
4. duration: 스와이프가 수행되는 시간을 나타냅니다.\
   \- 최소값: 500\
   \- 최대값: 5000\
   \- 단위: ms

<figure><img src="../.gitbook/assets/image (182).png" alt=""><figcaption><p>스와이프 액션 Attributes 예제</p></figcaption></figure>



### Scroll

상하로 스크롤할 수 있는 화면 요소을 대상으로 스크롤하는 액션입니다. 전체 화면을 스크롤 할 때는 UIObject Selector 패널에서 Full Screen Strategy를 사용해 화면 요소를 생성한 스텝에 등록하면 됩니다.

#### Scroll Attributes&#x20;

1. area: 스크롤 액션을 수행할 영역의 비율을 설정할 수 있습니다.\
   \- 기본값: 60\
   \- 최소값: 1\
   \- 최대값: 100\
   \- 단위: %
2. UIObject: 스크롤을 수행하는 화면 요소가 출력됩니다.
3. direction: 스크롤을 위로 할지, 아래로 할지 설정할 수 있습니다.\
   \- 기본값: UP
4. duration: 스크롤 액션을 수행하는 시간을 설정할 수 있습니다.\
   \- 기본값: 2500\
   \- 최소값: 500\
   \- 최대값: 5000\
   \- 단위: ms

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption><p>스크롤 액션 Attributes 에제</p></figcaption></figure>



### Drag

드래그 할 수 있는 두 개의 화면 요소를 필요로 합니다. 첫번째 화면 요소에서 두번째 화면 요소로 드래그 합니다.

주로 날짜나 시간을 설정하는 화면에서 주로 사용되는 액션입니다.

<figure><img src="../.gitbook/assets/image (63).png" alt=""><figcaption><p>드래그  액션 예제</p></figcaption></figure>

#### Drag Attributes&#x20;

1. start UIObject: 드래그 액션을 시작하는 기준이 되는 화면 요소입니다.
2. end UIObject: 드래그 액션을 끝내는 기준이 되는 화면 요소입니다.
3. press duration: 드래그 액션을 시작하기 전에 오래 누르기를 먼저해야할 경우 설정할 수 있습니다.\
   바탕화면의 아이콘을 오래 눌어서 옮길 수 있게 한다음 다른 위치로 옮기는 동작을 구현할 수 있습니다.\
   \- 기본값: 0\
   \- 최소값: 0\
   \- 최대값: 5000\
   \- 단위: ms
4. duration: 드래그 액션이 수행되는데 걸리는 시간을 설정할 수 있습니다.\
   \- 기본값: 2500\
   \- 최소값: 500\
   \- 최대값: 5000\
   \- 단위: ms

<figure><img src="../.gitbook/assets/image (76).png" alt=""><figcaption><p>드래그 액션 Attributes 예제</p></figcaption></figure>

### Pinch In / Pinch Out

Zoom in, Zoom out 액션을 수행합니다.

#### Pinch In / Pinch Out Attributes&#x20;

1. area: Pinch In/Out이 수행될 영역의 비율입니다.\
   \- 기본값: 60\
   \- 최소값: 50\
   \- 최대값: 100\
   \- 단위: %
2. UIObject: Pinch In/Out을 수행하는 화면 요소가 출력됩니다.
3. duration: 액션을 수행하는데 걸리는 시간을 설정할 수 있습니다.\
   \- 기본값: 2500\
   \- 최소값: 1000\
   \- 최대값: 5000\
   \- 단위: ms

<figure><img src="../.gitbook/assets/image (74).png" alt=""><figcaption><p>핀치 인/아웃 액션 Attributes 예제</p></figcaption></figure>

### Input

키보드로 특정 값을 입력하고자 할 때 사용합니다. 앱화면에 키보드가 활성화 된 상태에서 전체 화면을 UIObject로 설정하고 입력할 값을 Attributes 패널의 value 필드에 입력하세요.

<figure><img src="../.gitbook/assets/image (92).png" alt=""><figcaption><p>입력 액션 적성 예제</p></figcaption></figure>

#### Input Attributes&#x20;

1. value: 입력 필드에 입력될 문자열을 설정합니다.
2. UIObject: 문자열이 입력될 화면 요소를 나타냅니다. 만약 화면에 키보드가 활성화 되어 있을 경우에는 화면 전체를  UIObject로 설정하면 현재 활성화 되어 있는 입력 필드에 값이 입력됩니다.

<figure><img src="../.gitbook/assets/image (203).png" alt=""><figcaption><p>입력 Attributes 예제</p></figcaption></figure>

### Secure Keyboard

화면에 띄워진 보안키보드에 Attributes에서 설정한 입력값을 입력합니다. \
_<mark style="color:red;">주의) 보안키보드가 켜진 상태의 Full Screen Strategy를 사용해야 합니다.</mark>_

#### Secure Keyboard Attributes&#x20;

1. value: 보안키보드에 입력할 값입니다.
2. UIObject: Secure Keyboard를 수행하는 UIObject 입니다.&#x20;
3. typename: Secure Keyboard의 종류입니다. (자동으로 입력됩니다.)
4. interval: 키 입력 사이에 유휴시간을 설정할 수 있습니다.\
   \- 기본값: 1000\
   \- 최소값: 500\
   \- 최대값: 5000\
   \- 단위: ms

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption><p>보안 키보드 Attributes 예제 </p></figcaption></figure>

