# 家庭作业

## 练习题 8.9

{% tabs %}
{% tab title="答案" %}

{% endtab %}

{% tab title="练习题 8.9" %}
考虑四个具有如下开始和结束时间的进程：

| 进程 | 开始时间 | 结束时间 |
| :---: | :---: | :---: |
| A | 5 | 7 |
| B | 2 | 4 |
| C | 3 | 6 |
| D | 1 | 8 |

对于每对进程，指明它们是否是并发地运行的：

| 进程对 | 并发地？ |
| :---: | :---: |
| AB |  |
| AC |  |
| AD |  |
| BC |  |
| BD |  |
| CD |  |
{% endtab %}
{% endtabs %}

## 练习题 8.10

{% tabs %}
{% tab title="答案" %}

{% endtab %}

{% tab title="练习题 8.10" %}
在这一章里，我们介绍了一些具有不寻常的调用和返回行为的函数：setjmp、longjmp、execve 和 fork。找到下列行为中和每个函数相匹配的一种：

A. 调用一次，返回两次。

B. 调用一次，从不返回。

C. 调用一次，返回一次或者多次。
{% endtab %}
{% endtabs %}

## 练习题 8.11

{% tabs %}
{% tab title="答案" %}

{% endtab %}

{% tab title="练习题 8.11" %}
这个程序会输出多少个 “hello” 输出行？

{% code title="code/ecf/forkprob1.c" %}
```c
#include "csapp.h"

int main()
{
    int i;

    for (i = 0; i < 2; i++)
        Fork();
    printf("hello");
    exit(0);
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

## 练习题 8.12

{% tabs %}
{% tab title="答案" %}

{% endtab %}

{% tab title="练习题 8.12" %}
这个程序会输出多少个 “hello” 输出行？

{% code title="code/ecf/forkprob4.c" %}
```c
#include "csapp.h"

void doit()
{
    Fork();
    Fork();
    printf("hello\n");
    return;
}

int main()
{
    doit ();
    printf("hello\n");
    exit(0);
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

## 练习题 8.13

{% tabs %}
{% tab title="答案" %}

{% endtab %}

{% tab title="练习题 8.13" %}
下面程序的一种可能的输出是什么？

{% code title="code/ecf/forkprob3.c" %}
```c
#include "csapp.h"

int main() 
{
    int x = 3;

    if (Fork() != 0)
        print! ("x=%d\n", ++x);

    printf("x=%d\n", --x);
    exit(0);
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

## 练习题 8.14

{% tabs %}
{% tab title="答案" %}

{% endtab %}

{% tab title="练习题 8.14" %}
这个程序会输出多少个 “hello” 输出行？

{% code title="code/ecf/forkprob5.c" %}
```c
#include "csapp.h"

void doit()
{
    if (Fork() == 0) {
        Fork();
        printf("hello\n");
        exit(0);
    }
    return;
}

int main()
{
    doit();
    printf("hello\n");
    exit(0);
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

## 练习题 8.15

{% tabs %}
{% tab title="答案" %}

{% endtab %}

{% tab title="练习题 8.15" %}
这个程序会输出多少个 “hello” 输出行？

{% code title="code/ecf/forkprob6.c" %}
```c
#include "csapp.h"

void doit()
{
    if (Fork() == 0) {
        Fork();
        printf("hello\n");
        return;
    }
    return;
}

int main()
{
    doit();
    printf("hello\n");
    exit(0);
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

## 练习题 8.16

{% tabs %}
{% tab title="答案" %}

{% endtab %}

{% tab title="练习题 8.16" %}
下面这个程序的输出是什么？

{% code title="code/ecf/forkprob7.c" %}
```c
#include "csapp.h"
int counter = 1;

int main()
{
    if (fork() == 0) {
        counter--;
        exit(0);
    }
    else {
        Wait(NULL);
        printf("counter = %d\n", ++counter);
    }
    exit(0);
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

## 练习题 8.17

{% tabs %}
{% tab title="答案" %}

{% endtab %}

{% tab title="练习题 8.17" %}
列举练习题 8.4 中程序所有可能的输出。
{% endtab %}
{% endtabs %}

练习题 8.18

练习题 8.19

练习题 8.20

练习题 8.21

练习题 8.22

练习题 8.23

练习题 8.24

练习题 8.25

练习题 8.26
