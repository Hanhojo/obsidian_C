####  값을 변경할 수 없는 변수를 선언할 때 const를 사용한다. ####
___

**(1) const 데이터형 * 변수;**
 const가 데이터형 앞에 있으면 포인터가 가리키는 변수의 값을 변경할 수 없다.

```c
int a = 10, b = 20;
const int *p1 = &a; // p1는 a에 읽기 전용으로 접근한다.
printf("*p1 = %d\n", *p1); // p1으로 a를 읽어올 수 있다.
*p1 = 100; // p1이 가리키는 변수를 변경할 수 없다.
```

읽기 전용 포인터는 선언 시 **널 포인터**로 초기화하고, 원하는 시점에 특정 변수의 주소를 저장하고 사용할 수 있다. 
```c
const int *p1 = NULL; // p1는 가리키는 변수가 없다.
int sum = 12345;

p1 = &sum; // 원하는 시점에 변수의 주소를 저장한다.
```

**(2) 데이터형 * const 변수;**
포인터가 자신의 값을 변경할수 없고, 특정 변수의 전용 포인터가 된다.
```c
int *const p2 = &a; // p2는 a의 전용 포인터이다. 즉 a에 접근하는 용도로만 사용된다.
p2 = &b; // p2는 다른 변수를 가리킬 수 없다. 
```

특정 변수 전용 포인터는 선언 시 초기화 하지 않으면 그 이후에 주소를 저장할 수 없으므로 선언 시 반드시 초기화 해야 한다.
```c
int *const p2; // 초기화 하지 않으면 p2는 쓰레기값이고 나중에 주소를 저장할 수도 없다.
```

**(3) const 데이터형 * const 변수;**
읽기 전용 포인터이면서 특정 변수 전용 포인터가 된다.
이 포인터는 반드시 초기화 해야 한다.
```c
const int * const p3 = &a; // p3는 a전용 포인터이면서 a에 읽기 전용으로 접근한다.
*p3 = 100; // p3가 가리키는 변수를 변경할 수 없다.
p3 = &b; // p3는 다른 변수를 가릴킬 수 없다.
```
