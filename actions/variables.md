# Variables

테스트 도중 특정 값을 저장해 두거나, 랜덤하게 값을 생성하는 기능이 있습니다. 여기서 저장해 둔 값들은 다른 스텝에서 사용됩니다.

&#x20;_ <mark style="color:red;">주의) key 값은 대소문자를 구분하지 않습니다.</mark>_

### Store Value

작성자가 특정 값을 저장해 두는 용도로 사용됩니다.

예를 들어 로그인 아이디를 자주 입력해야 하는 시나리오를 작성해야 한다면, 초반에 값을 미리 설정해 두고 필요한 곳에서 불러와 쓸 수 있습니다.

#### Store Value Attributes&#x20;

1. key: 값을 저장해 두고 다른 곳에서 사용할때 사용될 키값입니다.
2. value: key 값으로 저장되어 있는 실제 데이터 입니다.

<figure><img src="../.gitbook/assets/image (197).png" alt=""><figcaption><p>Store Value Attributes 예제</p></figcaption></figure>

### Store Content

화면의 특정 위치에 있는 문자열을 읽어들려 저장해 두는 기능입니다. 여기서 저장된 값을 다른 스텝에서 사용할 때는 key 값을 사용하면 됩니다.

다음 예제를 참고하세요.

{% content-ref url="../tutorial/3..md" %}
[3..md](../tutorial/3..md)
{% endcontent-ref %}

#### Store Content Attributes&#x20;

1. key: 다른 스텝에서 저장한 값을 사용할 때 쓰기 위한 식별자 입니다.
2. UIObject: 데이터를 읽어들일 화면 요소를 출력합니다.
3. pattern: 정규표현식을 사용할 수 있습니다.\
   만약 특정 위치에 대소문자 구분없이 "welcome"이라는 문구가 있을때만 값을 저장하고 싶으면 <mark style="background-color:blue;">/welcome/i</mark> 정규표현식을 입력하면 됩니다.

<figure><img src="../.gitbook/assets/image (94).png" alt=""><figcaption><p>Store Content Attributes 예제</p></figcaption></figure>

### Random Number

랜덤으로 숫자를 생성해서 사용하고 싶을때 사용할 수 있는 기능입니다.

#### Random Number Attributes&#x20;

1. key: 저장한 값을 사용할 때 쓰기 위한 식별자 입니다.

<figure><img src="../.gitbook/assets/image (154).png" alt=""><figcaption><p>랜덤 숫자 생성 Attributes 예제</p></figcaption></figure>

### Random Text

랜덤하게 생성된 텍스트를 만들 수 있습니다.

랜덤 생성에 사용되는 문자는 영문 소문자(a-z), 영문 대문자(A-Z) 그리고 숫자 0-9 입니다.

#### Random Text Attributes&#x20;

1. key: 저장한 값을 사용할 때 쓰기 위한 식별자 입니다.
2. prefix (optional): 텍스트 앞부분에 고정된 값을 사용하고 싶을 때 설정할 수 있습니다.
3. number of characters: 랜덤으로 생성할 문자 수를 지정할 수 있습니다. (1-10 중에 선택할 수 있습니다.)

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption><p>랜덤 문자열 생성 Attributes 예제</p></figcaption></figure>

### Export Variable

현재 시나리오에서 저장한 값(Store Value, Store Content, Random Number, Random Text)을 다른 시나리오에서 사용할 수 있도록 지정할 수 있습니다.

다른 시나리오에서 저장한 값을 사용하기 위해서는 먼저 해당 시나리오가 공유 시나리오가 되어야 하고, 사용할 값을 Export Variable로 지정해 줘야 합니다.&#x20;

#### Export Variable Attributes&#x20;

1. key: 다른 시나리오와 공유할 저장한 값의 key를 입력합니다.

<figure><img src="../.gitbook/assets/image (193).png" alt=""><figcaption><p>변수 공유 Attributes 예제</p></figcaption></figure>
