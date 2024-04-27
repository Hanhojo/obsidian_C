#### 감소되기 전 변수 a의 값(후위 감소 연산자) ####

## 후위 감소 연산자 예제 ##

```c
#include <stdio.h>

int main(void)
{
	int b = 5;

	int post_decrement = b--; // 후위 감소 연산자 사용

	printf("After b--: b = %d, post_decrement = %d\n", b, post_decrement);

	return 0;
}
// 출력 결과// 
// After b--: b = 4, post_decrement = 5//
```
