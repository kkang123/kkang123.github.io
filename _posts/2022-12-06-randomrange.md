---
layout: post
title: (Unity) 랜덤함수 Random.Range
tags: [Unity]
categories: Unity
---


# 랜덤함수 Random.Range

컴퓨터 프로그래밍 언어에서는 난수라고도 한다.  
컴퓨터는 랜덤이란게 존재 할 수 없어서 일정 범위에 숫자값을 집어넣고 그 중에 윈도우나 유니티 상에서 시간값을 가지고 숫자를 뽑아내는 것을 난수라고한다.

```c#
Random.Range(min,max ) //min [inclusive]과 max [inclusive]사이의 랜덤 float 수를 반환 , inclusive=포함
```

`주의할점을 값이 int일 경우 max값은[exclusive](제외) 나오지 않는다. `

INT형
```c#
using UnityEngine;
public class Example : MonoBehaviour
{
    private void Start()
    {
        Debug.Log("1차 테스트");
        for (int i = 0; i < 5; ++i)
        {
            // UnityEngine.Random.Range(0, 10);
            // 0 ~ 9 정수
            int result = Random.Range(0, 10);
            Debug.Log($"Random {i + 1}회 : {result}");
        }

        Debug.Log("2차 테스트");
        for (int i = 0; i < 5; ++i)
        {
            // -10 ~ 19 정수
            int result = Random.Range(-10, 20); 
            Debug.Log($"Random {i + 1}회 : {result}");
        }
    }
}
```

<br>

float형
```c#
using UnityEngine;
public class Example : MonoBehaviour
{
    private void Start()
    {
        Debug.Log("1차 테스트");
        for (int i = 0; i < 5; ++i)
        {
            // UnityEngine.Random.Range(0.0f, 10.0f);
            // 0 ~ 10 실수
            float result = Random.Range(0.0f, 10.0f);
            Debug.Log($"Random {i + 1}회 : {result}");
        }

        Debug.Log("2차 테스트");
        for (int i = 0; i < 5; ++i)
        {
            // -10 ~ 20 실수
            float result = Random.Range(-10.0f, 20.0f);
            Debug.Log($"Random {i + 1}회 : {result}");
        }
    }
}
```
