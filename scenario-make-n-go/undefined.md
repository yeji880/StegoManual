# 작성하기

시나리오는 아래 순서대로 작성됩니다.

{% hint style="info" %}
시나리오는 다음 순서대로 작성 및 저장합니다.

1. 스텝 생성하기
2. 스마트폰 화면 분석하기
3. 화면 요소 선택하여 스텝에 추가하기
4. 작성된 스텝 테스트하기
5. 시나리오 저장하기
{% endhint %}

1번 부터 3번까지 진행하면 하나의 스텝이 만들어지고 이렇게 만들어진 스텝들이 쌓여서 하나의 시나리오가 완성됩니다.

<figure><img src="../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

**1.스텝 생성하기**

스텝은 기본 스텝과 하위 스텝(Child) 두 종류로 나뉩니다.

① 기본 스텝 생성\
시나리오 작성 패널의 상단 툴바에 있는 <img src="../.gitbook/assets/image (73).png" alt="" data-size="line">를 클릭해서 생성할 수 있습니다. 신규로 작성된 스텝은 스텝 목록 최하단에 추가되며, 기본으로 설정되어 있는 액션은 Touch입니다.

스텝에서 선택 가능한 액션 목록 및 각 기능은 아래 링크를 참고 하시기 바랍니다.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

상단 툴바를 이용하는 방법 이외에 스텝에서 마우스 오른쪽 버튼을 클릭해서 뜨는 Context 메뉴를 이용해서 스텝을 만들수도 있습니다.\
&#x20;이미 스텝이 존재하는 경우에 스텝의 바로 앞에 스텝을 만들고 싶으면 **"Insert above"**를 클릭하고, 바로 뒤에 스텝을 만들고 싶을 때는 **"Insert below"**를 클릭하면 됩니다.

② 하위 스텝(Child) 생성\
액션 중 Control 항목(Loop Wait For제외)은 하단에 하위 스텝(Child Step)을 생성할 수 있습니다. \


③ 스텝의 <img src="../.gitbook/assets/image (94).png" alt="" data-size="line"> 아이콘을 위아래로 드래그&드롭하는 방식으로 Step의 순서를 변경할 수 있습니다.\
(하위 스텝 추가가 가능한 액션의 경우 특정 스텝을 드래그&드롭 하여 하위 스텝으로 넣을 수도 있습니다.)



④ 스텝 이름 수정하기                                                                                                                               &#x20;

스텝을 생성하면 처음에 설정되어 있는 스텝의 이름은 "Unnamed" 입니다.

처음 설정된 값을 수정하지 않고 스텝을 작성해 나가도 당장 시나리오를 작성하고 실행하는데는 아무런 문제가 없지만, 스텝이 쌓일수록 스텝간 구분이 어려워져 시나리오 유지보수가 어려워 집니다.

되도록 의미 있는 이름으로 스텝 이름을 설정해 주세요.

스텝 이름 필드를 클릭하면 커서가 활성화 되어 이름을 변경 할 수 있습니다.

<figure><img src="../.gitbook/assets/image (124).png" alt=""><figcaption><p>스텝 이름을 수정하지 않아 관리가 힘든 시나리오와 스텝 이름을 알아 보기 쉽게 수정해서 관리가 쉬운 시나리오 예제</p></figcaption></figure>



**2.스마트 폰 화면 분석하기**

스텝에서 액션을 수행할 앱의 화면에 대한 분석을 실행합니다. 화면 분석은 디바이스 패널 오른쪽 상단에 있는 <img src="../.gitbook/assets/image (178).png" alt="" data-size="line"> 을 클릭하면 실행됩니다.&#x20;

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption><p> 화면 분석 실행하기</p></figcaption></figure>

최적의 시나리오 작성을 위해 다양한 화면 분석 도구를 제공하고 있으며, 처음 화면 분석을 실행하면 기본적으로 OD(Object Detection) 방식으로 분석한 결과를 보여줍니다.

다양한 화면 분석 도구에 대한 자세한 설명은 아래를 참고해 주세요.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}



**3.화면 요소 선택하여 스텝에 추가하기**

<figure><img src="../.gitbook/assets/image (104).png" alt=""><figcaption><p>화면 요소를 선택하여 스텝에 추가하기</p></figcaption></figure>

화면 분석 결과 중에서 액션이 실행될 화면 요소를 선택하여 스텝에 추가합니다.&#x20;

스마트폰 화면 분석에서 분석한 결과에서 조작하고자 하는 화면 요소를 스텝의 액션 우측 공란에 드래그&드롭하면 스텝에 해당 화면 요소가 추가됩니다. 시나리오를 실행하면 스텝에 추가된 화면 요소를 대상으로 액션을 진행하게 됩니다.

만약, 화면 분석 도구로 찾아지지 않는 요소를 선택해야 한다면 ["Crop Image"](../strategy/crop-image.md) 분석도구를 이용해서 직접 화면 요소를 지정해서 가져올 수도 있습니다.



**4.작성된 스텝 테스트하기**&#x20;

작성이 끝난 시나리오를 실행하여 스텝이 원하는대로 잘 동작 하는지 확인할 수 있습니다.

시나리오를 실행하는 방법은 스텝의 Context 메뉴에서 "Play only" 또는 "Play until the end"를 선택하시면 됩니다.

(1) Play only\
특정 스텝만 한번 실행하고 싶을 때 사용합니다.\
선택한 스텝 실행을 마치면 다음 스텝으로 넘어가지 않고 테스트가 중단됩니다.

(2) Play until the end\
특정 스텝부터 마지막 스텝까지 실행하고 싶을 때 사용합니다.\
선택한 스텝부터 시나리오의 마지막 스텝까지 순서대로 실행됩니다.

<figure><img src="../.gitbook/assets/image (199).png" alt=""><figcaption><p>스텝 Context 메뉴</p></figcaption></figure>

하나의 스텝이 완성되면 다음 스텝을 작성하세요. 스텝들을 하나씩 완성해 나가다 보면 하나의 시나리오가 완성됩니다.



**5.시나리오 저장하기**

시나리오가 수정되어 저장이 필요한 경우에는 작성 패널 상단 시나리오 이름 옆에 노란색 동그라미 아이콘이 출력됩니다. 예) <img src="../.gitbook/assets/image (177).png" alt="" data-size="line">

저장하기 위해서는 작성 패널 상단 툴바에 있는 저장 아이콘(<img src="../.gitbook/assets/image (37).png" alt="" data-size="line">)을 클릭하거나 ⌘+S 단축키를 입력하면 현재 상태가 저장됩니다.

_<mark style="color:red;">주의) 시나리오는 자동저장 되지 않습니다. 작성중 틈틈이 시나리오를 저장해 주세요.</mark>_

_<mark style="color:red;"></mark>_
