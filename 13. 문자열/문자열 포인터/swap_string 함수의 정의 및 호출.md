###  문자 배열을 변경하려면 배열의 크기가 필요하므로 size를 인자로 전달한다.
_____
```c
int swap_string(char* lhs, char* rhs, int size)
{
	int lhs_len = strlen(lhs);
	int rhs_len = strlen(rhs);
	char temp[SIZE] = "";

	if (lhs_len + 1 > SIZE || rhs_len + 1 > SIZE)
		return 0; // swap_string 실패

	strcpy(temp, lhs);
	strcpy(lhs, rhs);
	strcpy(rhs, temp);
	return 1; // swap_string 성공
}
```
- swap_string 함수는 **문자열 2개를 매개변수로 받아와야 하며,** 함수 안에서 그 값을 읽어서 변경해야 하므로 **입출력 매개변수**이다.
- swap_string 함수는 lhs 길이나 rhs길이가 size보다 큰 경우에는 문자열을 서로 맞 바꿀수 없으므로 0을 리턴한다.
- **함수 성공 시 1을 리턴하고 실패 시 0을 리턴하게 정의할 수 있다.

```c
swap_string(str1, str2, SIZE); // swap_string의 인자로 문자 배열만 전달할 수 있다.
swap_string(str1, "no good", SIZE) // 실행 에러
```
- **swap_string 함수를 호출하려면 매개변수가 char* 형이므로 문자배열을 인자로 전달해야 한다.**

```c
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <string.h> // 문자열 처리 라이브러리
#define SIZE 28 // 문자열 배열의 크기를 정의, 문자열의 최대 길이 28
int swap_string(char* lhs, char* rhs, int size); // size는 문자열의 최대 크기

int main(void)
{
	char str1[SIZE] = ""; // 빈 문자열로 초기화
	char str2[SIZE] = ""; // 빈 문자열로 초기화

	printf("문자열 2개? ");
	scanf("%s %s", str1, str2);

	printf("str1=%s, str2=%s\n", str1, str2);
	swap_string(str1, str2, SIZE);
	printf("str1=%s, str2=%s\n", str1, str2);
	return 0;
}

int swap_string(char* lhs, char* rhs, int size)
{
	int lhs_len = strlen(lhs); // lhs의 문자열의 길이를 계산후 저장
	int rhs_len = strlen(rhs); // rhs의 문자열의 길이를 계산후 저장
	char temp[SIZE] = "";

	if (lhs_len + 1 > size || rhs_len + 1 > size) // lhs나 rhs 문자열의 길이가 size보다 크면 교환하지 않고 0을 반환 +1은 널문자가 필요해서임
		return 0; // swap_string 실패

	strcpy(temp, lhs);
	strcpy(lhs, rhs);
	strcpy(rhs, temp);
	return 1; // swap_string 성공
}
/* 문자열 2개? ski golf
str1=ski, str2=golf
str1=golf, str2=ski
```

#### 수시 시험 출제 
```c
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <string.h> 
#define SIZE 120 // if 문의 사이즈에 따라 성공 실패 결정
int swap_string(char* lhs, char* rhs, int size);

int main(void)
{
	char str1[SIZE] = "";
	char str2[SIZE] = "";
	int swap_ok;

	printf("문자열 2개? ");
	scanf("%s %s", str1, str2);

	printf("str1=%s, str2=%s\n", str1, str2);
	swap_ok = swap_string(str1, str2, SIZE);
	if(swap_ok) {
		printf("swap success!\n");
		printf("str1=%s, str2=%s\n", str1, str2);
		}
	else
		printf("swap failed\n");
		
	return 0;
}

int swap_string(char* lhs, char* rhs, int size)
{
	int lhs_len = strlen(lhs);
	int rhs_len = strlen(rhs);
	char temp[SIZE] = "";

	if (lhs_len + 1 > size || rhs_len +1 > size)
		return 0; // swap 실패

	strcpy(temp, lhs);
	strcpy(lhs, rhs);
	strcpy(rhs, temp);
	return 1; // swap 성공
}
```