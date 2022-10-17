# 시나리오 테스트

* **테스트 시나리오를 작성하는 데 얼마나 걸리나요?**\
  때에 따라 다르지만, 프로그래밍 보다는 훨씬 빠르게 작성할 수 있습니다. Stego를 통한 테스트 시나리오 작성은 스마트폰 터치 제스처를 기반으로 이루어지며, GUI의 버튼과 텍스트 요소를 선택하여 원하는 동작을 드래그 앤 드랍 으로 저장하는 것만으로 충분합니다.\
  특히 Stego는 저작 도구로서 코드 작성 필요 없이, 사람의 동작을 흉내 내는 방식으로 작동합니다. 로그인 테스트처럼 간단한 케이스를 작성할 때, 초보자라면 약 10분, 숙련자라면 5분이면 가능합니다. 시나리오 작성과 관련된 자세한 사항은 사용설명서를 참조하세요.\

*   **테스트 지식이 없는 사람도 시나리오를 작성할 수 있나요?**

    네. 코드를 작성하지 않기 때문에 초보자도 쉽고 빠르게 시나리오를 작성할 수 있습니다.\

* **내가 작성한 시나리오를 팀과 공유하고 싶어요. 어떻게 해야 하나요?**\
  ****Stego에서 작성한 시나리오는 `내보내기`(Export), `불러오기`(Import) 기능을 통해 .zip 형태로 저장된 파일로 공유할 수 있습니다. 자세한 사항은 사용설명서를 참조하세요.\

*   **Stego내의 UIObject, OCR, OD, 그리고 Relative 기능에 대해 잘 이해하지 못했습니다. 무엇인가요?**

    Stego는 사람이 디바이스 애플리케이션을 이용할 때 상호작용하는 방식을 흉내 내도록 AI로 구현되었습니다.

    &#x20;\- 인공지능 기술을 바탕으로, Stego는 UIObject라고 불리는 특정 UI 요소를 구별합니다.\
    &#x20;\- UIObject는 AI 화면 분석을 통해 만들어진 UI 요소를 뜻합니다.\
    &#x20;\- OCR은 텍스트 형식의 UIObject를 뜻합니다.\
    &#x20;\- OD(Object Detection)은 AI를 통한 UIObject의 추천 선택을 뜻합니다.\
    &#x20;\- Relative는 화면 내의 선택 요소를 상값으로 한 UIObject를 뜻합니다.\
    &#x20; \* 기술과 관련된 다른 질문사항은 사용설명서를 참조하거나 stego.support@apptest.ai로 문의하세요.\

* **시나리오 테스트시에 어떻게 오류를 찾아 낼 수 있나요?**\
  ****테스트 도중 발생하는 ERROR / WARNING Message는 [디바이스](../basic/devices.md) 창 하단의 Output 창에 표시됩니다.\
  Message의 종류와 설명은 하단의 표를 참조하세요.

| ERROR / WARNING                                                              | Message 설명                                                                                                                                                             |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| {custom message}                                                             | Assertion에서 작성자가 입력한 메시지                                                                                                                                               |
| Invalid Variable: The {key} variable is not defined                          | <p>- Action의 key attribute에 입력한 값에 매칭되는 variable이 session에 선언(저장)되지 않은 경우<br>- Action의 value attribute에 ${VARIABLE}로 입력한 값에 매칭되는 variable이 session에 선언(저장)되지 않은 경우</p> |
| Invalid Value: The {value} pattern is an invalid regular expression          | Action의 value attribte에 regular expression을 잘못 입력한 경우                                                                                                                  |
| Condition Mismatched:{locator\_desc} {arg.comparator}                        | IfUIObject, AssertUIObject의 comparator의 조건과 일치하지 않는 경우                                                                                                                 |
| Condition Mismatched:{\_val} {self.\_to\_sign\_char(arg.comparator)} {value} | IfContent, IfValue, AssertContent, AssertValue의 comparator의 조건과 일치하지 않는 경우                                                                                             |
| Detected(n%) in {limit}ms                                                    | IfChanged, AssertChanged에서 제한시간(limit)내에 변화된 영역을 감지한 경우                                                                                                                |
| Detected(n%), but the difference score is lower than the threshold(y%)       | IfChanged, AssertChanged에서 제한시간(limit)내에 변화된 영역을 감지 하였으나, threshold값보다 변화량이 작은 경우                                                                                      |
| No changes detected in {limit}ms                                             | IfChanged, AssertChanged에서 제한시간(limit)내에 변화를 감지하지 못한경우                                                                                                                 |
| Condition Mismatched: {message} {arg.comparator} {value}                     | AssertMessage에서 comparator의 조건과 일치하지 않는 메시지를 감지한 경우                                                                                                                    |
| A system-side error occurred due to a connection failure with the device.    | 장비 연결문제로 인해 스텝을 수행할 수 없는 경우                                                                                                                                            |
| Invalid Step: {description of step}                                          | 스텝의 정보가 잘못된 경우                                                                                                                                                         |
| No Element Matched                                                           | UIObject를 테스트 당시 스크린에서 찾을 수 없는 경우                                                                                                                                      |
| Failed: {error message}                                                      | 시나리오가 실패한 경우                                                                                                                                                           |
