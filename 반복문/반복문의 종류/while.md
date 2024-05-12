#### while문은 조건식과 반복할 문장으로 구성되며, 조건식이 참인 동안 반복할 문장을 수행한다. 조건식이 거짓이 되면 while문을 빠져나가 while문의 다음 문장을 수행한다. ####
____

## while의 기본 ##
```c
i = 0; // 변수의 초기화
while (i < 10); // while(조건식)
	printf("%d ". i ++); // 반복할 문장
```

## while의 특징 ##

-  while문은 조건식과 반복할 문장으로 구성되므로 사용 형식이 for문에 비해 간단하다.
-  변수의 초기화는 while문 전에 수행되어야 한다.
-  for의 증감식은(후위형 증가 연산자) while문의 반복할 문장에서 수행되어야 한다.

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
