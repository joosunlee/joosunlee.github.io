---
layout: single
title:  "실습 예제입니다.!"
---




# Ex 1-1: Introduction
텐서플로우 2.x을 이용한 인공지능 실습

임포트: 필요한 모듈이나 라이브러리를 갖고 온다.


```python
import tensorflow as tf
import numpy as np
import matplotlib.pyplot as plt
```

버전 체크


```python
tf.__version__
```




    '2.5.0'



Eager execution


```python
a = tf.constant(5)
b = tf.constant(3)
c = a*b

print(c)
```

    tf.Tensor(15, shape=(), dtype=int32)
    

Hello TensorFlow!


```python
hello = tf.constant("Hello TensorFlow!")

print(hello.numpy())
```

    b'Hello TensorFlow!'
    

Indexing, slicing


```python
nums = list(range(5))
print(nums)
```

    [0, 1, 2, 3, 4]
    


```python
print(nums[2:4])
print(nums[2:])
print(nums[:2])
print(nums[:])
print(nums[:-1])
```

    [2, 3]
    [2, 3, 4]
    [0, 1]
    [0, 1, 2, 3, 4]
    [0, 1, 2, 3]
    


```python
nums[2:4] = [8,9]
print(nums)
```

    [0, 1, 8, 9, 4]
    

2D Array


```python
b = np.array([1])
b
```




    array([1])




```python
print(b.ndim)
```

    1
    


```python
print(b.shape)
```

    (4, 4)
    


```python
print(b[:,-1])
```

    [ 4  8 12]
    


```python
print(b[-1])
```

    [ 9 10 11 12]
    


```python
print(b[-1,:])
```

    [ 9 10 11 12]
    


```python
print(b[-1,...])
```

    [ 9 10 11 12]
    


```python
print(b[0:2,:])
```

    [[1 2 3 4]
     [5 6 7 8]]
    

Reshape


```python
a = np.arange(12)

a
```




    array([ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11])






```python
a.reshape(3,4)
```




    array([[ 0,  1,  2,  3],
           [ 4,  5,  6,  7],
           [ 8,  9, 10, 11]])



텍스트



```python
a.reshape(-1,2)
```




    array([[ 0,  1],
           [ 2,  3],
           [ 4,  5],
           [ 6,  7],
           [ 8,  9],
           [10, 11]])



# 제목
## 소제목
### 작성

