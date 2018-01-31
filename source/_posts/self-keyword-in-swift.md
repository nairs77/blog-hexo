---
title: How to use correctly 'self' keyword in Swift
tags:
 - swift
categories: 
 - iOS
 - swift
date: 2017-06-21 18:20:58
thumbnail:
 http://code.visualstudio.com/opengraphimg/opengraph-blog.png
---

원본 - [How to use correctly 'self' keyword in Swift - Dmitri Pavlutin Blog](https://dmitripavlutin.com/how-to-use-correctly-self-keyword-in-swift/)

Swift에서 'self'는 인스턴스 자신을 가리키는 아주 특별한 property이다. 

### Access instance properties and methods
예를 들면 아래 Weather 구조체에서는 초기화나 isDayForWalk() Method 호출시 self를 사용했다.
