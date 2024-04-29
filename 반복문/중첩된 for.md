#### for문 안에 다시 for문을 사용하는 것을 중첩된 for라고 한다. ####
____

## 입력된 문자로 직사각형 그리기 ##
```c
int main(void)
{
	int width, height;
	char ch;
	int i, j;

	printf("직사각형의 폭과 높이? ");
	scanf("%d %d", &width, &height);
	printf("직사각형을 그릴 문자? ");
	scanf(" %c", &ch); // %c 앞에 빈칸 지정 

	for ( i = 0; i < height; i++)
	{
		for(j = 0; j < width; j++)
			printf("%c". ch);
		printf("\n");
		}

	return 0;	
}
```
### scanf의 형식 문자열에서 빈칸을 지정하면 이전 입력에서 입력 버퍼에 남아있는 공백 문자를 무시한다. ###
```c
scanf("%d%d", &width, &height); // 정수, 실수 입력에서는 빈칸이 없어도 된다.
scanf(" %c", &ch); // 문자 입력에서는 빈칸이 있어야 공백 문자를 무시한다.
```