# 시나리오

시나리오는 1개 이상의 Step으로 구성됩니다.&#x20;

시나리오에 등록된 스텝은 위에서부터 순서대로 접속되어 있는 실제 디바이스에서 실행됩니다. Step에 대한 구체적인 정보 확인과 수정은 Step의 Attributes 패널에서 하실 수 있습니다.\
시나리오를 작성하는 법은 시나리오 작성과 실행 파트를 참고해 주세요.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

화면 왼쪽에 있는 시나리오 패널은 워크스페이스에 포함되어 있는 시나리오의 목록과 관리를 위한 기능들이 위치해 있습니다.

<figure><img src="../.gitbook/assets/image (107).png" alt=""><figcaption><p>시나리오 관리 패널</p></figcaption></figure>

**시나리오 생성하기**

시나리오를 생성하기 위해서는 시나리오를 담을 워크스페이스가 반드시 필요합니다.&#x20;

신규 워크스페이스를 작성하거나, 이미 작성된 워크스페이스를Open해 주세요.(※방법은 아래 참조)

{% content-ref url="undefined-2.md" %}
[undefined-2.md](undefined-2.md)
{% endcontent-ref %}

<figure><img src="../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>

① 신규 작성 또는 Open한 워크스페이스의 이름이 표시됩니다.\
② 시나리오 목록 상단에 있는 <img src="../.gitbook/assets/image (6).png" alt="" data-size="line">을 클릭합니다.\
③ 시나리오 이름을 입력하면 새로운 시나리오 만들기가 완료 됩니다.\
_<mark style="color:red;">주의) 시나리오는 특수문자(\`\~!@#$%^&\*|/’“;:/?) 를 포함하여 시나리오 이름을 설정할 수 없습니다.</mark>_

_<mark style="color:red;"></mark>_

**시나리오 불러오기**

시나리오 관리 패널 상단에 있는 <img src="../.gitbook/assets/image (111).png" alt="" data-size="line">을 클릭하면 내보내기해 두었던 시나리오를 불러올 수 있습니다.\
시나리오를 내보내기 하는 법은 아래 링크를 참고하세요.

{% content-ref url="../scenario-make-n-go/undefined-2.md" %}
[undefined-2.md](../scenario-make-n-go/undefined-2.md)
{% endcontent-ref %}

_<mark style="color:red;"></mark>_

**시나리오 Context 메뉴**

시나리오 항목에서 마우스 오른쪽 버튼을 클릭하면 관리할 수 있는 Context 메뉴가 활성화 됩니다.

&#x20;

<figure><img src="../.gitbook/assets/image (156).png" alt=""><figcaption><p>시나리오 Context 메뉴 </p></figcaption></figure>



**Rename : 시나리오 이름 변경하기**

이름을 변경하고자 하는 시나리오 위에서 마우스 오른쪽 클릭을 하고 "Rename" 메뉴를 클릭하면 이름을 변경할 수 있는 인터페이스가 뜹니다.\
변경하는 이름도 시나리오 생성 규칙과 동일한 이름 규칙이 적용됩니다.



**Delete : 시나리오 삭제하기**

삭제하고자 하는 시나리오 위에서 마우스 오른쪽 클릭을 하고 "Delete" 메뉴를 클릭합니다.



**Share : 공유 시나리오 만들기**

공유 시나리오로 만들 시나리오에서 마우스 오른 클릭 후 "Share" 메뉴를 클릭하거나 시나리오를 클릭 후 Shared Scenario로 드래그하면 공유 시나리오로 변경할 수 있습니다. \
_<mark style="color:red;">주의) 시나리오 이름 수정 시에는 Shared Scenario로 드래그 할 수 없습니다.</mark>_

{% hint style="info" %}
공유 시나리오란?

반복되는 부분을 하나의 시나리오 작성한 다음 다른 시나리오에서 불러와 사용 할 수 있습니다. 이렇게 다른 시나리오에서 불러와 사용할 수 있는 시나리오를 "공유 시나리오"라고 부릅니다.\
예로, 로그인이 필요한 앱인 경우 로그인 부분을 공유 시나리오로 작성한 다음 다른 시나리오를 작성할 때 로그인 부분을 다시 작성할 필요 없이 미리 작성해서 공유해둔 시나리오를 재활용할 수 있습니다.\
_<mark style="color:red;">주의) 공유 시나리오는 같은 워크스페이스 내에서만 사용할 수 있습니다. 그리고 공유 시나리오를 이미 포함하고 있는 시나리오를 다시 공유 시나리오로 변경하는 것은 불가능 합니다.</mark>_&#x20;
{% endhint %}



**Make a copy : 시나리오 복사하기**

비슷한 시나리오를 추가로 작성해야 할 경우 기존 시나리오를 복사해서 수정하는 것이 더 빠를 수 있습니다.

시나리오를 복사하는 방법은 오른쪽 버튼 클릭 후 "Make a copy"를 클릭하면 됩니다.

<mark style="background-color:red;"></mark>

**Copy to other workspace : 다른 워크스페이스에 시나리오 복사하기**

다른 워크스페이스에 시나리오를 복사해야 할 경우에는 "Copy to other workspace" 메뉴를 클릭 후 복사할 워크스페이스를 선택하면 됩니다.

