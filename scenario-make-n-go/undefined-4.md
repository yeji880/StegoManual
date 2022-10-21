# 스텝 속성 설정

스텝은 크게 액션과 화면 요소로 구성되며, 각 구성 요소에 대한 세부 설정을 통해 보다 정교한 시나리오 작성이 가능합니다.

### 액션 속성 수정하기

① 스텝의 빈공간을 클릭하면 스텝에 설정된 액션의 속성을 변경할 수 있는 Attributes 패널이 하단에 활성화 됩니다.

<figure><img src="../.gitbook/assets/image (126).png" alt=""><figcaption><p>액션 속성 패널</p></figcaption></figure>



② 속성 목록은 액션의 종류에 따라 다릅니다.

자세한 설명은 액션 목록의 각 액션 항목을 참고해 주세요.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}



### 화면 요소 속성 확인 및 수정하기

스텝의 화면 요소를 클릭하면 화면 요소에 대한 세세한 설정을 할 수 있는 UIObject Field 창이 뜹니다.

<figure><img src="../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>

#### UIObject Field

<figure><img src="../.gitbook/assets/image (125).png" alt=""><figcaption><p>UIObject Field 창</p></figcaption></figure>

****\
**① 화면 요소 목록**

스텝 목록에서는 하나의 화면 요소만 보이지만 UIObject Field 창을 통해서 여러개의 화면 요소를 추가할 수 있습니다.  테스트가 수행될 때 화면 요소들 중 하나라도 현재 디바이스 화면과 매칭된 것이 있으면 해당 요소를 대상으로 액션을 수행합니다.

예를 들어, 디바이스의 언어 설정에 따라 Youtube 아이콘은 동일한데 앱이름이 다를 경우(영어/한글) 화면 요소에 영어 버전 Youtube 아이콘과 한글 버전 Youtube 아이콘을 함께 등록해두면 디바이스 언어와 상관없이 해당 스텝이 실행 가능하게 됩니다.\


**② 화면 요소 속성 패널**

처음에는 가장 먼저 추가 되었던 화면 요소의 속성이 출력됩니다. 화면 요소 목록에서 특정 요소를 클릭하면 해당 요소의 속성이 출력됩니다.

이 패널에서 세세한 속성값 조정을 통해 보다 더 견고하고 세밀한 시나리오 작성이 가능합니다. 화면 요소의 속성값들은 화면 요소를 생성할 때 사용했던 화면 분석 도구에 따라 다릅니다.

각 속성에 대한 자세한 설명은 화면 분석 도구에서 확인하세요.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

****\
**③ 화면 요소 추가 드롭 공간**

스텝에 새로운 화면 요소를 추가할 때 사용합니다. 화면 분석 패널에서 새로운 화면 요소를 선택해서 이 공간에 드래그&드롭하면 현재 스텝에 새로운 화면 요소가 추가됩니다.

<figure><img src="../.gitbook/assets/image (65).png" alt=""><figcaption><p>현재 스텝에 새로운 화면 요소 추가하는 방법</p></figcaption></figure>

****\
**④ 화면 요소 테스트하기**

화면 요소 목록에서 선택된 화면 요소와 연결된 디바이스의 화면으로 테스트하는 버튼입니다.  테스트를 하면 UIObject Field 창이 테스트 모드로 변경됩니다.&#x20;

테스트 모드를 종료하려면 "Quit Test Mode" 버튼을 클릭하세요.

<figure><img src="../.gitbook/assets/image (162).png" alt=""><figcaption><p>화면 요소 테스트 모드 화면</p></figcaption></figure>

****\
**⑤ 화면 요소 삭제하기**

여러개의 화면 요소 중 필요없는 요소를 삭제할 수 있습니다. 다만 스텝에 추가된 화면 요소가 한 개일 때는 삭제가 되지 않습니다.

