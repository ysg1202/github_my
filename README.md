# AI 학습 정리

## 1. About GitHub, Markdown, Colab
- [GitHub 사용법](#github-사용법)
- [Markdown 문법](#markdown-문법)  
- [Colab 기초](#colab-기초)

- ## GitHub 사용법

### ✅ GitHub 계정 만드는 순서 (2025년 기준)

1. **웹 브라우저 열기**
   크롬(Chrome), 엣지(Edge), 사파리(Safari) 중 편한 걸 사용하세요.

2. **GitHub 웹사이트 접속**
   주소창에 아래 주소를 입력하고 Enter 누르세요: https://github.com

3. **회원가입 시작하기**
   화면 오른쪽 위 또는 중간에 있는 Sign up 버튼 클릭

4. **이메일 주소 입력**
   평소 자주 사용하는 이메일을 입력

5. **비밀번호 만들기**
   영어 대문자, 소문자, 숫자, 특수문자를 섞어 안전하게!
   예시: Git1234!hub

6. **사용자 이름(Username) 정하기**
   나만의 고유한 이름을 지어요 (다른 사람이 쓰고 있으면 불가)
   - 예시: jetsunmom, sungsookjang66 등
   - 영어, 숫자, 하이픈(-) 가능 (띄어쓰기 ❌)

### ✅ Repository 만들기 순서

1. **GitHub에 로그인 후 New Repository 클릭**
2. ![new](https://github.com/user-attachments/assets/3481a680-f677-403b-be8c-1fe59d5aa7cb)

3. **Repository 이름 입력**
4. **Public/Private 선택**
5. **README.md 파일 생성 체크**
6. **Create repository 버튼 클릭**
   
![create_repository](https://github.com/user-attachments/assets/8c2eb16b-8dfc-465a-88cd-d35770d12df0)

## Markdown 문법

### 글자 크기 조절
# 제목1  
## 제목2  
### 제목3  
#### 제목4  
##### 제목5  
###### 제목6

### 글자 꾸미기   
**굵게**  
*기울임*  
~~취소선~~  

### 목록 만들기
- 항목1
- 항목2
  -하위항목

### 링크 & 이미지
[내 깃허브 저장소](https://github.com/ysg1202)  
![car](https://github.com/user-attachments/assets/13fbe4e1-160a-48d6-80d4-5e5ec8e24cbe)


### 인용문
> 인용문입니다
>> 중첩 인용 가능

### 코드 
```python
print('hello world')
```
```
pip install matplotlib
sudo apt update
```

### 표 만들기
| 이름 | 나이 | 직업     |
|------|------|---------|
| 영희 | 25   | 디자이너 |
| 철수 | 30   | 개발자   |

## Colab 기초 
![colab1](https://github.com/user-attachments/assets/3d338674-bac3-4dea-9e5c-6a2206f0d5cc)
![colab2](https://github.com/user-attachments/assets/fc8effa0-5550-4368-8131-387e6eb76132)


파일 -> Github에 사본 저장 -> 저장할 repository 선택 후 확인 

## 2. About python3
- [ws3school](https://www.w3schools.com/python/)
- [파이썬 자료](https://docs.google.com/document/d/19VkSDEzg3EgwLROp6Z0-3Bdayx0T_X4vmB3hQZFbOxY/edit?tab=t.0#heading=h.xznvs0glpxkj)
- [Python basic](python3.md)
- [for문 기초 가이드](https://claude.ai/public/artifacts/0ef57f69-96fa-4833-9b40-9ea79b0bd691)
- [클래스 기초 가이드](https://claude.ai/public/artifacts/82c1fb01-030d-4ae3-abde-118676216f64)
- [딕셔너리 기초 가이드](https://claude.ai/public/artifacts/a11af36d-c9fa-4366-9580-379644d1af5d)
- [리스트 기초 가이드](https://claude.ai/public/artifacts/fd98c798-ab20-40a4-8a3b-537503b9849c)
- [딕셔너리 기초 가이드](https://claude.ai/public/artifacts/a11af36d-c9fa-4366-9580-379644d1af5d)

## 3.  data structure / data sciencs

- [데이터 구조 개요](./data_structures.md)
- [Pandas](./pandas.md)
- [Numpy](./numpy.md)
- [Matplotlib](./Matplotlib.md)

## 4. Machine Learning

- [Machine Learning Basic](./ml_basic.md)
- [모델 훈련 및 평가](./ml_test.md)

## 5. OpenCV

- [OpenCV Basic](./OpenCV_basic.md)
- [이미지 처리](./image_test.md)

## 6. CNN(Convolution Neural Network
- [CNN_Basic](./CNN_basic.md)
- [CNN_자율주행 관련 코드](./cnn_test.md)

## 7. Ultralytics
- [Ultralytics_Basic](./Ultralytics_basic.md)
- [YOLOv8](./YOLOv8_test.md)
- [YOLOv12](./YOLOv12_test.md)
  
## 8. TensorRT vs PyTorch 
- [PyTorch_Basic](./PyTorch_basic.md)
- [TensorRT](./TensorRT_test.md)
- [YOLOv12](./YOLOv12_test.md)

## 9. TAO Toolkit on RunPod
- [TAO_사용법](.TAO_install.md)
- [TAO_Toolkit](.TAO_Toolkit.md)

## 10. 칼만필터, CARLA, 경로 알고리즘
- [kalman](.kalman.md)
- [CARLA_simulator](.CARLA.md)

## 11. ADAS & (ADAS TensorRT vs PyTorch)
- [adas_basic](.adas_basic.md)
- [TensorRT vs PyTorch 비교](.vs.md)














