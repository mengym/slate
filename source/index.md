---
title: API Reference

language_tabs:
  - json
  - 
toc_footers:
  - <a href='http://github.com/tripit/slate'>Documentation Powered by AA 租车</a>

includes:
  - errors

search: true
---

# 简介

欢迎使用AA租车系统API说明文档

该API系统包含，APP接口，内部业务接口，事件接口，以及各种综合查询接口。

# 综合查询接口

## 权限查询接口

```json

请求示例代码

```

> The above command returns JSON structured like this:

```json

返回JSON结果示例

```

根据管理员ID，获取其所对应的所有权限信息。

### HTTP Request

`GET http://example.com/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="notice">
当传递参数有误,用户ID为空或者用户已经被禁用等情况,返回值将为空.
</aside>

