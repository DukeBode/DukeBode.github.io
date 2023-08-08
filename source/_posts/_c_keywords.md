---
title: C language keywords
date: 2023-07-17 17:15:16
cover:
tags: c
---

<!-- more -->

### 0.1. nullptr
### 0.2. true
### 0.3. false
## 1. 类型说明符
### 1.1. void
### 1.2. bool
### 1.3. \_Bool
### 1.4. char
### 1.5. short
### 1.6. int
### 1.7. signed
### 1.8. unsigned
### 1.9. long
### 1.10. \_BitInt
### 1.11. float
### 1.12. double
### 1.13. \_Decimal32
### 1.14. \_Decimal64
### 1.15. \_Decimal128
### 1.16. \_Imaginary
### 1.17. \_Complex

### 1.18. enum 
### 1.19. struct 结构体
### 1.20. union 联合体
## 2. 存储类说明符
### 2.1. auto
### 2.2. register
### 2.3. static
### 2.4. extern
### 2.5. thread_local
### 2.6. \_Thread_local
### 2.7. typedef
## 3. 类型限定符
### 3.1. const
### 3.2. volatile
### 3.3. restrict
### 3.4. \_Atomic
## 4. 函数说明符
### 4.1. inline
### 4.2. \_Noreturn
## 5. 对齐说明符
### 5.1. alignas
### 5.2. \_Alignas
## 6. 选择语句
### 6.1. if
### 6.2. else
### 6.3. switch
### 6.4. case
### 6.5. default
## 7. 循环语句
### 7.1. while
### 7.2. do
### 7.3. for
## 8. 跳转语句
### 8.1. break

### 8.2. continue

### 8.3. return

### 8.4. goto

## 9. 运算符

### 9.1. sizeof
### 9.2. alignof
### 9.3. \_Alignof
### 9.4. typeof
### 9.5. typeof_unqual

```c
if(true){}else{}
```

```c
switch(i){
    case 1:;
    default:;break;
}
```
```c
/* 声明不接收参数的函数 */
int f(void);
```
## 10. 其他
### 10.1. constexpr
### 10.2. \_Generic
```c
#define cbrt(X) _Generic((x),\
	long double: cbrtl,\
	default:curt,\
	flat:cbrtf\
	}(x)
```
## 11. 静态断言
### 11.1. static_assert
### 11.2. \_Static_assert

