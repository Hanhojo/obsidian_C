#### if문 안에 다른 if문이 포함된 것을 중첩된if라고 한다. ####
```c
#include <stidio.h>

int main(void)
{
	int age, fee;

	printf("나이?" );
	scanf("%d", &age);

	if (age >= 8){
		if (age >=65){
			fee = 5000;
			}
			else {
				fee = 10000;
				}
			}
			else {
				fee = 0;
				}
		printf("입장료 : %d원\n", fee);

		return 0;
}
```
