#### 피연산자가 1개이다. ####
___
## 단항 연산자의 종류 ##

- '+' a
- '-' a
- [[a ++]]
- [[++a]]
- [[a -- ]]
- [[-- a]]
- !a
- &a
- ~a
- size of a

### 피연산자가 하나인 단항 연산자에서는 항상 정수의 승격이 일어난다. ###
```c
short a = 10;
printf("%d", sizeof(+a)); // +a는 int형으로 승격되므로 sizeof(+a)는 4
printf("%d", sizeof(-a)); // -a는 int형으로 승격되므로 sizeof(-a)는 4
```

### 피연산자의 형이 일치하더라도 int형보다 크기가 작은 경우에는 항상 int형으로 변환해서 연산을 수행한다. ###
```c
short a = 1000, b = 1000;
printfg("%d", sizeof(a * b)); //a, b는 int형으로 승격되므로 sizeof(a*b)는 4
```