# 🐍 Python 핵심 노트

> Python 공부 중 반드시 기억해야 할 핵심 개념만 정리합니다.

---

## 1. `print()` — 출력하기

⭐ `print()`는 값을 화면에 출력할 때 사용한다.

```python
name = "철수"
print(name)
```

결과:

```text
철수
```

### 문자열과 변수의 차이

```python
name = "철수"

print("name")  # 글자 그대로 name 출력
print(name)    # 변수 안에 저장된 철수 출력
```

---

## 2. `input()` — 입력받기

⭐ `input()`은 사용자가 키보드로 값을 입력할 때 사용한다.

```python
name = input("이름을 입력하세요: ")
print(name)
```

### ⭐ 매우 중요

`input()`으로 입력받은 값은 **항상 `str`(문자열)** 이다.

숫자를 입력해도 문자열로 들어온다.

```python
age = input("나이: ")
```

`20`을 입력해도:

```text
"20" → str
```

---

## 3. 자료형 — `int`, `str`, `bool`

### `int`

정수를 저장하는 자료형.

```python
age = 20
page = 15
```

---

### `str`

문자열을 저장하는 자료형.

```python
name = "철수"
title = "파이썬 매뉴얼"
```

따옴표가 붙은 `"10"`은 숫자처럼 보여도 `str`이다.

```python
number1 = 10      # int
number2 = "10"    # str
```

---

### `bool`

참 또는 거짓을 저장하는 자료형.

```python
is_open = True
is_closed = False
```

---

## 4. 형 변환

⭐ 자료형을 다른 자료형으로 바꾸는 것을 **형 변환**이라고 한다.

문자열 `"10"`을 정수 `10`으로 바꾸려면:

```python
number = int("10")
```

### ⭐ `input()`과 `int()` 같이 사용하기

`input()`은 값을 `str`로 받기 때문에 숫자로 계산하려면 `int()`로 변환한다.

```python
age = int(input("나이: "))
```

흐름:

```text
사용자가 20 입력
        ↓
input()
        ↓
"20" (str)
        ↓
int()
        ↓
20 (int)
```

⭐ **숫자로 사용할 입력값은 저장할 때부터 `int(input())`로 변환해두면 편하다.**

```python
page = int(input("페이지: "))
```

---

## 5. `dict` — 딕셔너리

⭐ 딕셔너리는 여러 값을 **`"key": value`** 구조로 저장할 수 있다.

```python
manual = {
    "title": "파이썬 매뉴얼",
    "page": 10,
    "content": "변수와 자료형을 설명한다."
}
```

구조:

```text
key          value

"title"   → "파이썬 매뉴얼"
"page"    → 10
"content" → "변수와 자료형을 설명한다."
```

---

## 6. 딕셔너리에 변수 넣기

⭐ 딕셔너리의 `value` 자리에는 변수를 넣을 수도 있다.

```python
title = input("매뉴얼 제목: ")
page = int(input("페이지: "))
content = input("내용: ")

manual_data = {
    "title": title,
    "page": page,
    "content": content
}
```

예를 들어 사용자가 다음과 같이 입력하면:

```text
매뉴얼 제목: 엘리베이터 안전 매뉴얼
페이지: 15
내용: 운행 전 브레이크를 점검한다.
```

딕셔너리는 다음과 같은 데이터를 가지게 된다.

```python
{
    "title": "엘리베이터 안전 매뉴얼",
    "page": 15,
    "content": "운행 전 브레이크를 점검한다."
}
```

---

## 7. 딕셔너리에서 값 꺼내기

⭐ 딕셔너리에서 값을 꺼낼 때는 **`[]`**를 사용한다.

기본 형태:

```text
딕셔너리["key"]
```

예시:

```python
print(manual_data["title"])
print(manual_data["page"])
print(manual_data["content"])
```

### ⭐ `()`와 `[]` 헷갈리지 않기

```text
()       → 함수 실행
["key"]  → 딕셔너리에서 값 꺼내기
```

예:

```python
print("안녕")               # 함수 실행
manual_data["title"]        # 딕셔너리 값 꺼내기
```

---

## 8. 괄호 닫기

⭐ 함수를 여러 개 겹쳐 사용하면 **연 괄호만큼 닫아야 한다.**

```python
page = int(input("페이지: "))
```

구조:

```text
int( input( "페이지: " ) )
 ↑      ↑             ↑ ↑
열기   열기          닫기 닫기
```

---

## 9. `ValueError`

⭐ 값의 형태가 변환하려는 자료형에 맞지 않으면 `ValueError`가 발생할 수 있다.

정상:

```python
number = int("15")
```

`"15"`는 정수 `15`로 변환할 수 있다.

오류:

```python
number = int("hello")
```

`"hello"`는 정수로 바꿀 수 없기 때문에 `ValueError`가 발생한다.

---

# 💻 Day 01 최종 실습

## 매뉴얼 데이터 입력받아 딕셔너리로 저장하기

```python
title = input("매뉴얼 제목: ")
page = int(input("페이지: "))
content = input("내용: ")

manual_data = {
    "title": title,
    "page": page,
    "content": content
}

print(manual_data["title"])
print(manual_data["page"])
print(manual_data["content"])
```

---

# 🧠 Day 01 이것만은 기억하기

1. `print()` → 출력한다.
2. `input()` → 사용자에게 입력받는다.
3. `input()`의 결과는 항상 `str`이다.
4. 숫자로 계산하려면 `int()`로 변환한다.
5. 딕셔너리 → `"key": value`
6. 딕셔너리 값 꺼내기 → `딕셔너리["key"]`
7. `()`와 `[]`를 구분한다.
8. 숫자가 아닌 문자열을 `int()`로 바꾸면 `ValueError`가 발생할 수 있다.
