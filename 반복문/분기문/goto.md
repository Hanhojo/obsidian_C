#### 프로그램 실행 중 제어의 흐름을 프로그램의 특정 위치로 이동하려면 goto문을 사용한다. ####

## goto 특징 ##

- goto문을 사용하려면 먼저 이동할 문장을 가리키는 레이블(label)이 필요하다.
- 레이블을 정의할 때는 콜론이 필요하다.
- 한꺼번에 여러 개의 루프를 탈출해야 할 때 유용하게 사용된다.
## goto의 사용 예 ##
```c
#include <stdio.h>

int main(void)
{
	int i;

	for (i = 10; i > 0; i--)
	{
		if (i % 3 == 0)
			goto quit;
			printf("%d ", i);
	}
	quit:
		printf("\n");

	return 0;
}
```
