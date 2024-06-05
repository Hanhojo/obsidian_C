#### 배열은 같은 데이터형의 변수를 메모리에 연속적으로 할당하고 같은 이름으로 사용하는 기능이다. ####
____
배열 사용
```c
int main(void)
{
	int num[5]; //크기가 5인 배열을 선언한다.
	int sum = 0;
	int i, max;
	for ( i = 0; i < 5; i++)
	{
		scanf("%d", &num[i]);
		sum += num[i];
	}
	printf("sum = %d\n", sum);
	max = num[0] > num[1] ? num[0] : num[1];

	return 0;
}
```
- [[배열의 특징]]
- [[배열의 선언]]
- [[배열의 초기화]]
- [[배열의 사용]]
- 