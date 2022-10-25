# Control

시나리오에 분기점이 필요하거나 동일 스텝들을 반복해야 할 때 사용할 수 있는 기능들이 있습니다.\


### If UIObject

설정한 UIObject가 화면 상에 존재하는지를 판단해서 자식 스텝을 실행합니다.

<figure><img src="../.gitbook/assets/image (157).png" alt=""><figcaption><p>부모 스텝과 자식 스텝 예제</p></figcaption></figure>

#### If UIObject Attributes&#x20;

1. UIObject: 화면에 존재하는지 확인하는데 사용될 화면 요소가 출력됩니다.
2. comparator:  비교 조건을 선택할 수 있습니다.\
   \- EXISTS: 화면에 화면 요소가 존재한다면 자식 스텝을 실행합니다.\
   \- NOT EXISTS: 화면에 화면 요소가 존재하지 않는다면 자식 스텝을 실행합니다.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption><p>If UIObject Attributes 예제 </p></figcaption></figure>

### If Content

UIObject 자체보다 UIObject의 실제 내용을 비교 대상으로 사용할 경우 쓰입니다. UIObject의 Text 정보를 OCR로 읽어 들여 Text 정보끼리 비교를 합니다.

If UIObject는 화면 요소 자체를 비교 대상으로 사용하는 반면, If Content는 화면 요소 자체 보다는 그 안에 포함되어 있는 Text 정보를 비교 대상으로 사용한다는 차이점이 있습니다.

<figure><img src="../.gitbook/assets/image (93).png" alt=""><figcaption><p>If Content 예제</p></figcaption></figure>

#### If Content Attributes&#x20;

1. UIObject: 비교할 Text를 포함하고 있는 화면 요소가 출력됩니다.
2. comparator: 비교 조건을 선택할 수 있습니다.\
   \- = : 화면 요소의 Text와 value가 똑같다면 자식 스텝을 실행합니다.\
   \- != : 화면 요소의 Text와 value가 다르면 자식 스텝을 실행합니다.\
   \- > : 화면 요소의 Text가 숫자이고 value 보다 크면 자식 스텝을 실행합니다.\
   \- >= : 화면 요소의 Text가 숫자이고 value 보다 크거나 같으면 자식 스텝을 실행합니다.\
   \- < : 화면 요소의 Text가 숫자이고 value 보다 작으면 자식 스텝을 실행합니다.\
   \- <= : 화면 요소의 Text가 숫자이고 value 보다 작거나 같으면 자식 스텝을 실행합니다.\
   \- match: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식과 일치하면 자식 스텝을 실행합니다.\
   &#x20; 참고자료: [https://docs.python.org/3/library/re.html#re.match](https://docs.python.org/3/library/re.html#re.match)\
   \- search: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식을 포함하면 자식 스텝을 실행합니다. \
   &#x20; 참고자료: [https://docs.python.org/3/library/re.html#re.search](https://docs.python.org/3/library/re.html#re.search)

<figure><img src="../.gitbook/assets/image (75).png" alt=""><figcaption><p>If Content Attributes 예제 </p></figcaption></figure>

### If Value

Store Value/Content 또는 Random Number/Text 액션을 통해 저장된 값을 비교 대상으로 사용할 때 사용하는 액션입니다. 그래서 별도의 UIObject를 설정할 필요가 없습니다.

자세한 사용법은 예제6. 조건문 액션 사용하기를 참고하세요.

{% content-ref url="../tutorial/5..md" %}
[5..md](../tutorial/5..md)
{% endcontent-ref %}

#### If Value Attributes&#x20;

1. key: 이전에 Store Value/Content등으로 저장해 두었던 값의 key값을 입력합니다.
2. comparator: 비교 조건을 선택할 수 있습니다.\
   \- = : 화면 요소의 Text와 value가 똑같다면 자식 스텝을 실행합니다.\
   \- != : 화면 요소의 Text와 value가 다르면 자식 스텝을 실행합니다.\
   \- > : 화면 요소의 Text가 숫자이고 value 보다 크면 자식 스텝을 실행합니다.\
   \- >= : 화면 요소의 Text가 숫자이고 value 보다 크거나 같으면 자식 스텝을 실행합니다.\
   \- < : 화면 요소의 Text가 숫자이고 value 보다 작으면 자식 스텝을 실행합니다.\
   \- <= : 화면 요소의 Text가 숫자이고 value 보다 작거나 같으면 자식 스텝을 실행합니다.\
   \- match: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식과 일치하면 자식 스텝을 실행합니다.\
   &#x20; 참고자료: [https://docs.python.org/3/library/re.html#re.match](https://docs.python.org/3/library/re.html#re.match)\
   \- search: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식을 포함하면 자식 스텝을 실행합니다. \
   &#x20; 참고자료: [https://docs.python.org/3/library/re.html#re.search](https://docs.python.org/3/library/re.html#re.search)&#x20;
3. value: 비교할 문자열 또는 숫자를 입력합니다.

<figure><img src="../.gitbook/assets/image (57).png" alt=""><figcaption><p>If Value Attributes 예제 </p></figcaption></figure>

### If Changed

If Changed 액션은 이전 스텝의 액션이 수행되기 직전 화면과 현재 디바이스 화면의 변화 여부를 비교해 조건을 충족할 경우 자식 스텝을 실행합니다.

화면의 특정 위치에 있는 컨텐츠의 내용 변화를 감지 할 수 있기 때문에 토스트 팝업이나 동영상 재생 여부 등을 판단해서 자식 스텝을 선택적으로 실행할 수 있습니다.

예를 들어 동영상이 재생중일 경우 동영상 재생을 중지하는 시나리오를 작성할 수 있습니다.

아래 예제를 참고하세요.

{% content-ref url="../tutorial/6..md" %}
[6..md](../tutorial/6..md)
{% endcontent-ref %}

#### If Changed Attributes&#x20;

1. UIObject: 화면 변화를 감지할 공간 요소가 출력됩니다.
2. threshold: 화면 요소가 얼만큼 변해야 변한 것으로 판정할지 수치를 지정할 수 있습니다. 수치가 작을수록 조금만 변해도 화면 요소가 변한것으로 간주합니다.\
   \- 기본값: 10\
   \- 최소값: 1\
   \- 최대값: 100\
   \- 단위: %
3. limit: 화면 변화를 언제까지 감지할지 한계를 설정할 수 있습니다. 설정시간 동안 화면 변화가 없다면 자식 스텝들은 실행되지 않고 다음 스텝으로 넘어갑니다.\
   \- 기본값: 5000\
   \- 최소값: 3000\
   \- 최대값: 10000\
   \- 단위: ms

### Loop UIObject

화면에 특정 화면 요소가 존재하는지 여부에 따라 자식 스텝을 반복하는 액션입니다.

가장 흔한 사용 예로, 리스트형 UI에서 원하는 컨텐츠가 나올때까지 스크롤을 반복해야 하는 경우을 시나리오로 작성할 때 주로 사용됩니다.

아래 예제를 참고하세요.

{% content-ref url="../tutorial/2..md" %}
[2..md](../tutorial/2..md)
{% endcontent-ref %}

#### Loop UIObject Attributes&#x20;

1. UIObject: 존재 여부 판단에 사용될 화면 요소가 출력됩니다.
2. comparator: 판단 기준을 선택합니다.\
   \- EXISTS: 화면 요소가 존재하면 자식 스텝을 반복 수행합니다.\
   \- NOT EXISTS: 화면 요소가 존재하지 않으면 자식 스텝을 반복 수행합니다.
3. limit: 자식 스텝의 최대 반복 횟수를 설정할 수 있습니다.\
   \- 기본값: 5\
   \- 최소값: 1\
   \- 최대값: 1000\
   \- 단위: 횟수

<figure><img src="../.gitbook/assets/image (194).png" alt=""><figcaption><p>Loop UIObject Attributes 예제 </p></figcaption></figure>

### Loop Ntimes

동일한 스텝을 여러번 반복해야 할 때 사용하면 좋은 액션입니다.

이 액션은 자식 스텝을 정해진 횟수만큼 반복 실행합니다.

<figure><img src="../.gitbook/assets/image (106).png" alt=""><figcaption><p>Play store에서 추천앱 상세보기 후 뒤로가기, 스와이프로 다음 앱으로 이동하는 과정을 Loop Ntimes로 반복하는 시나리오 예제</p></figcaption></figure>

#### Loop Ntimes Attributes

1. limit: 반복 횟수를 지정할 수 있습니다.\
   \- 기본값: 5\
   \- 최소값: 1\
   \- 최대값: 1000\
   \- 단위: 횟수

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>Loop Ntimes Attributes 예제</p></figcaption></figure>

### Loop Content

반복을 위한 조건이 횟수 이외에 한 가지가 더 추가된 액션입니다. 화면상의 특정 위치에 있는 문자를 읽어 작성자가 지정한 값과 비교해서 반복 여부를 판단합니다.

자세한 사용법은 아래 예제를 확인하세요.

{% content-ref url="../tutorial/7..md" %}
[7..md](../tutorial/7..md)
{% endcontent-ref %}

#### Loop Content Attributes

1. UIObject: 문자열을 읽어올 화면 요소가 출력됩니다.
2. comparator: 비교 조건을 선택할 수 있습니다.\
   \- = : 화면 요소의 Text와 value가 똑같다면 자식 스텝을 실행합니다.\
   \- != : 화면 요소의 Text와 value가 다르면 자식 스텝을 실행합니다.\
   \- > : 화면 요소의 Text가 숫자이고 value 보다 크면 자식 스텝을 실행합니다.\
   \- >= : 화면 요소의 Text가 숫자이고 value 보다 크거나 같으면 자식 스텝을 실행합니다.\
   \- < : 화면 요소의 Text가 숫자이고 value 보다 작으면 자식 스텝을 실행합니다.\
   \- <= : 화면 요소의 Text가 숫자이고 value 보다 작거나 같으면 자식 스텝을 실행합니다.\
   \- match: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식과 일치하면 자식 스텝을 실행합니다.\
   &#x20; 참고자료: [https://docs.python.org/3/library/re.html#re.match](https://docs.python.org/3/library/re.html#re.match)\
   \- search: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식을 포함하면 자식 스텝을 실행합니다. \
   &#x20; 참고자료: [https://docs.python.org/3/library/re.html#re.search](https://docs.python.org/3/library/re.html#re.search)&#x20;
3. value: 비교할 문자열 또는 숫자를 입력합니다.
4. limit: 반복 횟수를 지정합니다.\
   \- 기본값: 5\
   \- 최소값: 1\
   \- 최대값: 1000\
   \- 단위: 횟수

<figure><img src="../.gitbook/assets/image (86).png" alt=""><figcaption><p>Loop Content Attributes 예제</p></figcaption></figure>

### Loop Value

Store Value/Content 또는 Random Number/Text 로 미리 저장해둔 값과 사용자가 설정한 값을 비교해서 자식 스텝을 실행합니다. 미리 설정한 값을 사용하기 때문에 별도의 화면 요소를 지정할 필요가 없습니다.

이 액션을 이용하면 이전 화면에서 잔여포인트를 읽어서 저장해 두고, 잔여포인트가 특정 수치에 도달할때까지 포인트를 추가하는 스텝을 반복하는 시나리오를 작성 할 수 있습니다.

#### Loop Value Attributes

1. key: 사전에 설정해 둔 값의 key값을 입력합니다.
2. comparator: 비교 조건을 선택할 수 있습니다.\
   \- = : 화면 요소의 Text와 value가 똑같다면 자식 스텝을 실행합니다.\
   \- != : 화면 요소의 Text와 value가 다르면 자식 스텝을 실행합니다.\
   \- > : 화면 요소의 Text가 숫자이고 value 보다 크면 자식 스텝을 실행합니다.\
   \- >= : 화면 요소의 Text가 숫자이고 value 보다 크거나 같으면 자식 스텝을 실행합니다.\
   \- < : 화면 요소의 Text가 숫자이고 value 보다 작으면 자식 스텝을 실행합니다.\
   \- <= : 화면 요소의 Text가 숫자이고 value 보다 작거나 같으면 자식 스텝을 실행합니다.\
   \- match: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식과 일치하면 자식 스텝을 실행합니다.\
   &#x20; 참고자료: [https://docs.python.org/3/library/re.html#re.match](https://docs.python.org/3/library/re.html#re.match)\
   \- search: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식을 포함하면 자식 스텝을 실행합니다. \
   &#x20;  참고자료: [https://docs.python.org/3/library/re.html#re.search](https://docs.python.org/3/library/re.html#re.search)&#x20;
3. value: 비교할 문자열 또는 숫자를 입력합니다.
4. limit: 반복 횟수를 지정합니다.\
   \- 기본값: 5\
   \- 최소값: 1\
   \- 최대값: 1000\
   \- 단위: 횟수

<figure><img src="../.gitbook/assets/image (163).png" alt=""><figcaption><p>Loop Value Attributes 예제</p></figcaption></figure>

### Loop Wait For

설정한 화면 요소가 출력될때까지 기다리는 액션입니다. 로딩 시간이 불규칙적인 경우에 사용하면 테스트 수행 시간을 많이 단축할 수 있습니다.

&#x20;

<figure><img src="../.gitbook/assets/image (70).png" alt=""><figcaption><p>네트워크 속도가 느리거나 저사양 디바이스에서 구글맵을 실행했을 때 Search here라는 문자열이 뜰때까지 대기하는 예제</p></figcaption></figure>

#### Loop Wait For Attributes

1. UIObject: 화면에 출력되기를 기대릴 화면 요소가 출력됩니다.
2. limit: 설정한 시간을 초과할때까지 화면 요소가 출력되지 않으면 대기를 중단하고 다음 스텝을 실행합니다.\
   \- 기본값: 1000\
   \- 최소값: 1000\
   \- 최대값: 60000\
   \- 단위: ms

<figure><img src="../.gitbook/assets/image (122).png" alt=""><figcaption><p>Loop Wait For Attributes 예제</p></figcaption></figure>

