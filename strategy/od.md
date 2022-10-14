# OD(Object Detection)

<figure><img src="../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

화면 분석 도구 중 기본 도구입니다.&#x20;

모바일 앱에서 일반적으로 사용되는 아이콘, 컴포넌트, 화면영역 등의 데이터를 학습한 AI 엔진이 주어진 화면을 분석하여 15개의 유형의 사용 가능한 화면 요소를 보여줍니다.

AI 엔진이 인식하는 화면 요소 유형은 아래와 같습니다.

* Home Icon
* Back Button
* HamburgerMenu
* Search Icon
* Clickable Object
* AD Icon
* More Icon
* Spinner Icon
* SearchArea
* Swipe Icon
* EditText Area
* Keyboard
* Tabs
* Close Icon
* Switch
* Thirdpartykeyboard

### OD Result Inspector

AI가 Object Detection으로 인식한 화면 요소에 대한 구체적인 정보는 화면 분석 패널 하단에 있는 "Inspector"를 클릭하면 확인할 수 있습니다.&#x20;

"Inspector"를 클릭하면 인식한 화면 요소가 테이블 형태로 출력됩니다.

1. LABEL: 화면 요소의 유형을 나타냅니다. 특별한 유형이 아닌 경우는 대부분 터치가 가능한 요소인 "Clickable"로 표시됩니다.
2. TEXT: 화면 요소에 문자열이 포함되어 있을 경우 OCR을 이용해 문자열까지 인식해서 출력합니다.
3. BOX: 화면 요소의 화면상 위치 정보(좌표)가 출력됩니다.

&#x20;_ <mark style="color:red;">주의) Object Detection으로 특징을 구분할 수 있는 요소(text)가 없는 화면을 분석할 경우, 분석한 결과와 같은label을 가진 요소를 selector로 지정한 순서에 따라 시나리오가 동작합니다.</mark>_

_<mark style="color:red;"></mark>_

Inspector 테이블의 항목을 클릭하면 화면 분석 결과에 노란색으로 선택한 부분이 활성화 됩니다.

반대로 화면 분석 결과에서 특정 화면 요소를 클릭해도 Inspector 테이블의 항목이 노란색으로 활성화 됩니다.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption><p>OD Inspector 활성화 된 상태 예제</p></figcaption></figure>

### OD 화면 요소 Attributes

OD를 사용한 스텝에서 화면 요소를 클릭하면 다양한 OD 속성을 설정할 수 있습니다.

OD 화면 요소 Attributes를 접근하는 방법은 아래 링크를 참고하세요.

[**화면요소 속성 확인 및 수정하기**](../scenario-make-n-go/undefined-4.md#undefined-1)****

1. Label: 화면 요소 유형
2. Text: 화면 요소에 있는 문자 정보와 테스트할 때 비교 조건을 설정할 수 있습니다.\
   \= : 화면 요소의 Text와 value가 똑같은지 검사합니다.\
   \*= : value로 설정한 값이 화면 요소의 Text에 포함되어 있는지 검사합니다.\
   ^= : value로 설정한 값이 화면 요소의 Text에 시작 부분과 일치하는지 검사합니다.\
   $= : value로 설정한 값이 화면 요소의 Text에 끝 부분과 일치하는지 검사합니다.\
   match: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식과 일치하는지 검사합니다.\
   &#x20;           참고자료: [https://docs.python.org/3/library/re.html#re.match](https://docs.python.org/3/library/re.html#re.match)\
   search: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식을 포함하는지 검사합니다. \
   &#x20;           참고자료: [https://docs.python.org/3/library/re.html#re.search](https://docs.python.org/3/library/re.html#re.search)\
   not used: Text 정보를 비교 대상으로 사용하지 않습니다.
3. Text Similarity(threshold): 문자열 유사도를 뜻합니다.(비교 조건이 '=' 일때만 사용 가능)\
   시나리오 작성 당시와 테스트 실행 당시 문자 정보가 얼마나 동일해야 통과할지를 설정할 수 있습니다.\
   OCR의 특성상 동일 문자열을 인식할 때 해상도 및 기타 환경에 따라서 약간의 오인식이 발생 할 수 있는데, 이런 경우 유사도를 조절해서 작성할 수 있습니다. 값이 높을 수록 비교 정확도가 올라갑니다.\
   \- 기본값: 0.8\
   \- 최소값: 0\
   \- 최대값: 1
4. Case Sensitive: 알파벳 문자의 경우 대소문자 구분 여부를 설정할 수 있습니다.
5. Selector: 테스트를 진행할 때 화면 요소와 일치하는 요소가 여러개 나왔을 때 몇번째 요소를 사용할지 지정합니다. 0을 제외한 정수값으로 설정 가능합니다. (참고: '-1'을 입력했을 경우 맨 마지막 요소를 사용합니다.)&#x20;

<figure><img src="../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>
