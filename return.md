#### 프로그램 수행 중에 return문을 만나면 함수를 호출한 곳으로 되돌아간다. ####

## return의 사용 예 ##
```c
# include <stdio.h>

int main(void)
{
	int i;

	for (i = 10; i > 0; i--)
	{
		if (i % 3 == 0)
			return 1; // main 함수를 리턴시킨다.(프로그램 종료)
		printf("%d ", i);
		}
		printf("\n");

		return 0;
}
// 10
```