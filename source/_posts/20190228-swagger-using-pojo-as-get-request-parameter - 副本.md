---
title: Swagger使用POJO类作为GET方法的入参
date: 2019-02-28 15:32:56
tags:
---

在使用Swagger注解生成文档时，出现一个问题，
原本paramType是正常的query形式

但在加入了@Valid注解后，paramType变成了body形式

要恢复正常只需要在@Valid注解之后再添加 @ModelAttribute 注解即可。

参考 https://github.com/springfox/springfox/issues/1219
