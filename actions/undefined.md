# 액션 목록

<figure><img src="../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

①<img src="../.gitbook/assets/image (188).png" alt="" data-size="line">버튼을 눌러 Step을 생성 합니다.

② 클릭하여 생성된 Step의 이름을 변경할 수 있습니다.

③ 생성된 Step에서 액션 선택영역을 누르면 아래와 같이 선택 가능한 액션 리스트가 표시됩니다.

<figure><img src="../.gitbook/assets/image (61).png" alt=""><figcaption><p>액션 목록</p></figcaption></figure>

#### Motion

스마트폰을 실제로 조작할 때 사용되는 동작들입니다.

{% content-ref url="motion.md" %}
[motion.md](motion.md)
{% endcontent-ref %}

#### Variables

테스트 도중 특정 값을 저장해 두거나, 랜덤하게 값(숫자, 텍스트)을 생성하는 기능이 있습니다. 여기서 저장해 둔 값들은 다른 스텝에서도 사용이 가능합니다.

{% content-ref url="variables.md" %}
[variables.md](variables.md)
{% endcontent-ref %}

#### Control

시나리오에 분기점이 필요하거나 동일 스텝들을 반복해야 할 때 사용할 수 있는 기능들이 있습니다.

{% content-ref url="control.md" %}
[control.md](control.md)
{% endcontent-ref %}

#### Assertion

화면상 특정 위치에 요소나 문자열이 있는지 검사할 때 사용하는 기능들입니다. 실제 테스트를 위해 사용되는 스텝 액션으로 여기 있는 액션을 통과하지 못하면 빨간색으로 에러 메시지가 출력되면서 시나리오가 중지 됩니다.

주로 특정 스텝 수행 후 그 스텝이 잘 진행되었는지 확인 하는 과정(예: 로그인 후 환영 메시지가 출력되는지 확인)에서 사용됩니다.

{% content-ref url="assertion.md" %}
[assertion.md](assertion.md)
{% endcontent-ref %}

#### Events

Motion 이외에 디바이스에서 할 수 있는 다양한 컨트롤 동작들이 모여 있습니다. 예를 들어 세로 화면을 가로 화면으로 바꾸거나 앱 실행 혹은 종료 시키는 등의 이벤트를 발생 시킬 수 있습니다.

{% content-ref url="events.md" %}
[events.md](events.md)
{% endcontent-ref %}

#### Advanced

시나리오를 보다 풍성하게 작성하기 위한 고급 기능이 포함되어 있습니다. 현재는 Shared Scenario 기능만 있지만, 지속적으로 기능들이 업데이트 될 예정입니다.

{% content-ref url="advanced.md" %}
[advanced.md](advanced.md)
{% endcontent-ref %}

