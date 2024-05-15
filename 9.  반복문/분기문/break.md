#### break문은 switch나 반복문과 함께 사용된다. ####
___

## break의 기본 ##

1. break문은 switch나 반복문과 함께 사용된다.
2. break문을 switch문 안에 사용하면 제어의 흐름이 switch를 탈출해서 switch의 다음 문장으로 이동한다.
3. break문을 for while do while 등의 반복문 안에서 사용하면 반복문을 빠져나가게 된다.

## break의 사용 예
```c
# include <stdio.h>

int main (void)
{
	int i;

	for (i = 10, i > 0; i--)
	{
		if (i % 3 == 0) // 루프 탈출 조건
			break;
			printf("%d ", i);
	}
	printf("\n");

	return 0;
}
// 10
```

