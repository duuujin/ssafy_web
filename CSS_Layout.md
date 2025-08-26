# block 타입
- 하나의 독립된 덩어리처럼 동작하는 요소
- 항상 새로운 행으로 나뉨
- width, height, margin, padding 속성을 모두 사용할 수 있음
- padding, margin, border로 인해 다른 요소를 상자로부터 밀어냄
- width 속성을 지정하지 않으면 박스는 inline 방향으로 사용 가능한 공간을 모두 차지함
    - 상위 컨테이너 너비 100%로 채우는 것
- 대표적인 block 태그
    - h1~6, p, div, ul, li
## block 타입의 대표: div
- 다른 HTML 요소들을 그룹화 하여 레이아웃을 구성하거나 스타일링을 적용할 수 있음
- 헤더, 푸터, 사이드바 등 웹 페이지의 다양한 섹션을 구조화하는데 가장 많이 쓰이는 요소

# inline 타입
- 문장 안의 단어처럼 흐름에 따라 자연스럽게 배치되는 요소
- 줄바꿈이 일어나지 않음 (콘텐츠의 크기만큼만 영역을 차지)
- width와 height 속성을 사용할 수 없음
- 수직 방향 (상하)
    - padding, margin, border가 적용되지만, 다른 요소를 밀어낼 수는 없음
- 수평 방향 (좌우)
    - padding, margin, border가 적용되어 다른 요소를 밀어 낼 수 있음
- 대표적인 inline 타입 태그
    - a, img, span, strong

## inline 타입의 대표: span
- 자체적으로 시각적 변화 없음
    - 스타일을 적용하기 전까지는 특별한 변화 없음
- 텍스트 일부 조작
    - 문장 내 특정 단어나 구문에만 스타일을 적용 할 때 유용
- 블록 요소처럼 줄바꿈을 일으키지 않으므로, 문서의 구조에 큰 변화를 주지 않음

# Normal flow 
- 일반적인 흐름 또는 레이아웃을 변경하지 않은 경우 웹 페이지 요소가 배치되는 방식

---

# 기타 display

---

# inline 타입 - inline-block 타입
- inline과 block의 특징을 모두 가진 특별한 display 속성 값
- Block과 Inline의 특징을 합친 것 (줄바꿈 없이, 크기 지정 가능)
- width 및 height 속성 사용 가능 
- padding, margin 및 border로 인해 다른 요소가 상자에서 밀려남

# none 타입
- 요소를 화면에 표시하지 않고, 공간조차 부여되지 않음

---

# CSS Layout 
- 각 요소의 **위치**와 **크기를 조정**하여 웹 페이지의 디자인을 결정하는 것
- 요소들을 상하좌우로 정렬하고, 간격을 맞추고, 전체적인 페이지의 뼈대를 구성
- 핵심 속성: display(block, inline, flex, grid...)

# CSS Position
- 요소를 Normal Flow에서 제거하여 **다른 위치로 배치**하는 것
- 다른 요소 위에 올리기, 화면의 특정 위치에 고정시키기 등
- 핵심 속성: position(static, relative, absolute, fixed, sticky...)

# Position: static
- 요소를 Normal Flow에 따라 배치
- top, right, bottom, left 속성이 적용되지 않음

# Position: relative
- 요소를 Normal Flow에 따라 배치
- 자신의 원래 위치(static)을 기준으로 이동
- top, right, bottom, left 속성으로 위치를 조정
- 다른 요소의 레이아웃에 영향을 주지 않음(요소가 차지하는 공간은 static일 때와 같음)

# Position: absolute
- 요소를 Normal Flow에서 제거
- 가장 가까운 relative 부모 요소를 기준으로 이동
    - 만족하는 부모 요소가 없다면 body 태그를 기준으로 함
- top, right, bottom, left 속성으로 위치를 조정
- 문서에서 요소가 차지하는 공간이 없어짐

# Position: fixed
- 요소를 Normal Flow에서 제거
- 현재 화면영역(viewport)을 기준으로 이동
- 스크롤해도 항상 같은 위치에 유지됨
- top,right,bottom,left 속성으로 위치를 조정
- 문서에서 요소가 차지하는 공간이 없어짐

# Position: sticky
- relative와 fixed의 특성을 결합한 속성
- 스크롤 위치가 임게점에 도달하기 전에는 relative처럼 동작
- 스크롤 위치가 임계점에 도달하면 fixed처럼 화면에 고정
- 다음 sticky 요소가 나오면 이전 sticky 요소의 자리를 대체
    - 이전 sticky 요소와 다음 sticky 요소의 위치가 겹치게 되기 때문

# z-index
- 요소의 쌓임 순서를 정의하는 속성
- 정수 값을 사용해 Z축 순서를 지정
- 값이 클수록 요소가 위에 쌓이게 됨
- static이 아닌 요소에만 적용됨
- 기본값은 auto로 부모 요소의 z-index 값에 영향을 받음
- 같은 부모 내에서만 z-index 값을 비교하고, 값이 같으면 HTML 문서 순서대로 쌓임
- 부모의 z-index가 낮으면 자식의 z-index가 아무리 높아도 부모보다 위로 올라갈 수 없음