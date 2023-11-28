# dart

나도 한다 Dart + Flutter

## 참고

http://mobilelab.khu.ac.kr/wordpress/beprogrammer/

## 요약

### main()

```dart
void main() {
    print("Hello, World!");
    print('Hello, World!');
}
```

### Comments

```dart
// 한 줄 주석
/*
    여러 줄 주석
    우히히우히히
    우히히우히히
*/
```

### Built-in Number Types

```dart
/*
    - Dart의 숫자형 데이터 타입은 클래스 기반의 객체
    - Dart의 숫자형 데이터 타입이 갖는 최소/최대값은 -2^63 ~ 2^63 - 1
        - Dart -> JavaScript를 할 경우 -2^53 ~ 2^53 - 1
*/
void main() {
    int i = 1;
    double d = 3.6;
    bool b = true;

    print(i); // 1
    print(d); // 3.6
    print(b); // true
}
```

### Type Inference

```dart
// Dart 언어가 스스로 타입을 유추하는 기능
void main() {
    var i = 1;
    var d = 3.6;
    var b = true;

    print(i); // 1
    print(d); // 3.6
    print(b); // true
}
```

- 이미 값을 저장하고 있는 `var` 타입 변수에 다른 타입의 값을 저장하면 오류 발생

```dart
// Dynamic 타입으로 변수 선언
void main() {
    dynamic i = 1;
    dynamic d = 3.6;

    i = 7.2;
    d = 2;

    print(i); // 7.2
    print(d); // 2
}
```

### final과 const

```dart
/*
    - 두 타입 모두 한 번 값을 대입하면 변경할 수 없다.
    - final
        - 실행 중 값이 결정된다.
    - const
        - 컴파일 시에 값이 결정된다.
*/
```

### Built-in Data Collection Types

```dart
void main() {
    var myList = [1, 2, 3]; // List
    var mySet = {'C++', 'Python', 'Java', 'JavaScript'}; // Set
    var myMap = {1: 'Kotlin', 2: 'TypeScript'}; // Map

    print(myList); // [1, 2, 3]
    print(mySet); // {C++, Python, Java, JavaScript}
    print(myMap); // {1: Kotlin, 2: TypeScript}
}
```

- List
  - 동일 타입의 데이터를 여러 개 저장할 수 있다.
  - 저장한 순서를 유지한다.
- Set
  - 저장된 데이터에 중복된 값이 없도록 한다.
  - 순서는 의미가 없다.
- Map
  - `Key - Value` 꼴로 저장하며, Key는 중복될 수 없다.

### Conditional Statement

```dart
// C++과 거의 똑같지만, switch문에서 fall-through 시 오류가 발생한다.
void main() {
    var i = 1;

    if (i == 1) {
        print("1");
    } else if (i == 2) {
        print("2");
    } else {
        print("else");
    }
}
```

### Loop Statement

```dart
// for, while, do-while, break, continue
// Collection 타입의 경우 for-in 사용 가능
void main() {
    var myList = [1, 2, 3];

    for (var i = 0; i < 3; ++i) {
        print(myList[i]);
    }

    for (var number in myList) {
        print(number);
    }
}
```

### Function

```dart
void sayHello() {
    print("Hello");
}

void main() {
    sayHello();

    // Anonymous Function
    var a = ((i) => print(i));
    a(5); // 5
}
```
