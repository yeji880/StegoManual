# 예제1. 앱 실행하기

테스트의 가장 기본이 되는 앱을 실행하는 몇가지 방법에 대해서 실습해 보겠습니다.

1.  바탕 화면의 아이콘을 클릭해서 실행하기\


    스마트폰의 바탕 화면에 있는 아이콘을 클릭해서 앱을 실행해 보겠습니다.\

2. 앱이름을 검색해서 실행하기\

3. 앱 고유 아이디값을 이용해 바로 실행하기\


### 1. 바탕화면의 아이콘 클릭해서 실행하기&#x20;

스마트폰의 바탕 화면에 있는 아이콘을 클릭해서 앱을 실행해 보겠습니다.

<mark style="background-color:green;">Step1.</mark> 새 스텝을 만들고 "Touch"액션을 선택합니다. (새 스텝을 생성 하면 기본 액션이 "Touch"로 지정됩니다.)

<figure><img src="../.gitbook/assets/스크린샷 2022-09-22 오후 12.57.08.png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:green;">Step2.</mark> 화면 분석 후 분석 도구로 "OD"를 선택합니다.

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:green;">Step3.</mark> 화면에서 "Youtube"를 선택한 다음 드래그&드롭으로 선택해서 스텝의 UIObject로 추가합니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-09-23 오후 3.29.04.png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:green;">Step4.</mark> 작성한 스텝을 실행합니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-09-22 오후 3.00.11.png" alt=""><figcaption></figcaption></figure>



### 2. 앱 이름을 검색하여 실행하기&#x20;

앱 이름을 검색하기 위해서는 먼저 검색 창으로 이동해야 합니다.&#x20;

<mark style="background-color:green;">Step1.</mark> 새 스텝을 만들고 "Scroll"액션을 선택합니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-09-22 오후 3.12.07.png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:green;">Step2.</mark> 화면 분석 후 분석 도구로 "Full Screen"을 선택합니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-09-22 오후 3.13.54.png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:green;">Step3.</mark> 선택된 "Full Screen"을 드래그&드롭 하여 스텝의 UIObject로 추가합니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-09-23 오후 3.34.37.png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:green;">Step4.</mark> 새로운 스텝을 만들고 액션은 "Touch"로 선택, 디바이스 화면 분석 도구로 OCR을 선택한 다음 화면에서 "Search"를 드래그&드롭하여 UIObject로 추가합니다.&#x20;

<figure><img src="../.gitbook/assets/스크린샷 2022-09-23 오후 3.38.16.png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:green;">Step5.</mark> 새로운 스텝을 만들고 액션은 "Input"을  선택, 디바이스 화면 분석 도구로 Full Screen을 선택한 다음 전체화면을 드래그&드롭 하여 UIObject로  설정합니다. 그 후 value 값에 "Youtube"를 입력합니다.&#x20;

<figure><img src="../.gitbook/assets/스크린샷 2022-09-23 오후 3.44.46.png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:green;">Step6.</mark> 새로운 스텝을 만들고 액션은 "Touch"를  선택, 디바이스 화면 분석에서 Crop image를 선택한 다음 앱의 아이콘 부분을 마우스로 드래그하여 선택한 후, 드래그&드롭 하여 UIObject로 추가합니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-09-23 오후 3.52.27.png" alt=""><figcaption></figcaption></figure>



### 3. 앱 고유 아이디값을 이용해 바로 실행하기

<mark style="background-color:green;">Step1.</mark> 새 스텝을 만들고 "Launch"액션을 선택합니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-09-22 오후 5.39.13.png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:green;">Step2.</mark> 실행하고자 하는 앱(Youtube)의 App ID를 입력합니다. 테스트 할 기기가 Android일 경우 화면 하단 Attributes의 Package Name에 , iOS일 경우 Bundle ID에 입력합니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-09-22 오후 5.42.08.png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:green;">Step3.</mark> 작성한 스텝을 실행합니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-09-22 오후 5.42.42.png" alt=""><figcaption></figcaption></figure>
