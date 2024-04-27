#### 감소된 변수 a의 값 (전위 감소 연산자)####

____
## 전위 감소 연산자 예제 ##

```c
#include <stdio.h>

int main(void) 
{
	int a  = 5;
	int b  = 5;

	int pre_decrement = --a; // 전위 감소 연산자 사용

	printf("After --a: a = %d, pre_decrement = %d\n", a,pre_decrement);

	return 0;
}

	//출력 결과//
	//After = --a: a = 4, pre_decrement = 4//
```