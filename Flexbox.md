# Flex Container 관련속성
- display
- flex-direction
- flex-wrap
- justify-content
- align-items
- align-content

# Flex Item 관련 속성
- align-self
- flex-grow
- flex-basis
- order

---

# Flex Container 지정
- display 속성을 flex로 설정하면, Flex Container로 지정됨
- flex item은 기본적으로 행(주 축의 기본값인 가로 방향)으로 나열
- flex item은 주 축의 시작 선에서 시작
- flex item은 교차 축의 크기를 채우기 위해 늘어남

# flex-direction
- flex item이 **나열되는 방향을 지정**
- 속성
    - row(기본값): 아이템을 가로 방향으로, 왼쪽에서 오른쪽으로 배치
    - column: 아이템을 세로 방향으로, 위에서 아래로 배치
    - "-reverse"로 지정하면 flex item 배치의 시작 선과 끝 선이 서로 바뀜

# flex-wrap
- flex item 목록이 flex container의 한 행에 들어가지 않을 경우, **다른 행에 배치할지 여부 설정**
- 속성
    - nowrap(기본값): 줄 바꿈을 하지 않음
    - wrap: 여러 줄에 걸쳐 배치될 수 있게 설정

# justify-content
- 주 축을 따라 flex item 들을 정렬하고 간격을 조정
- 속성
    - flex-start(기본값): 주 축의 시작점으로 정렬
    - center : 주 축의 중앙으로 정렬
    - flex-end : 주 축의 끝점으로 정렬

# align-content
- 컨테이너에 여러 줄의 flex item이 있을 때, 그 줄들 사이의 공간을 어떻게 분배할지 지정
    - flex-wrap이 wrap 또는 wrap-reverse로 설정된 여러 행에만 적용됨
    - Flex 아이템이 두 줄 이상일 때만 의미가 있음(flex-wrap이 nowrap으로 설정된 경우)
- 속성
    - strtch(기본값) : 여러 줄을 교차 축에 맞게 늘려 빈 공간을 채움
    - center : 여러 줄을 교차 축의 중앙에 맞춰 정렬
    - flex-start : 여러 줄을 교차 축의 시작점(보통 위쪽)에 맞춰 정렬
    - flex-end : 여러 줄을 교차 축의 끝점(보통 아래쪽)에 맞춰 정렬

# align-items
- 컨테이너 안에 있는 flex item 들의 **교차 축 정렬** 방법을 지정
- 속성
    - stretch(기본 값) : 아이템을 교차 축 높이를 꽉 채우도록 늘어남
    - center : 아이템을 교차 축의 중앙에 맞춰 정렬
    - flex-start : 아이템을 교차 축의 시작점(가로 방향일 경우 위쪽)에 맞춰 정렬
    - flex-end : 아이템을 교차 축의 끝점(가로 방향일 경우 아래쪽)에 맞춰 정렬

# align-self
- 컨테이너 안에 있는 flex item 들을 교차 축을 따라 개별적으로 정렬
- 속성
    - auto(기본 값): 부모 컨테이너의 align-items 속성 값을 상속
    - stretch: 해당 아이템만 교차 축 방향으로 늘어나 컨테이너를 꽉 채우도록 정렬
    - center : 해당 아이템만 교차 축의 중앙에 정렬
    - flex-start: 해당 아이템만 교차 축의 시작점에 정렬
    - flex-end : 해당 아이템만 교차 축의 끝점에 정렬

---

# 목적에 따른 속성 분류
- 배치 (flex-direction, flex-wrap)
- 공간 분배(justify-content, align-content)
- 정렬 (align-items, align-self)

# 속성 쉽게 이해하는 방법
- justify - 주축
- align - 교차 축