# 시나리오 속성 설정

<figure><img src="../.gitbook/assets/image (212).png" alt=""><figcaption></figcaption></figure>

작성 패널 툴바 중 톱니 아이콘(<img src="../.gitbook/assets/image (117).png" alt="" data-size="line">)을 클릭하면 아래와 같은 시나리오 속성창이 표시됩니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-09-26 오후 3.10.16 (1).png" alt=""><figcaption><p>시나리오 속성 설정창</p></figcaption></figure>

#### User Variable : 사용자 설정 변수

사용자 설정 변수 기능은 시나리오에서 자주 사용될 것으로 예상되는 값을 미리 저장해 두고 사용하기 위한 값입니다.

액션 중 ["Store Value"](../actions/variables.md#store-value)가 비슷한 기능을 하는데, 다른 점은 "Store Value"를 사용한 스텝 이후에 실행되는 스텝에서만 설정한 값을 사용할 수 있는 반면, 사용자 설정 변수로 만들어둔 값은 시나리오가 실행되는 동안 어떤 스텝에서든 사용할 수 있습니다. \


#### 사용자 설정 변수 만들기

시나리오 속성창에서 <img src="../.gitbook/assets/image (207).png" alt="" data-size="line">을 클릭하면 새로운 key와 value를 입력할 수 있는 입력란이 출력됩니다.

출력된 입력란에 key와 value를 입력한 다음, <img src="../.gitbook/assets/image (218).png" alt="" data-size="line">를 클릭하면 사용자 설정 변수가 만들어 집니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-09-26 오후 3.11.18.png" alt=""><figcaption><p>새로운 사용자 설정 변수 만들기</p></figcaption></figure>

\
사용자 설정 변수 수정 / 삭제 하기

사용자 설정 변수는 수정 가능한 입력란 형태로 출력이 되기 때문에 key나 value 값을 수정한 다음 <img src="../.gitbook/assets/image (218).png" alt="" data-size="line">를 클릭하면 수정 사항이 저장됩니다.

삭제는 변수 오른쪽에 있는 <img src="../.gitbook/assets/image (175).png" alt="" data-size="line">버튼을 클릭한 다음, <img src="../.gitbook/assets/image (218).png" alt="" data-size="line">를 클릭하면 해당 사용자 설정 변수가 삭제됩니다.

_<mark style="color:red;">주의) 사용자 설정 변수를 생성, 수정, 삭제 한 다음 반드시</mark>_ <img src="../.gitbook/assets/image (218).png" alt="" data-size="line">_<mark style="color:red;">버튼을 클릭해서 저장해야 작업한 내용이 적용됩니다.</mark>_

####

#### 사용자 설정 변수 사용하기

만들어둔 변수를 사용해야 하는 곳에 변수의 key값을 입력하면 사용할 수 있습니다.

여기서 주의할 점은 key값을 입력할 때는 ${key값}형태로 입력하셔야 합니다. 이는 작성자가 입력하고자 하는 값이 일반 문자인지 변수인지를 구분하기 위한 규칙입니다.

예를들어 위에서 만들어둔 변수인 age를 사용하기 위해서는 ${age}를 입력하시면 됩니다.(값은 age 변수를 설정할 때 value로 저장한 34가 됩니다.)

_<mark style="color:red;">주의) 변수를 사용할 경우에는 반드시 변수의 key값을 ${key값} 형태로 입력해주세요.</mark>_

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption><p>사용자 설정 변수 사용하기 예제</p></figcaption></figure>

#### &#x20;공유 시나리오의 사용자 설정 변수

공유 시나리오를 불러와 사용하고 있는 시나리오는 사용자 설정 변수 목록에 공유 시나리오에 설정된 사용자 설정 변수도 함께 출력됩니다.

<figure><img src="../.gitbook/assets/photo_2022-09-26 15.18.39.jpeg" alt=""><figcaption><p>공유 시나리오의 사용자 설정 변수가 함께 출력된 설정창</p></figcaption></figure>

다만, 목록에 보인다고 해서 출력된 모든 변수를 사용할 수 있는 것은 아닙니다.

실제로 공유 시나리오의 사용자 설정 변수를 사용하기 위해서는 공유 시나리오에서 "Export Variable" 액션으로 사용할 사용자 설정 변수를 설정해 줘야 이 공유 시나리오를 불러온 부모 시나리오에서 변수를 사용할 수 있습니다.

<figure><img src="../.gitbook/assets/image (99).png" alt=""><figcaption><p>공유 시나리오에서 Export Variable을 하지 않아 실행이 실패한 경우</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption><p>공유 시나리오에서 Export Variable을 해 서 실행이 성공한 경우</p></figcaption></figure>

"Export Variable"에 대한 자세한 설명은 ["액션 목록"](broken-reference) 아래 "Variables" 페이지를 아래 참고해 주세요.

{% content-ref url="../actions/variables.md" %}
[variables.md](../actions/variables.md)
{% endcontent-ref %}
