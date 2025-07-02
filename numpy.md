# Numpy란?
- NumPy는 **Numerical Python(수치 연산용 파이썬)**의 줄임말로,
**다차원 배열(ndarray)**을 지원하며 고속 수치 계산을 가능하게 해주는 파이썬 라이브러리
- 수학, 과학, 머신러닝, 데이터 분석 등에서 널리 사용

# Nunpy를 사용해야 하는 이유
- 파이썬에서는 배열의 역할을 하는 리스트가 있지만, 처리 속도가 느림
- NumPy는 기존 Python 리스트보다 최대 50배 빠른 배열 객체를 제공하는 것을 목표로 함
- NumPy의 배열 객체는 ndarray라고 불리며 작업을 쉽게 하는 도구를 제공

# NumPy가 리스트보다 빠른 이유
- NumPy 배열은 리스트 달리 메모리의 한 연속된 위치에 저장되므로 프로세스가 매우 효율적으로 접근하고 조작됨
- 이런 동을 컴퓨터 과학에서는 참조 지역성이라고 합니다.
- NumPy는 최신 CPU 아키텍처에 최적화되어 있음

## 

| 항목               | 보완 추천 이유                                      |
|--------------------|------------------------------------------------------|
| `dtype`            | 데이터 타입 명시/변환은 중요 기본기                 |
| `np.random`        | 머신러닝, 통계 시뮬레이션 등에서 자주 사용          |
| 조건 필터링 (`np.where`) | 배열 조건 추출에서 자주 사용됨               |
| `axis` 통계        | 평균/최댓값을 축 기준으로 자주 계산함              |
| 배열 합치기        | 다양한 데이터 전처리 상황에서 필수                  |
| boolean indexing   | 필터링 효율을 크게 높여주는 핵심 문법              |


## Numpy 설치 및 버전 확인 
```python
C:\Users\Your Name>pip install numpy
print(np.__version__) 
```

## 배열 생성 예시
```python
import numpy as np

# 1차원 배열 생성
a = np.array([1, 2, 3])

# 2차원 배열 생성
b = np.array([[1, 2], [3, 4]])

# 특정 값으로 채운 배열
zeros = np.zeros((2, 3))     # 0으로 채운 2x3 배열
ones = np.ones((3,))         # 1로 채운 1차원 배열
arange = np.arange(0, 10, 2) # 0부터 10까지 2 간격
linspace = np.linspace(0, 1, 5)  # 0과 1 사이를 5등분

print(a.shape)     # 배열의 형태
print(a.ndim)      # 차원 수
print(a.dtype)     # 데이터 타입
```

## 배열간 연산
```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

print("덧셈:", a + b)      # [5 7 9]
print("뺄셈:", a - b)      # [-3 -3 -3]
print("곱셈:", a * b)      # [4 10 18]
print("나눗셈:", a / b)    # [0.25 0.4 0.5]
```

## 스칼라 연산
```python
arr = np.array([1, 2, 3, 4])

print("곱하기 2:", arr * 2)   # [2 4 6 8]
print("더하기 10:", arr + 10) # [11 12 13 14]
```

## 행렬 연산
```python
a = np.array([[1, 2],
              [3, 4]])

b = np.array([[5, 6],
              [7, 8]])

print("행렬 곱:\n", np.dot(a, b))
```

## 1차원 배열 인덱싱
```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
print(arr[2] + arr[3])
```

## 2차원 배열 인덱싱
```python
arr = np.array([[1,2,3,4,5], [6,7,8,9,10]])

print('2nd element on 1st row: ', arr[0, 1])
print('5th element on 2nd row: ', arr[1, 4])
```

## 3차원 배열 인덱싱
```python
import numpy as np

arr = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])

print(arr[0, 1, 2])
```

## 1차원 배열 슬라이싱
```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6, 7])

print(arr[1:5])
print(arr[4:])
print(arr[-3:-1])
print(arr[1:5:2]) # 인덱스 1부터 4까지, 2칸씩 건너뜀
print(arr[::2]) # 짝수 인덱스를 가진 요소들만 출력
```

## 2차원 배열 슬라이싱
```python
import numpy as np

arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])

print(arr[1, 1:4]) # 두 번째행 인덱스 1,2,3
print(arr[0:2, 2]) # 첫 번쨰행~두 번째행 각 행에서 2열 
```

## 배열 형태 변경
```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6])

reshaped = arr.reshape(2, 3)
print(reshaped)
```

## 배열 펼치기
```python
arr = np.array([[1, 2, 3],
                [4, 5, 6]])

flattened = arr.flatten()
print(flattened)
```

## 통계 함수
```python
arr = np.array([1, 2, 3, 4, 5])

print("합계:", arr.sum())         # 15
print("평균:", arr.mean())        # 3.0
print("최댓값:", arr.max())       # 5
print("최솟값:", arr.min())       # 1
print("표준편차:", arr.std())     # 1.4142...
```

## 축 지정 통계
```python
arr = np.array([[1, 2, 3],
                [4, 5, 6]])

print("행 기준 합:", arr.sum(axis=1))   # [ 6 15 ]
print("열 기준 합:", arr.sum(axis=0))   # [5 7 9]
```









