# Crop Image

<figure><img src="../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

OD나 OCR 도구로 인식이 되지 않은 부분을 화면 요소로 사용해야 할 경우 작성자가 직접 화면 요소를 지정할 때 사용하는 화면 분석 도구 입니다.

작성자가 디바이스 화면에서 직접 드래그&드롭으로 화면 요소를 직접 선택하게 되며, 이렇게 선택된 화면 요소는 해당 영역의 이미지를 특징 매칭(Feature Matching)기법을 사용해 분석해서 비교하게 됩니다.

Crop Image로 화면 요소를 만들 때는 몇가지 주의 사항이 있습니다.

1. 단순한 이미지 보다는 복잡한 이미지가 인식률이 높습니다.\
   이미지의 특징점을 추출해서 비교대상으로 사용하기 때문에 간단한 이미지 보다는 복잡한 이미지 일수록 추출되는 특징점들이 많아서 인식률이 높아집니다.
2. 이미지를 선택할때 되도록 바탕화면이 포함되지 않도록 지정하면 인식률이 높아집니다.\
   이는 단색 영역의 비중이 높아질수록 상대적으로 특징점 비율이 낮아지기 때문입니다.\
   ![](https://lh4.googleusercontent.com/s5SO\_xR5s1Cw6GVEWoBqnLbevayzzV6IPxF-iSE4caplR3FQHbNA-9cphevKJiyxYUZNBkRXyf6A9Yyr2uzot1i\_AdMAAEC3YgDqJd4k2-4NwUhlMTNlpjblAiFYbqGnM1brDIY9Y-7Gz8cq2RyxTtaaAdabQHVXWxCeOqiAbdyriJeeaXHxEbaop\_A\_) 바탕화면 영역까지 포함해서 지정했을 때 보다 \
   ![](<../.gitbook/assets/image (171).png>) 바탕화면 영역을 최소한으로 잡히도록 지정하는 것이 인식률이 더 높습니다.

### Crop Image 화면 요소 Attribute&#x20;

Crop Image를 사용한 스텝에서 화면 요소를 클릭하면 다양한 속성을 설정할 수 있습니다.

화면 요소 Attribute를 접근하는 방법은 아래 링크를 참고하세요.

[**화면요소 속성 확인 및 수정하기**](../scenario-make-n-go/undefined-4.md#undefined-1)****

1. Left: 화면 요소의 좌측 상단 X 좌표
2. Top: 화면 요소의 좌측 상단 Y 좌표
3. Right: 화면 요소의 우측 하단 X 좌표
4. Bottom: 화면 요소의 우측 하단 Y 좌표
5. Threshold: 특징 매칭(Feature Matching) 유사도. 수치가 높을 수록 비슷한 점이 많아야 통과됩니다.\
   \- 기본값: 0.7\
   \- 최소값: 0\
   \- 최대값: 1

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>
