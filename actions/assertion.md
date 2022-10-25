# Assertion

화면상 특정 위치에 요소나 문자열이 있는지 검사할 때 사용하는 기능들입니다. 실제 테스트를 위해 사용되는 스텝 액션으로 여기 있는 액션을 통과하지 못하면 빨간색으로 에러 메시지가 출력되면서 시나리오가 중지 됩니다.

주로 특정 스텝 수행 후 그 스텝이 잘 진행되었는지 확인 하는 과정(예: 로그인 후 환영 메시지가 출력되는지 확인)에서 사용됩니다.

### Assert UIObject

지정한 화면 요소가 화면상에 존재하는지 검사하는 액션입니다.

이전 스텝 실행 후 현재 화면이 제대로 출력 되었는지 판단하고 싶을 때 사용할 수 있습니다.

사용법은 아래 예제를 참고하세요.

{% content-ref url="../tutorial/9..md" %}
[9..md](../tutorial/9..md)
{% endcontent-ref %}

#### Assert UIObject Attributes

1. UIObject: 검사 대상이 될 화면 요소가 출력됩니다.
2. comparator: 비교 조건을 선택할 수 있습니다.\
   _<mark style="color:red;">주의) comparator에서 설정한 조건이 참이어야 검사가 통과해서 다음 스텝으로 넘어갑니다. 만약 comparator 조건이 거짓인 경우에는 custom message가 출력되고, type이 Error인 경우에는 여기서 시나리오가 멈추게 됩니다.</mark>_\
   _<mark style="color:red;"></mark>_- EXISTS: 화면에 화면 요소가 존재한다면 검사가 성공합니다.\
   \- NOT EXISTS: 화면에 화면 요소가 존재하지 않는다면 검사가 성공합니다.
3. custom message: comparator 조건이 거짓일 경우 Output으로 출력할 메시지를 입력할 수 있습니다. 입력하지 않으면 거짓인 이유가 출력됩니다.
4. type: comparator가 거짓인 경우 검사 결과를 Error로 출력할지 Warning으로 출력할지 선택할 수 있습니다.\
   \- ERROR: 조건이 거짓이면 빨간색으로 결과가 출력되며 시나리오가 중단됩니다.\
   \- WARNING: 조건이 거짓이면 노란색으로 결과가 출력되며 다음 스텝이 계속 진행됩니다.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

### Assert Content

지정한 화면 요소의 문자열 내용과 작성자가 입력한 값을 비교하는 검사 액션입니다.

화면 요소 자체의 존재 여부가 비교 대상인 Assert UIObject와는 다르게 화면 요소 안에 있는 문자 정보가 비교 대상이 됩니다.

#### Assert Content Attributes

1. UIObject: 검사 대상이 될 화면 요소가 출력됩니다.
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
3. value: 화면 요소의 문장과 비교할 값을 입력합니다. 만약 이전에 설정해둔 값을 사용할 경우에는 ${key}를 입력합니다.
4. custom message: comparator 조건이 거짓일 경우 Output으로 출력할 메시지를 입력할 수 있습니다. 입력하지 않으면 거짓인 이유가 출력됩니다.
5. type: comparator가 거짓인 경우 검사 결과를 Error로 출력할지 Warning으로 출력할지 선택할 수 있습니다.\
   \- ERROR: 조건이 거짓이면 빨간색으로 결과가 출력되며 시나리오가 중단됩니다.\
   \- WARNING: 조건이 거짓이면 노란색으로 결과가 출력되며 다음 스텝이 계속 진행됩니다.

<figure><img src="../.gitbook/assets/image (152).png" alt=""><figcaption><p>Assert Content Attributes 예제</p></figcaption></figure>

### Assert Value

이전 스텝에서 Store Value/Content 또는 Random Number/Text 등으로 설정해둔 값과 사용자가 지정한 값을 비교 검사하는 액션입니다.&#x20;

이 액션은 사용자가 미리 설정해둔 값을 검사하는 액션이기 때문에 Assert UIObject, Assert Content와 달리 별도의 UIObject를 필요로 하지 않습니다.

#### Assert Value Attributes

1. key: 이전에 설정해둔 값의 key를 입력합니다. \
   _<mark style="color:red;">주의) attributes의 value에 key를 입력할 때 ${key}와 같은 형태로 입력하는 것과 달리 key값 만을 입력해야 합니다.</mark>_
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
3. value: 화면 요소의 문장과 비교할 값을 입력합니다. 만약 이전에 설정해둔 값을 사용할 경우에는 ${key}를 입력합니다.
4. custom message: comparator 조건이 거짓일 경우 Output으로 출력할 메시지를 입력할 수 있습니다. 입력하지 않으면 거짓인 이유가 출력됩니다.
5. type: comparator가 거짓인 경우 검사 결과를 Error로 출력할지 Warning으로 출력할지 선택할 수 있습니다.\
   \- ERROR: 조건이 거짓이면 빨간색으로 결과가 출력되며 시나리오가 중단됩니다.\
   \- WARNING: 조건이 거짓이면 노란색으로 결과가 출력되며 다음 스텝이 계속 진행됩니다.

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption><p>Assert Value Attributes 예제</p></figcaption></figure>

### Assert Changed

Assert Changed는 이전 스텝의 액션이 수행되기 직전의 화면과 현재 디바이스의 화면의 변화 여부를 검사하는 액션입니다.

어떠한 액션 수행 후 특정 화면 요소나 위치의 내용이 변하는지를 검사할 때 사용할 수 있습니다.

주로 자동으로 나타나거나 사라지는 UI나 토글 버튼 변화 감지 시나리오 작성에 사용됩니다.

{% content-ref url="../tutorial/8.-ui.md" %}
[8.-ui.md](../tutorial/8.-ui.md)
{% endcontent-ref %}

#### Assert Changed Attributes

1. UIObject: 화면 변화를 감지할 공간 요소가 출력됩니다.
2. threshold: 화면 요소가 얼만큰 변해야 변한것으로 판정할지 수치를 지정할 수 있습니다. 수치가 작을수록 조금만 변해도 화면 요소가 변한것으로 간주합니다.\
   \- 기본값: 10\
   \- 최소값: 1\
   \- 최대값: 100\
   \- 단위: %
3. limit: 화면 변화를 언제까지 감지할지 한계를 설정할 수 있습니다. 설정시간 동안 화면 변화가 없다면 검사를 실패한 것으로 간주합니다.\
   \- 기본값: 5000\
   \- 최소값: 3000\
   \- 최대값: 10000\
   \- 단위: ms
4. custom message: comparator 조건이 거짓일 경우 Output으로 출력할 메시지를 입력할 수 있습니다. 입력하지 않으면 거짓인 이유가 출력됩니다.
5. type: comparator가 거짓인 경우 검사 결과를 Error로 출력할지 Warning으로 출력할지 선택할 수 있습니다.\
   \- ERROR: 조건이 거짓이면 빨간색으로 결과가 출력되며 시나리오가 중단됩니다.\
   \- WARNING: 조건이 거짓이면 노란색으로 결과가 출력되며 다음 스텝이 계속 진행됩니다.

<figure><img src="../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>

### Assert Wait For

Assert UIObject와 유사하게 지정한 화면 요소가 화면상에 존재하는지를 검사합니다. 다만 화면 요소가 나타날때까지 얼마나 기다릴지 작업자가 선택할 수 있는 옵션이 추가된 점이 다른 점입니다.

주로 화면 로딩 시간이 불규칙적인 경우에 유용하게 사용할 수 있습니다.

#### Assert Wait For Attributes

1. UIObject: 검사 대상이 될 화면 요소가 출력됩니다.
2. limit: 화면 요소가 나타날때까지 얼마나 기다릴지 설정할 수 있습니다.\
   \- 기본값: 1000\
   \- 최소값: 1000\
   \- 최대값: 60000\
   \- 단위: ms
3. custom message: comparator 조건이 거짓일 경우 Output으로 출력할 메시지를 입력할 수 있습니다. 입력하지 않으면 거짓인 이유가 출력됩니다.
4. type: comparator가 거짓인 경우 검사 결과를 Error로 출력할지 Warning으로 출력할지 선택할 수 있습니다.\
   \- ERROR: 조건이 거짓이면 빨간색으로 결과가 출력되며 시나리오가 중단됩니다.\
   \- WARNING: 조건이 거짓이면 노란색으로 결과가 출력되며 다음 스텝이 계속 진행됩니다.

<figure><img src="../.gitbook/assets/image (109).png" alt=""><figcaption><p>Assert Wait For Attributes 예제</p></figcaption></figure>



### Assert Message

특정 액션 이후 토스트 팝업이 잘 뜨는지 검사하는 액션입니다.

Assert Message는 limit으로 정해진 시간 동안 화면에 변화가 감지되면 변한 부분에 있는 문자를 읽어서 작성자가 입력한 value값과 비교하게 됩니다.

#### Assert Message Attributes

1. comparator: 비교 조건을 선택할 수 있습니다.\
   \- = : 화면 요소의 Text와 value가 똑같은지 검사합니다.\
   \- \*= : value로 설정한 값이 화면 요소의 Text에 포함되어 있는지 검사합니다.\
   \- ^= : value로 설정한 값이 화면 요소의 Text에 시작 부분과 일치하는지 검사합니다.\
   \- $= : value로 설정한 값이 화면 요소의 Text에 끝 부분과 일치하는지 검사합니다.\
   \- match: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식과 일치하는지 검사합니다.\
   &#x20; 참고자료: [https://docs.python.org/3/library/re.html#re.match](https://docs.python.org/3/library/re.html#re.match)\
   \- search: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식을 포함하는지 검사합니다. \
   &#x20; 참고자료: [https://docs.python.org/3/library/re.html#re.search](https://docs.python.org/3/library/re.html#re.search)
2. value: 토스트 팝업의 메세지를 입력합니다. 모든 메세지 내용을 입력할 수도 있고, 일부 값 만을 입력할 수도 있습니다. 만약 이전에 설정한 값을 사용할 경우에는 ${key}를 입력합니다.
3. limit: 화면 요소가 나타날때까지 얼마나 기다릴지 설정할 수 있습니다.\
   \- 기본값: 5000\
   \- 최소값: 3000\
   \- 최대값: 10000\
   \- 단위: ms
4. use previous screen: 이전 스텝의 액션이 수행되기 전의 화면 정보부터 화면 변화를 감지할 지 액션 이후 화면부터 변화를 감지할지 선택할 수 있습합니다. true로 설정하면 이전 스텝의 액션 수행 전 화면부터 화면 감지를 시작합니다.
5. custom message: comparator 조건이 거짓일 경우 Output으로 출력할 메시지를 입력할 수 있습니다. 입력하지 않으면 거짓인 이유가 출력됩니다.
6. type: comparator가 거짓인 경우 검사 결과를 Error로 출력할지 Warning으로 출력할지 선택할 수 있습니다.\
   \- ERROR: 조건이 거짓이면 빨간색으로 결과가 출력되며 시나리오가 중단됩니다.\
   \- WARNING: 조건이 거짓이면 노란색으로 결과가 출력되며 다음 스텝이 계속 진행됩니다.

<figure><img src="../.gitbook/assets/image (210).png" alt=""><figcaption><p>Assert Message Attributes 예제</p></figcaption></figure>

