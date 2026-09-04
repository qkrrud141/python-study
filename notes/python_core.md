# Python 핵심 노트

## 1. input()과 자료형

⭐ `input()`은 입력받은 값을 항상 `str`로 반환한다.

숫자로 계산하려면 `int()`로 변환한다.

```python
age = int(input("나이: "))
```

## 2. Dictionary

⭐ 딕셔너리에서 값을 꺼낼 때는 `딕셔너리["key"]` 형식을 사용한다.

```python
print(manual["title"])
```

## 괄호 규칙

⭐ `int(input("입력: "))`처럼 함수가 겹쳐 있으면 연 괄호 수만큼 닫는다.

```python
number = int(input("숫자: "))
#             ↑      ↑↑
#          input(   닫고 닫고
```
