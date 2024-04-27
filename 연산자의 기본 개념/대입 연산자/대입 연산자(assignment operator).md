#### 좌변에 있는 변수에 우변의 값을 지정한다. ####

____
## 대입 연산자 특징 ##

- 대입 연산자의 **좌변을 l - value 우변을 r - value**라고 한다.
- l - value는 변수 r - value 값이 있는 수식이 올 수 있다.
- 대입 연산식의 값을 다른 수식에 이용할 수 있다.

```c
int price = 3000, amount = 2;
int total = 0;
int count = 0;

price = 1000; // price 변수에 리터럴 상수의 값을 저장한다.
total = amount * price; // total 변수에 amount * price 연산의 결과값을 저장한다.
count = printf("hello"); // count 변수에 printf 함수의 리턴값을 지정한다.
```

## 대입 연산의 결과값 예제 ##

```c
#include <stdio.h>

int main(void)
{
	int a = 0;
	double b = 0;
	int c = 0;

	a = 123; // a에 123 저장
	printf("a = %d\n", a);
	printf("a = %d\n", a = 456); //a에 456 저장 후 a의 값이 수식의 값
	printf("b = %f\n", b = a + 0.5); // b에 a + 0.5 저장 후 b의 값이 수식의 값
	printf("c = %d\n", c = printf("ABC\n"));
	// printf 함수의 러턴값을 c에 저장하고 c의 값이 수식의 값

	return 0;
}

// a = 123 a = 456 b = 456.500000 ABC c = (a, b, c, \n)총4개
```