# CSS Flexbox
- 요소를 행과 열 형태로 배치하는 1차원 레이아웃 방식
- Flexbox 구성 요소
    - main axis
    - cross axis
    - flex container
    - flex item

- main axis (주 축)
    - flex item들이 배치되는 기본 축
    - main start에서 시작하여 main end 방향으로 배치 (기본 값)
- cross axis (교차 축)
    - main axis에 수직인축
    - cross start에서 시작하여 cross end 방향으로 배치(기본 값)
- Flex Container
    - display:flex; 혹은 display: inline-flex; 가 설정된 부모 요쇼
    - 이 컨테이너의 1차 자식 요소들이 Flex Item이 됨
    - flexbox 속성 값들을 사용하여 자식 요소 Flex Item들을 배치하는 주체
- Flex Item
    - Flex Container 내부에 레이아웃 되는 항목
    - 이후 배우는 내용을 이용해 자유로운 순서 변경 및 정렬 가능
    