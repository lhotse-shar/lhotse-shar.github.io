---
layout: default
title:  "C++ 에서 형변환"
parent: C++
nav_order: 2
---

* content
{:toc}

<br>

# 요약
1. const_cast
2. static_cast
3. reinterpret_cast
4. dynamic_cast

<br>
<br>

# 1. const_cast

> 어떤 타입에서 const 속성이나 volatile 속성을 제거할 때 사용한다.

```c
const int ADC_Value = 100;

int i = const_cast<int> (ADC_Value);
```

<br>
<br>

# 2. static_cast

> C언어의 묵시적 형변한과 같다.

ex)


```c
int a = 5;

double b = (double)a;
```

|C 스타일|C++ 스타일|
|:------:|:------:|
|int a = 5;<br>double b = (double)a;|double a = 10.0;<br>char b = static_cast<char> (a);|

<br>
<br>

# 3. reinterpret_cast

> 일반적으로 허용하지 않는 위험한 형변환을(강제 형변환) 할 때 사용한다. 그 안의 데이터가 어떤 객체이던 그저 비트열로만 보고 원하는 형으로 강제로 변환한다는 것이다.

ex)

```c
포인터를 정수로 변환하는 작업.

int a;

int * b;

a = reinterpret_cast<int>(&b);
```

<br>
<br>

# 4. dynamic_cast

> **유일하게 C스타일의 형변환으로 흉내낼 수 없는 형 변환** 이다. dynamic_cast는 서로 상속 관계에 있는 클래스간의 형변환을 할 때 사용한다.

> 형 변환에 문제가 없는지 안전검사도 하는데 문제가 있을시에는 NULL값을 리턴하거나 예외를 띄운다. 가상함수가 없는 클래스는 사용할 수 없다.

ex)

```c
truck* ptruck = new car;

truck* ptruck = dynamic_cast<truck*>(new car);
```


<br>

---

<script src="https://utteranc.es/client.js"
        repo="lhotse-shar/lhotse-shar.github.io"
        issue-term="pathname"
        label="Comment"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>