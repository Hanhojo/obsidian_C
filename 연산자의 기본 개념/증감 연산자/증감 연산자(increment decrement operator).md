#### 증감 연산자는 변수의 값을 1만큼 증가시키거나 감소기키는 [[단항 연산자(unary operator)]]이다. ####

## 증감 연산자의 특징 ##

- 증감 연산자는 피연산자의 앞에 오거나 뒤어 올 수 있다.
- 피연산자의 앞에 사용하는 것을 **전위형(prefix)** 이라고 한다. = 수의 값을 1만큼 증가시킨다.
- 피연산자의 뒤에 사용하는 것을 **후위형(postfix)** 이라고 한다. = 증가 전 변수의 값

### 예제 코드 ###
```c
#include <stdio.h>

int main(void)
{
	int index1 = 0, index2 = 0;
	int current1, current2;
	float x1 = 0.5F, x2 = 0.5F;
	float y1, y2;

	current1 = index1++; // 증가 전의 index1
	printf("index1 = %d, current1 = %d\n", index1, current1);

	current2 = ++index2 // 증가 후의 index2
	printf("index2 = %d, current2 = %d\n", index2, current2);

	y1 = x1++; // 증가 전의 x1
	printf("x1 = %.2f, y1 = %.2f\n", x1. y1);

	y2 = ++x2; // 증가 후의 x2
	printf("x2 = %.2f, y2 = %.2f\n", x2, y2);

	return 0;
}

/* 실행 결과 
index1 = 1, current1 = 0
index2 = 1, current2 = 1
x1 = 1.50, y1 = 0.50
x2 = 1.50, y2 1.50
*/
```