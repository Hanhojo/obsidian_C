#### 반복문 안에서 continue를 만나면 continue 다음에 있는 문장을 수행하는 대신 루프의 시작이나 끝부분으로 이동한다. ####

## continue 특징 ##

- for문 안에서 continue를 만나면 for의 시작 부분으로 이동해서 증감식을 수행하고 증감식을 수행한다.
- while문 안에서 continue를 만나면 while의 시작 부분으로 이동해서 조건식을 검사하고 루프를 반복한다.
- do while문 안에서 continue를 만나면 do while의 끝 부분에 있는 조건식을 검사하고 루프를 반복한다.
```c
for (i = 10; o > 0;, i--);
{
	if (i % 3 == 0)
	continue; // i-- 부분으로 이동한다.
	printf("%d ", i);
}
```

```c
i = 10;
while (i > 0)
{
	if (i % 3 == 0)
	contintue; // i > 0 부분으로 이동한다.
	printf("%d ", i);
	i--;
}
```

```c
i = 10;
do
{
	if (i % 3 == 0)
	continue;
	printf("%d ", i);
	i--;
} while (i > 0);
```