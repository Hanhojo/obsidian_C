#### 함수나 블록 안에 선언되는 변수로 함수나 블록 안에서만 사용할 수 있다. ####
___

## 지역 변수 선언 (함수 안에 선언하는 경우)##
```c
int get_gcd(int x, int y)
{
	int r; // get_gcd 함수 전체에서 사용할 수 있다.
	while (y != 0)
	{
		r = x % y;
		x = y;
		y = r;
	}
	printf("%d", r);  // 사용가능
	return x;
}
```

## 지역 변수 선언(while 블록 안에 선언하는 경우) ##
```c
int get_gcd(int x, int y)
{
	while (y != 0)
	{
		int r; // while블록 안에서만 사용할 수 있다.
		r = x % y;
		x = y;
		y = r;
	}
	printf("%d", r);  // 사용가능
	return x;
}
```