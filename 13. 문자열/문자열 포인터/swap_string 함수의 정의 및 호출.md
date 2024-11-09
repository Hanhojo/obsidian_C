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
-  