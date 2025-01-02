# 네줄리뷰(Four Lines Review)
**2024.01.02** 

## Fact(오늘 무엇을 하였나요?)
- 오늘도 어제와 마찬가지로 파이썬 기초를 한 바꾸 돌았습니다.
- 실습은 코랩에서 진행했어요.
- 조건문과 반복문(for문, while문)에 대해서 배웠습니다.

## Discovery(뭐를 알아냈을까요?)
- 조건문은 if 문만 있는 줄 알았는데 럴수 럴수 이럴수가 **match~case** 문이 있었습니다!(버전 3.10 이상에서 도입되었다고 하네요~)

## Lesson Learned(뭐를 배웠을까요?)
- if문과 match~case문이 차이가 뭔지 찾아봤는데요(chatgpt에게 물어봤어요).
    ![chatgptimage](https://github.com/user-attachments/assets/b3b4475d-07c1-4891-97d0-ff7bbe89e215)
- 아~ 가독성이 좋아진다고 합니다. 그럼 성능 차이는 없을까요?(차이는 미미하다고 합니다)
- 아래는 match~case문의 예시입니다.

    ~~~python
    def describe_value(value):
        # match문으로 value에 대해 패턴 매칭 시작
        match value:
            # 값이 정확히 1일 경우
            case 1:
                print("The value is one.")  # "값이 1입니다."
            
            # 값이 정확히 2일 경우
            case 2:
                print("The value is two.")  # "값이 2입니다."
            
            # 값이 특정 범위(3~5) 안에 있을 경우
            case _ if 3 <= value <= 5:
                print("The value is between three and five.")  # "값이 3에서 5 사이입니다."
            
            # 튜플 형태의 패턴 매칭 (예: (x, y))
            case (x, y) if x > 0 and y > 0:
                print(f"Tuple with positive values: ({x}, {y})")  # 예: "(3, 4)" 출력
            
            # 리스트 형태의 패턴 매칭 (길이가 3인 경우)
            case [a, b, c] if a < b < c:
                print(f"List in increasing order: {a}, {b}, {c}")  # 예: "[1, 2, 3]" 출력
            
            # 값이 "exit" 문자열일 경우
            case "exit":
                print("Exiting program...")  # "프로그램을 종료합니다."
            
            # 모든 다른 값에 대한 기본 처리 (_는 와일드카드로 모든 값과 매칭)
            case _:
                print("Unknown value.")  # "알 수 없는 값입니다.
    ~~~

- case문의 장점은 튜플(x,y)이나 리스트[a,b,c] 형태를 매칭하여 복잡한 구조를 처리가 가능합니다.
- "_" 언더바는 매칭되지 않은 모든 값을 처리하기 위해 있어요~

## Declaration(알게된 걸로 뭐를 하고 싶은가요?)
- 앞으로 복잡한 조건들은 match~case 문을 이용하여 가독성을 높여봐야겠습니다!