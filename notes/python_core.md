# Python 핵심 노트

## 1. input()과 int()

⭐ `input()`은 입력받은 값을 항상 `str`로 반환한다.

숫자로 계산하려면 `int()`로 변환한다.

```python
age = int(input("나이: "))
2. Dictionary
⭐ 딕셔너리는 "key": value 구조다.
manual_data = {
    "title": manual,
    "page": page
}
⭐ 딕셔너리에서 값을 꺼낼 때는 []를 사용한다.
print(manual_data["title"])
() = 함수 실행
["key"] = 딕셔너리에서 값 꺼내기
3. ValueError
⭐ int()로 숫자가 아닌 문자열을 변환하려고 하면 ValueError가 발생할 수 있다.
int("15")    # 정상
int("hello") # ValueError
