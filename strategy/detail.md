# 화면 분석 도구

Stego는 다양한 테스트 케이스를 빠르고 정확하게 시나리오로 작성할 수 있도록 다양한 화면 분석 도구들을 제공하고 있습니다.

현재 상황에 가장 적합한 분석 도구를 선택하는 것이 시나리오 완성도를 높이고 가장 견고하고 빠르게 작성할 수 있는 최고의 방법입니다.

화면 분석 도구에 대한 내용을 확인하셔서 현재 상황에 어떤 화면 분석 도구를 사용하면 좋을지 판단해 보시기 바랍니다.

현재 Stego는 총 6가지의 화면 분석 도구를 제공하고 있으며, 지속적인 연구 개발을 통해 업데이트를 계속 하고 있습니다.

### 화면 분석 시작하기

Stego에 디바이스를 연결하고 미러링이 시작된 상태에서 미러링 화면 오른쪽에 있는 메뉴 버튼 중 가장 상단에 있는 <img src="../.gitbook/assets/image (120).png" alt="" data-size="line">버튼을 클릭하면 현재 미러링 화면에 대한 화면 분석 패널로 전환되게 됩니다. 화면 분석 도구는 OD(Object Detection) 도구가 기본으로 설정되어 있습니다.&#x20;

<figure><img src="../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (46).png" alt=""><figcaption><p>화면 분석 도구 종류</p></figcaption></figure>

### 인터넷을 통해 가져온 이미지 분석하기&#x20;

디바이스의 미러링 화면을 분석하는 것 뿐만 아니라 디바이스 연결 없이 이미지 URL을 이용해 불러온 이미지의 화면을 분석할 수도 있습니다.\
테스트 실행 결과에서 시나리오 수정 사항이 발견되었을 때 디바이스를 연결하여 상황을 재현하는 것 보다 해당 기능을 사용하면 편리하게 시나리오를 수정할 수 있습니다. \
\
UIObject Selector 패널 상단 오른쪽에 있는 <img src="../.gitbook/assets/image (168).png" alt="" data-size="line">버튼을 클릭하면 이미지 URL을 입력하는 팝업창이 뜹니다. \
팝업창에 이미지 URL을 입력하면 URL을 통해 이미지를 가져온 다음 화면 분석을 실시합니다.

<figure><img src="../.gitbook/assets/image (63).png" alt=""><figcaption><p>이미지 URL을 이용한 화면 분석하기 </p></figcaption></figure>



### 보안화면 분석하기

안드로이드에서 'FLAG\_SECURE'가 적용되어 Vision을 통한 화면 분석이 불가능한 경우에도 Accessibility 기능을 통해 화면 분석이 가능합니다.

<figure><img src="../.gitbook/assets/스크린샷 2022-10-17 오후 1.06.44.png" alt=""><figcaption><p>Accessibility를 이용해 분석된 보안 화면</p></figcaption></figure>
