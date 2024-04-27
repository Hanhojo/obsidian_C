
if(조건식1)
	문장1;
else if(조건식2)
	문장2;
else
	문장 3;

```c
# include <stdio.h>

int main(void)
{
	 int menu;

	printf("1.파일 열기\n");
	printf("2.재생\n");
	printf("3.재생 옵션\n");
	printf("선택: ");

	scanf("%d", &menu);
	if (menu == 1) {
		printf("파일 열기 메뉴를 선택했습니다.\n");
	}
	else if (menu == 2) {
		printf("재생 메뉴를 선택했습니다.\n");
	}
	else if (menu == 3) {
		printf("재생 옵션 메뉴를 선택했습니다.\n");
	}
	else {
		printf("잘못 선택하셨습니다.\n");
	}

	return 0; 
}
```

```c
#include <stdio.h>

int main(void)
{
	int a,b;
	char op;

	printf("수식? ");
	scanf("%d %c %d", &a, &op, &b);

	if (op == '+') {
		printf("%d + %d = %d\n", a,b,a+b);
	}
	else if (op == '-') {
	printf("%d - %d = %d\n",a,b,a-b);
	}
	else if (op == '*') {
	printf("%d * %d = %d\n",a,b,a*b);
	}
	else if(op == '/') {
		if (b != 0)
			printf("%d / %d = %.2f\n",a,b,(double)a / b);
		else
			printf("0으로 나눌 수 없습니다.\n");
	}
	else {
		printf("잘못된 수식입니다.\n");
	}

	return 0;
}
```
