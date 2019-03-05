---
title: 使用swagger返回泛型的response
date: 2019-03-06 00:32:56
tags:
---

使用swagger时，当返回结果为泛型时，生成的文档中Response Class会没有具体的类型，如

```
public Wrapper<T> query(){
  ...
}
```

生成的response class会是

```
{
  "data": {},//泛型
  "message": "string",
  "resultCode": 0
}
```

想要输出完整的response，需要指明泛型的类，修改代码为

```
public Wrapper<User> query(){
  ...
}
```

得到

```
{
  "data": {
    "user": {
      "name":"string",
      "age":"string"
    }
  },//泛型
  "message": "string",
  "resultCode": 0
}

