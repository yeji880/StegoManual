# OCR(Optical Character Recognition)

<figure><img src="../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

화면에 있는 문자 정보를 읽어서 화면 요소로 제공해 줍니다. 현재 읽을 수 있는 문자는 한글, 영어, 숫자, 특수문자입니다.

OCR은 기본적으로 단어 단위로 인식합니다. 만약 여러개의 단어로 이루어진 문장을 하나의 화면 요소로 사용해야 할 경우에는 드래그&드롭으로 여러개의 단어를 선택해서 하나의 화면 요소로 사용할 수 있습니다.

### OCR Result Inspector

OCR로 인식한 단어에 대한 구체적인 정보는 화면 분석 패널 하단에 있는 "Inspector"를 클릭하면 확인 할 수 있습니다.

"Inspector"를 클릭하면 인식한 단어 목록이 테이블 형태로 출력됩니다.

1. TEXT: 인식한 단어 내용이 출력됩니다.
2. BOX: 단어의 화면상 위치 정보(좌표)가 출력됩니다.

Inspector 테이블의 항목을 클릭하면 화면 분석 결과에 노란색으로 선택한 부분이 활성화 됩니다.

반대로 화면 분석 결과에서 특정 화면 요소를 클릭해도 Inspector 테이블의 항목이 노란색으로 활성화 됩니다.

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

### OCR 화면 요소 Attribute

OCR을 사용한 스텝에서 화면 요소를 클릭하면 다양한 OCR 속성을 설정할 수 있습니다.

OCR 화면 요소 Attribute를 접근하는 방법은 아래 링크를 참고하세요.

[**화면요소 속성 확인 및 수정하기**](../scenario-make-n-go/undefined-4.md#undefined-1)****

1. Text: 화면 요소에 있는 문자 정보와 테스트할 때 비교 조건을 설정할 수 있습니다.\
   \= : 화면 요소의 Text와 value가 똑같은지 검사합니다.\
   \*= : value로 설정한 값이 화면 요소의 Text에 포함되어 있는지 검사합니다.\
   ^= : value로 설정한 값이 화면 요소의 Text에 시작 부분과 일치하는지 검사합니다.\
   $= : value로 설정한 값이 화면 요소의 Text에 끝 부분과 일치하는지 검사합니다.\
   match: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식과 일치하는지 검사합니다.\
   &#x20;           참고자료: [https://docs.python.org/3/library/re.html#re.match](https://docs.python.org/3/library/re.html#re.match)\
   search: 정규 표현식을 사용합니다. 화면 요소의 Text가 정규 표현식을 포함하는지 검사합니다. \
   &#x20;            참고자료: [https://docs.python.org/3/library/re.html#re.search](https://docs.python.org/3/library/re.html#re.search)
2. Text Similarity(threshold): 문자열 유사도를 뜻합니다.(비교 조건이 '=' 일때만 사용 가능) \
   시나리오 작성 당시와 테스트 실행 당시 문자 정보가 얼마나 동일해야 통과할지를 설정할 수 있습니다.\
   OCR의 특성상 동일 문자열을 인식할 때 해상도 및 기타 환경에 따라서 약간의 오인식이 발생 할 수 있는데, 이런 경우 유사도를 조절해서 작성할 수 있습니다. 값이 높을 수록 비교 정확도가 올라갑니다.\
   \- 기본값: 0.8\
   \- 최소값: 0\
   \- 최대값: 1
3. Case Sensitive: 알파벳 문자의 경우 대소문자 구분 여부를 설정할 수 있습니다.
4. Selector: 테스트를 진행할 때 화면 요소와 일치하는 요소가 여러개 나왔을 때 몇번째 요소를 사용할지 지정합니다. 0을 제외한 정수값으로 설정 가능합니다. (참고: '-1'을 입력했을 경우 맨 마지막 요소를 사용합니다.)

<figure><img src="../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>
