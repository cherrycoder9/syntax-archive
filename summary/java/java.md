# 자바 핵심 문법 요약

## 1. 클래스와 객체

```java
public class Person {
    String name;
    int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public void sayHello() {
        System.out.println("Hello, my name is " + name);
    }
}

// 객체 생성 및 사용
Person p = new Person("John", 30);
p.sayHello();
```

## 2. 상속과 인터페이스

```java
// 상속
public class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Woof");
    }
}

// 인터페이스
public interface Drawable {
    void draw();
}

public class Circle implements Drawable {
    public void draw() {
        System.out.println("Drawing a circle");
    }
}
```

## 3. 접근 제어자와 키워드

- `public`, `private`, `protected`
- `static`, `final`

## 4. 예외 처리

```java
try {
    // 예외가 발생할 수 있는 코드
} catch (Exception e) {
    // 예외 처리
} finally {
    // 항상 실행되는 코드
}
```

## 5. 컬렉션 프레임워크

```java
// ArrayList
ArrayList<String> list = new ArrayList<>();
list.add("Apple");

// HashMap
HashMap<String, Integer> map = new HashMap<>();
map.put("Apple", 1);
```

## 6. 제네릭

```java
public class Box<T> {
    private T t;
    public void set(T t) { this.t = t; }
    public T get() { return t; }
}
```

## 7. 람다 표현식과 스트림

```java
// 람다 표현식
list.forEach(item -> System.out.println(item));

// 스트림
int sum = numbers.stream()
                 .filter(n -> n % 2 == 0)
                 .mapToInt(n -> n)
                 .sum();
```

## 8. 어노테이션

```java
@Override
@Deprecated
@SuppressWarnings("unchecked")
```

## 9. 파일 입출력

```java
try (BufferedReader br = new BufferedReader(new FileReader("file.txt"))) {
    String line;
    while ((line = br.readLine()) != null) {
        System.out.println(line);
    }
} catch (IOException e) {
    e.printStackTrace();
}
```

## 10. 쓰레드

```java
public class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running");
    }
}

MyThread t = new MyThread();
t.start();
```

## 11. Optional

```java
Optional<String> optional = Optional.ofNullable(nullableString);
String result = optional.orElse("Default Value");
```

## 12. 함수형 인터페이스

```java
@FunctionalInterface
interface MyFunction {
    int apply(int a, int b);
}

MyFunction add = (a, b) -> a + b;
```
