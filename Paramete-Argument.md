# Paramete-Argument

> Parameter(매개변수)와 Argument(인수)는 Java 프로그래밍 언어에서도 함수(메서드)를 정의하고 호출할 때 사용되는 용어입니다.

Parameter(매개변수)는 메서드 정의(선언)할 때 메서드에 전달되는 값을 받아들이는 변수입니다. 메서드 내에서 이 변수를 사용하여 메서드의 작업을 수행하거나 결과를 반환합니다. 예를 들어, 다음과 같은 메서드가 있다면:

```java
public int addNumbers(int x, int y) {
    return x + y;
}
```
여기서 x와 y는 메서드 addNumbers()의 매개변수(parameter)입니다. 이 메서드를 호출할 때, 인수(arguments)를 전달해야 합니다.

Argument(인수)는 메서드를 호출할 때 전달되는 값입니다. 메서드가 호출될 때, 이 인수들이 메서드의 매개변수에 대응하여 전달됩니다. 이를 통해 메서드가 실행됩니다. 예를 들어, 위의 addNumbers() 메서드를 호출할 때, 다음과 같이 두 개의 인수를 전달할 수 있습니다.

```java

int result = addNumbers(3, 5);
```
이때, 3과 5가 addNumbers() 메서드의 인수(arguments)입니다. 메서드가 호출되면, x 매개변수는 3 값으로 설정되고, y 매개변수는 5 값으로 설정됩니다. 메서드는 8 값을 반환하고, 이 값은 result 변수에 할당됩니다.

따라서, 매개변수(parameter)는 메서드 정의에서 사용되며, 인수(argument)는 메서드 호출에서 사용됩니다. 메서드를 호출할 때는 매개변수와 동일한 순서로 인수를 전달해야 합니다.


***


## 메모리관점
Parameter(매개변수)와 Argument(인수)는 메모리 관점에서도 다른 개념입니다.

Parameter(매개변수)는 메서드의 스택 메모리에 할당됩니다. 메서드가 호출될 때, 매개변수의 개수에 따라 스택 메모리에 공간이 할당되고, 메서드 내에서 매개변수에 접근할 수 있습니다. 매개변수는 메서드 호출 시에 전달되는 값을 저장하는 역할을 합니다.

Argument(인수)는 메서드를 호출할 때 전달되는 값이며, 매개변수와 대응됩니다. 호출된 메서드는 인수의 값에 접근하여 작업을 수행합니다. 인수는 호출 시에 메모리에 할당됩니다. 일반적으로 인수는 스택 메모리에 저장됩니다.

즉, 매개변수와 인수는 모두 메모리에 저장되는 값이지만, 매개변수는 메서드 정의 시에 선언되고, 호출 시에 전달되는 값을 저장하는 변수이며, 인수는 메서드 호출 시에 전달되는 실제 값입니다. 두 개념은 혼용되어 사용되지만, 서로 다른 의미와 역할을 가지고 있습니다.



***

## 아규먼트의 할당

추가 [콜바이벨류](https://bcp0109.tistory.com/360)


일반적으로 Java에서 메서드를 호출할 때, Argument(인수)는 호출 스택 메모리의 매개변수(Parameter) 슬롯에 복사됩니다. 따라서 메서드가 호출되면, 인수의 값이 스택 메모리의 매개변수 슬롯에 복사되며, 이후에 메서드 내에서 매개변수로 사용됩니다.

이때, 인수의 값이 복사되기 때문에, 메서드 내에서 매개변수 값을 변경하더라도, 호출자(caller)에게는 영향을 미치지 않습니다. 예를 들어, 다음과 같은 메서드가 있다고 가정해보겠습니다.

```java
public void increment(int x) {
    x++;
    System.out.println("x: " + x);
}
```
이 메서드는 호출될 때, 전달된 인수 x 값을 1 증가시키고, 그 값을 출력합니다. 메서드를 호출할 때, 다음과 같이 인수를 전달할 수 있습니다.

```java
int num = 10;
increment(num);
System.out.println("num: " + num);
```
이때, num 변수에는 10이 저장되어 있습니다. increment() 메서드를 호출할 때, num 변수를 전달하면, 호출 스택 메모리에 x 매개변수 슬롯이 생성되고, num 값이 복사됩니다. 따라서 increment() 메서드 내에서 x 값이 증가해도, num 변수에는 아무런 영향을 미치지 않습니다. 따라서 위 코드를 실행하면, 다음과 같은 결과가 출력됩니다.

```
x: 11
num: 10
```
즉, 인수는 메서드를 호출할 때 메모리에 할당되며, 매개변수 슬롯에 복사됩니다. 이후에 메서드 내에서 매개변수로 사용됩니다.
