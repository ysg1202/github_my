# Python에서 주의해야 할 점들
## 문법 관련 주의사항
### 들여쓰기 (Indentation)
Python은 들여쓰기로 코드 블록을 구분합니다
탭과 스페이스를 섞어 쓰면 안 됩니다
일관성 있게 스페이스 4개 또는 탭 사용

![image](https://github.com/user-attachments/assets/9bc9ee09-ef12-4eb6-978c-368622643f0e)



### 대소문자 구분
Python은 대소문자를 구분합니다
Print와 print는 완전히 다른 것

![image](https://github.com/user-attachments/assets/6cc2feaa-d6e6-4689-9c12-4565c367d5dd)



## 변수와 데이터 타입
### 변수명 규칙
숫자로 시작할 수 없음
특수문자 사용 불가 (밑줄 _ 제외)
예약어 사용 불가

![image](https://github.com/user-attachments/assets/ee1d632d-4e1b-42ba-97ce-637ef5064e0a)




### 문자열 처리 주의사항
따옴표 주의

![image](https://github.com/user-attachments/assets/3d608388-7275-4d7b-b667-e05e5a6941ac)

문자열과 숫자 연산

![image](https://github.com/user-attachments/assets/10047445-7c45-4550-86bb-ebceae407e96)

## 리스트와 인덱스
### 인덱스 범위 주의
my_list = [1, 2, 3]
print(my_list[3])  # 에러! 인덱스 범위 초과
print(my_list[2])  # 올바름 (마지막 요소)
print(my_list[-1]) # 올바름 (뒤에서 첫 번째)

리스트 복사 주의
list1 = [1, 2, 3]
list2 = list1        # 참조 복사 (같은 메모리)
list2.append(4)
print(list1)         # [1, 2, 3, 4] - 원본도 변경됨!

# 올바른 복사 방법
list2 = list1.copy()  # 또는 list1[:]

반복문과 조건문
무한 루프 주의
# 위험한 코드
while True:
    print("무한 루프!")  # Ctrl+C로 중단해야 함

# 안전한 코드
count = 0
while count < 10:
    print(f"카운트: {count}")
    count += 1  # 카운터 증가 잊지 말기!

조건문에서 할당 연산자 실수
x = 5
if x = 10:  # 에러! 할당 연산자 사용
    print("x는 10")

if x == 10:  # 올바름! 비교 연산자 사용
    print("x는 10")




