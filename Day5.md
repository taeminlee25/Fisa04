**2024.01.06**
## 사줄리뷰<br>(Four Lines Review)</br>
---
### Fact<br>(오늘 무엇을 하였나요?)</br>
- 오늘은 지난주와 동일하게 파이썬 기초를 한 바꾸 돌았습니다.
- 지난 주차에 이어 함수 사용법과 파일을 읽고 쓰는 방법을 학습했어요.

## Discovery<br>(뭐를 알아냈을까요?)</br>
- 함수 중 저를 시련에 빠트리는 **재귀 함수**를 맞닥뜨렸습니다!
- 재귀 함수란 무엇이냐면 자기가 자기 스스로 부르는 함수 입니다.

> <u>Recursion</u>
> Python also accepts function recursion, which means a defined function can call itself.
 - 그렇다면! 왜 for나 while과 같은 반복문 대신에 재귀함수를 사용하는 걸까요?
 - 레딧에서는 **수학적으로 엘레강스~** 해서 멋있기 때문이라고 합니다(코딩도 중세 귀족처럼 우아하게).

<figure style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/52edb736-2c3b-440a-9148-d9dc6745305e" alt="레딧 코멘트">
</figure>

~~~python

def factorial_recursive(n): # 재귀함수, 간결한게 멋있죠?
    if n == 1:  # 종료 조건
        return 1
    return n * factorial_recursive(n - 1)

print(factorial_recursive(5))

def factorial_iterative(n): # 반복문
    result = 1
    for i in range(1, n + 1):
        result *= i
    return result

print(factorial_iterative(5))  
~~~

- 사실은 둘 다 장단점이 있어 상황에 맞게 사용하면 됩니다.
- 특히 변수가 너무 많아서 겹칠 것 같은 상황에는 재귀함수가 좋습니다.

| **항목**       | **재귀함수**                 | **반복문**            |
|:--------------:|:----------------------------:|:---------------------:|
| **구조**       | 함수 호출로 처리            | `for`, `while` 사용  |
| **메모리**     | 호출 스택 사용              | 메모리 사용 적음      |
| **가독성**     | 간결하고 직관적일 수 있음    | 복잡한 경우 가독성 감소 |
| **성능**       | 호출 오버헤드로 느릴 수 있음 | 일반적으로 더 빠름    |
| **제약**       | 호출 스택 크기 제한          | 제한 없음             |


## Lesson Learned<br>(뭐를 배웠을까요?)</br>
- 재귀함수를 다루면서 함수형 문법에 대해서도 배웠습니다!
- 함수형 문법은 '함수를 중심으로 작성'하는 방식입니다.
- 함수형 문법 중 핵심은 데이터 처리에 filter, map, reduce를 사용하는 것입니다.
- 함수형 문법을 왜 사용하는지는 상태 공유를 피하여 병렬 실행이 안전하기 때문입니다.
- <u>람다 함수</u>도 배웠습니다(filter, map, reduce와 함께 한다면 시너지 백만배!)
- 람다 함수는 **def**로 함수를 만들지 않아도 될 만큼 로직이 간단할 때 사용하면 좋습니다!
- 함수명을 고민하지 않아도 되고 무엇보다 한 줄로 함수를 작성한다니 **간.지.작.살** 입니다.
<figure style='text-align: center;'>
    <img src = 'https://github.com/user-attachments/assets/b686c822-6cb9-47ea-a1a8-12e673024d93' alt='멋져' width='300'>
</figure>

~~~python
def add(x, y): # 일반 함수
    return x + y

lambda x, y: x + y # 람다 함수(멋져...)
~~~
## Declaration<br>(알게된 걸로 뭐를 하고 싶은가요?)</br>
- 얼른 함수형 문법을 익혀 고수처럼 보이는 코딩이 하고 싶어집니다.
- 어서 빨리 병렬 처리를 배워서 병렬 프로그래밍이 하고 싶어집니다.