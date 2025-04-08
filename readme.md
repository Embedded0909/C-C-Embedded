⚠️ Hãy dùng giấy để code                 

### Kiến thức về For trong C

Q1:
```cpp
for(int i = 0 ; i < 129 ;i++){
    i++;
}
printf("%d res = \n",i);
```
Q2:
```cpp
char i;
for(int i = 0 ; i < 128 ;i++){

}
printf("%d res = \n",i);
```
Q3:
```cpp
char i;
for(;;i++){
    break;
    ++i;
}
printf("%d res = \n",i);
```
Q4:
```cpp
char i = -1;
for(;;++i){
    break;
    ++i;
}
printf("%d res = \n",i);
```
### Kiến thức về String trong C

Q1:
```cpp
// Online C compiler to run C program online
#include <string>
#include <iostream>
using namespace std;
int main() {
    string c = "hyhy";
    printf("%s",c);
    return 0;
}
```

### Kiến thức về Pointer trong C

Q1:
```cpp
int a = 1, b = 2, c = 3, d = 4;
int *pa = &a, *pb = &b, *pc = &c, *pd = &d;
pa = pb;
pb = pc;
pc = pd;
pd = pa;
pb = &a;
a = b + 2;
pc = &d;
pa = &d;
c++;
printf("%d %d %d %d \n", a, b, c, d);
```