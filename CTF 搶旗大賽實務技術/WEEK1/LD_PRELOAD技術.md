#
```

```
## 範例
```
// main.c
#include <stdio.h>
#include <math.h>

int main() {
  double x;
  
  scanf("%lf", &x);
  printf("%f\n", sqrt(x));
  return 0;
}
```
### 執行看看正確答案
```
gcc -o main main.c -lm
./main
```
### 撰寫駭客程式
```
//hook.c
double sqrt(double x) {
  return 2;
}
```
### 編譯並執行看看被竄改的答案
```
gcc -o hook.so -shared hook.c
LD_PRELOAD=./hook.so ./main
```
