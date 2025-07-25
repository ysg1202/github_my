# Numpy란?
- NumPy는 Numerical Python(수치 연산용 파이썬)의 줄임말로,다차원 배열(ndarray)을 지원하며 고속 수치 계산을 가능하게 해주는 파이썬 라이브러리
- 수학, 과학, 머신러닝, 데이터 분석 등에서 널리 사용

# Nunpy를 사용해야 하는 이유
- 파이썬에서는 배열의 역할을 하는 리스트가 있지만, 처리 속도가 느림
- NumPy는 기존 Python 리스트보다 최대 50배 빠른 배열 객체를 제공하는 것을 목표로 함
- NumPy의 배열 객체는 ndarray라고 불리며 작업을 쉽게 하는 도구를 제공

# NumPy가 리스트보다 빠른 이유
- NumPy 배열은 리스트 달리 메모리의 한 연속된 위치에 저장되므로 프로세스가 매우 효율적으로 접근하고 조작됨
- 이런 동을 컴퓨터 과학에서는 참조 지역성이라고 합니다.
- NumPy는 최신 CPU 아키텍처에 최적화되어 있음

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

## 자율주행 코드에 쓰이는 Numpy 명령어
| 명령어                    | 용도 및 설명                                                 |
|---------------------------|--------------------------------------------------------------|
| `np.array()`              | 센서 데이터나 좌표 데이터를 배열로 표현할 때 사용            |
| `np.linalg.norm()`        | 두 점 사이 거리 계산 (유클리드 거리 등)                      |
| `np.dot()`                | 방향 벡터, 속도 벡터의 내적 연산에 사용                      |
| `np.cross()`              | 3D 방향 벡터의 외적 계산에 사용 (방향 판단 등)              |
| `np.clip()`               | 제어 명령 제한 (예: 속도 - 최소/최대 범위 설정)             |
| `np.mean()` / `np.std()` | 센서 노이즈 평균 및 표준편차 계산                            |
| `np.argmax()`             | 가장 높은 신뢰도 또는 확률 값을 가진 인덱스 찾기             |
| `np.where()`              | 조건에 따라 경로 선택, 충돌 감지, 이상치 제거 등에 사용      |
| `np.stack()`              | 여러 센서 데이터를 하나의 배열로 합칠 때                    |
| `np.expand_dims()`        | 차원 추가 (딥러닝 입력 형태 맞출 때 유용)                   |

## Numpy 자율주행 코드 예시
```python
import numpy as np

# 내 차 위치
my_pos = np.array([5.0, 5.0])

# 다른 차 위치
other_pos = np.array([7.0, 8.0])

# 거리 계산
distance = np.linalg.norm(my_pos - other_pos)

# 안전 거리 기준
safe_distance = 4.0

print(f"두 차량 거리: {distance:.2f}m")

if distance < safe_distance:
    print("⚠️ 충돌 위험!")
else:
    print("✅ 안전 거리 유지")
```

## NumPy 사용 시 주의사항

- **파일 이름을 `numpy.py`로 짓지 말 것**
  - 파이썬이 진짜 NumPy 모듈이 아닌, 사용자 파일을 불러와 오류 발생
  - 예: `AttributeError: module 'numpy' has no attribute 'array'`

- **리스트와 ndarray 혼용 주의**
  - `list + ndarray` 같은 연산은 에러 또는 예상치 못한 결과를 발생시킬 수 있음
  - NumPy 연산은 **모두 ndarray 타입**으로 통일하는 것이 안정적

- **reshape 시 전체 원소 개수 일치 필수**
  - `reshape(a, b)`는 `a * b == 전체 원소 개수` 조건을 만족해야 함

- **broadcasting 규칙 이해 필요**
  - 배열 모양이 다를 때 자동 확장되지만, 규칙을 벗어나면 오류 발생

- **정수 나눗셈 결과 확인**
  - 파이썬 기본 나눗셈 `/`은 float 결과, `//`은 정수 나눗셈임

- **고정된 dtype 주의**
  - int 배열에 float을 넣으면 자동 변환 안 됨 → dtype 미스매치로 에러 가능

- **in-place 연산 시 원본 손상 가능**
  - `a += b` 같은 연산은 원본을 바꾸므로 주의 (복사본 필요 시 `.copy()` 사용)



- [넘파이_shape](https://claude.ai/public/artifacts/e9e50b3f-cd6a-4a15-8858-3a84f0b4bb36)
- [넘파이_index](https://claude.ai/public/artifacts/6accf154-ceb5-470a-b2e2-543df2d49b4a)
- [넘파이_기초](https://claude.ai/public/artifacts/0594c0ae-662a-4c1b-b29f-16dc69aff934)
- [넘파이_배열 인터랙티브](https://claude.ai/public/artifacts/fdea1f0a-439f-47d8-b954-956f34693a2e)
- [넘파이_브로드캐스팅](https://claude.ai/public/artifacts/1e559e5e-1a60-4c8f-8971-69d9d00581ae)





