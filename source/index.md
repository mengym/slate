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

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/3"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Isis",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">If you're not using an administrator API key, note that some kittens will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the cat to retrieve

