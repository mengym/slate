---
title: API Reference

language_tabs:
  - json
  - 
toc_footers:
  - <a href='http://www.aayongche.com'>Documentation Powered by AA 租车</a>

includes:
  - errors

search: true
---

# 简介

欢迎使用AA租车系统API说明文档

该API系统包含，APP接口，内部业务接口，事件接口，以及各种综合查询接口。

# 综合查询接口

Content-type : application/json

## 权限查询接口

> 返回JSON结果示例:

```json
{
  "code": 0,
  "result":{
  }
}
```

根据管理员ID，获取其所对应的所有权限信息。

### HTTP Request

`GET /privilege/user/{id}`

### Query Parameters

请求参数 | 类型 | 必填? | 描述
--------- | ------- | ------- | -----------
id | int | true | 用户的ID

<aside class="notice">
当传递参数有误,id为空或者用户已经被禁用等情况,返回值中result将为空.
</aside>
