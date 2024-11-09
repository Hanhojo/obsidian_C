###  문자 배열을 변경하려면 배열의 크기가 필요하므로 size를 인자로 전달한다.
_____
```c
int swap_string(char* lhs, char* rhs, int size)
{
	int lhs_len = strlen(lhs);
	int rhs_len = strlen(rhs);
	char temp[SIZE] = "";

	if (lhs_len + 1 > SIZE || rhs_len + 1 > SIZE)
}
```