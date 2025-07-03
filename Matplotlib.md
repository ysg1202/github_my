# Matplotlib이란?
- Matplotlib은 파이썬에서 가장 널리 쓰이는 데이터 시각화 라이브러리
- 선 그래프, 막대 그래프, 히스토그램, 산점도 등 다양한 그래프를 쉽게 그릴 수 있음
- 데이터 분석, 머신러닝 시각화, 자율주행 센서 데이터 시각화 등에서 활용

# 설치 및 버전 확인
```python
pip install matplotlib

import matplotlib
print(matplotlib.__version__)
```
## 그래프 종류
| 그래프 종류   | 함수             | 설명                                 |
|--------------|----------------------|--------------------------------------|
| 선 그래프     | `plt.plot()`         | 데이터의 흐름이나 경향을 선으로 표현 |
| 막대 그래프   | `plt.bar()`          | 범주형 데이터의 크기를 막대로 표현   |
| 수평 막대 그래프 | `plt.barh()`        | 막대를 가로 방향으로 표현             |
| 히스토그램   | `plt.hist()`         | 데이터 분포를 막대로 표현             |
| 산점도       | `plt.scatter()`      | 두 변수 간의 관계를 점으로 표현       |
| 파이 차트     | `plt.pie()`          | 전체에 대한 각 항목의 비율 표현       |
| 박스 플롯     | `plt.boxplot()`      | 데이터의 사분위수와 이상치 표현       |
| 에러바 그래프 | `plt.errorbar()`     | 데이터의 오차 범위를 함께 시각화      |
| 이미지 출력   | `plt.imshow()`       | 2차원 배열을 이미지로 표현            |
| 채워진 영역   | `plt.fill_between()` | 두 곡선 사이 영역을 색으로 채움       |

## 그래프 꾸미기
| 함수                        | 설명                                      |
|-----------------------------|-------------------------------------------|
| `plt.title("제목")`         | 그래프 제목 설정                          |
| `plt.xlabel("X축 이름")`    | X축 라벨 설정                             |
| `plt.ylabel("Y축 이름")`    | Y축 라벨 설정                             |
| `plt.grid(True)`            | 격자선(그리드) 표시                        |
| `plt.legend()`              | 범례(legend) 표시                         |
| `plt.xlim([xmin, xmax])`    | X축 범위 설정                             |
| `plt.ylim([ymin, ymax])`    | Y축 범위 설정                             |
| `plt.xticks([리스트])`      | X축 눈금 위치 및 값 설정                  |
| `plt.yticks([리스트])`      | Y축 눈금 위치 및 값 설정                  |
| `plt.text(x, y, "내용")`    | 지정된 위치에 텍스트 추가                 |
| `plt.annotate()`            | 화살표와 텍스트로 특정 지점 강조          |
| `plt.figure(figsize=(w,h))` | 그래프 크기 조절 (단위: 인치)             |
| `plt.subplots()`            | 복수 그래프를 그릴 때 Figure, Axes 객체 생성 |
| `plt.tight_layout()`        | 겹치지 않도록 자동 여백 조정              |
| `plt.savefig("파일명.png")` | 그래프를 이미지 파일로 저장               |

## Matplotlib 기본 사용법 예제

### 1. 기본 선 그래프 그리기
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.title("기본 선 그래프")
plt.xlabel("X축")
plt.ylabel("Y축")
plt.grid(True)
plt.show()
```

## 막대 그래프
```python
import matplotlib.pyplot as plt

labels = ['A', 'B', 'C', 'D']
values = [10, 20, 15, 25]

plt.bar(labels, values)
plt.title("막대 그래프")
plt.xlabel("항목")
plt.ylabel("값")
plt.show()
```

## 산점도 
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [5, 3, 9, 1, 6]

plt.scatter(x, y)
plt.title("산점도")
plt.xlabel("X 값")
plt.ylabel("Y 값")
plt.grid(True)
plt.show()
```

## 여러 그래프 그리기
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y1 = [1, 4, 9, 16, 25]
y2 = [25, 16, 9, 4, 1]

plt.subplot(1, 2, 1)
plt.plot(x, y1)
plt.title("y = x²")

plt.subplot(1, 2, 2)
plt.plot(x, y2)
plt.title("반전된 y")

plt.tight_layout()
plt.show()
```

# 자율주행에서 Matplotlib 활용
- 자율주행에서는 센서(라이다, 카메라, GPS 등)로부터 수집한 공간 정보, 차량 위치, 장애물, 경로 등을 시각화
- 실시간 주행 정보나 알고리즘 결과를 시각적으로 확인하고 디버깅하는 데 효과적

## 주로 사용하는 그래프
- 산점도: 장애물, 차량 위치 표현
- 선 그래프: 경로(Path) 시각화
- 벡터 시각화: 진행 방향, 속도 벡터
- 2D 이미지 출력: 카메라 영상, 마스크 출력

## 차량과 장애물 위치 시각화
```python
import matplotlib.pyplot as plt

# 차량 위치
car_position = (5, 5)

# 장애물 위치
obstacles = [(3, 4), (7, 2), (6, 8)]

# 시각화
plt.figure(figsize=(6, 6))
plt.scatter(*car_position, color='blue', label='차량')
for obs in obstacles:
    plt.scatter(*obs, color='red', label='장애물')

plt.xlim(0, 10)
plt.ylim(0, 10)
plt.grid(True)
plt.legend()
plt.title("자율주행 차량 및 장애물 위치")
plt.xlabel("X 좌표")
plt.ylabel("Y 좌표")
plt.show()
```

## 경로 시각화
```python
import matplotlib.pyplot as plt

# 경로 좌표
path_x = [1, 2, 3, 4, 5, 6]
path_y = [1, 2, 2, 3, 4, 5]

# 시각화
plt.plot(path_x, path_y, marker='o', linestyle='-', color='green', label='경로')
plt.title("자율주행 경로 시각화")
plt.xlabel("X 좌표")
plt.ylabel("Y 좌표")
plt.grid(True)
plt.legend()
plt.show()
```

## 카메라 이미지 출력
```python
import matplotlib.pyplot as plt
import numpy as np

# 예시 이미지: 2차원 배열 (흑백 이미지)
image = np.random.rand(100, 100)

plt.imshow(image, cmap='gray')
plt.title("카메라 입력 이미지")
plt.axis('off')
plt.show()
```























