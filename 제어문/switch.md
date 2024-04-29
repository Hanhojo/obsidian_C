#### 정수식의 값에 따라서 여러 가지 경우 중 하나로 분기한다. ####
___
```c
switch (menu) {
case 1:
	printf("1번 메뉴 선택");
	break;
case 2:
	printf("2번 메뉴 선택");
	break;
default:
	printf("잘못 선택하셨습니다.\n");
	break;
}
```

default가 생략된 switch문이다. num % 2는 항상 0또는 1이므로 생략이 가능하다.
```c
switch(num % 2) {
case 0:
	printf("even\n");
	break;
case 1:
	printf("odd\n");
	break;
}
```

## switch 사용 시 주의 사항 ##
1. ***switch문에서 break는 생략할 수 있다.***
	1. break를 생략시 끝을 만날 때까지 나오는 모든 문장들을 수행한다.
2. ***switch문에서 default는 생략할 수 있다.***
	1. switch문에 일치하는 case가 없고 default도 없으면 아무것도 수행하지 않고 switch문을 빠져나간다.
	2. default에도 break를 써주는 것이 좋다.