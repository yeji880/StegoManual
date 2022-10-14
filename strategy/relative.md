# Relative

<figure><img src="../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

내용이 실시간으로 바뀌어서 OD나 OCR로 화면 요소를 지정하기 애매할 경우 변하지 않는 화면 요소를 기준 삼아 상대 위치 기반으로 화면 요소를 지정해야 할 때 사용합니다.

기준점은 OD나 OCR, Crop Image 를 사용해 설정한 화면 요소가 사용되며, 실제로 사용될 화면 요소는 드래그&드롭으로 선택해서 설정합니다.

자세한 사용법은 예제를 참고하세요.

{% content-ref url="../tutorial/3..md" %}
[3..md](../tutorial/3..md)
{% endcontent-ref %}

{% content-ref url="../tutorial/5..md" %}
[5..md](../tutorial/5..md)
{% endcontent-ref %}

### Relative 화면 요소 Attribute&#x20;

Relative를 사용한 스텝에서 화면 요소를 클릭하면 다양한 속성을 설정할 수 있습니다.

화면 요소 Attribute를 접근하는 방법은 아래 링크를 참고하세요.

[**화면요소 속성 확인 및 수정하기**](../scenario-make-n-go/undefined-4.md#undefined-1)****

Relative 화면 요소는 기준점과 Relative 두가지에 대한 Attribute를 각각 제공합니다.

#### 기준점 화면 요소 Attribute&#x20;

기준점 설정에 사용한 화면 분석 도구의 Attribute를 참고하세요.

{% content-ref url="od.md" %}
[od.md](od.md)
{% endcontent-ref %}

{% content-ref url="ocr.md" %}
[ocr.md](ocr.md)
{% endcontent-ref %}

{% content-ref url="crop-image.md" %}
[crop-image.md](crop-image.md)
{% endcontent-ref %}

#### Relative 화면 요소 Attribute&#x20;

1. Left: 화면 요소의 좌측 상단 X 좌표
2. Top: 화면 요소의 좌측 상단 Y 좌표
3. Right: 화면 요소의 우측 하단 X 좌표
4. Bottom: 화면 요소의 우측 하단 Y 좌표

<figure><img src="../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>
