값을 변경할 수 없는 변수를 선언하기 위해 사용
### const 변수는 반드시 선언 시 초기화해야 한다. ###

```c
# include <stdio.h>

int main(void)
{
	int amount = 0 , price = 0;
	const double VAT_RATE = 0.1;
	int total_price = 0;

	total_price = amount * price * (1 + VAT_RATE); //const 변수 사용
}
```