#### while문은 조건식과 반복할 문장으로 구성되며, 조건식이 참인 동안 반복할 문장을 수행한다. 조건식이 거짓이 되면 while문을 빠져나가 while문의 다음 문장을 수행한다. ####
____

## while의 기본 ##
#### while(조건식)
#### 반복할 문장 ####
```c
i = 0;
while (i < 10);
	printf("%d ". i ++);
```

## while의 특징 ##

## while의 사용 예 ##
```c
#include <stdio.h>
int main(void)
{
	int i = 0;
	while (i < 10)
		printf("%d ", i++);
	printf("\n");

	return 0;
}
// 0 1 2 3 4 5 6 7 8 9
```
