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





