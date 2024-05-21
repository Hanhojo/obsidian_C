#### 함수 밖에 선언되는 변수로 소스 파일 전체에서 사용할 수 있다. ####
___

## 전역 변수의 특징 ##

1. 프로그램 전체에서 사용되는 변수이다.
2. 여러 함수에서 사용되어야 하므로 함수 안에 선언하는 대신 함수 밖에 선언한다.
3. 소스파일 시작 부분에 선언한다. 및 프로그램 종료 시 소멸된다.

## 전역 변수의 선언 및 활용 ##
```c
#inlcude <stdio.h>

void print_count(void);
void increment(void);
void decrement(void);

int count; // 전역 변수 

int main(void)
{
	int i;

	count = 0;
	print_count();

	for(i = 0; i < 3; i++)
		increment();
	print_count();

	for(i = 0; i < 3; i++)
		decrement();
	print_count();

	return 0;
}

void print_count(void)
{
	printf("count = %d\n", count);
}

void increment(void)
{
	count++;
}

void decrement(void)
{
	count--;
}
/* count = 0
count = 3
count = 0
```