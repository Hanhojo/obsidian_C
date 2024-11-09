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

₩