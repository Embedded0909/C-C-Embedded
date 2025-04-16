```cpp
CHƯƠNG 01 pointer
CHƯƠNG 02 bitwise
CHƯƠNG 03 typedef
CHƯƠNG 04 macro
CHƯƠNG 05 enum
CHƯƠNG 06 struct
CHƯƠNG 07 union
CHUONG 08 pack
```

## PHẦN 01: CON TRỎ
### 1.1 Con trỏ thông thường
### 1.2 Con trỏ void
```cpp
#include <stdio.h>
#include <stdint.h>

void mFunction(void* ptr, uint8_t size);

void mFunction( void *ptr , uint8_t size) {
    if (size == 1) {
        uint8_t* p8;
        p8 = (uint8_t*)ptr;
        *p8 = 0x12;
    }
    if (size == 2) {
        uint16_t* p16;
        p16 = (uint16_t*)ptr;
        *p16 = 0x1234;
    }
}

int main() {
    uint8_t a;
    uint8_t* ptr_a = &a;
    mFunction(ptr_a,1);

    uint16_t b;
    uint16_t* ptr_b = &b;
    mFunction(ptr_b, 2);

    printf("a = 0x%x\n", a);
    printf("b = 0x%x\n", b);

    return 0;
}
```
### 1.3 Con trỏ hàm
#### Call qua function
```cpp
#include <iostream>
#include <stdint.h>
using namespace std;

void view(int x);

void view(int x){
    printf("x = %d\r\n", x);
}

typedef void (*mfunction)(int);

int main()
{
    mfunction m = view;
    m(2);
    return 0;
}
```
#### Call qua địa chỉ
```cpp
#include <iostream>
#include <stdint.h>
using namespace std;

void view(int x);

void view(int x){
    printf("x = %d\r\n", x);
}

typedef void (*mfunction)(int);

int main()
{
    uint64_t address;

    printf("%p\r\n", address = (uint64_t)view);

    ((mfunction)address)(3);
 
    return 0;
}
```

## PHẦN 02: BITWISE
- AND
- OR
- XOR
- NOT
- Dịch trái
- Dịch phải