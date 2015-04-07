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

欢迎使用AA租车后台业务系统API说明文档

该API系统包含，综合查询数据接口，内部业务接口，事件接口等。

# 综合查询接口

## 权限查询接口

> 返回JSON结果示例:


```json
{
  "code": 1,
  "msg": "",
  "manager": {
    "user_id": 1,
    "user_name": "张三",
    "city_code": [
      "010",
      "021"
    ],
    "mail": "example@aayongche.com",
    "phone": "13xxxxxxxxx",
    "status": 1,
    "role": {
      "role_key": "role_key",
      "role_name": "城市经理",
      "role_desc": "角色描述",
      "is_default": 1,
      "privilege_group": [
        {
          "privilege_group_key": "privilege_group_key",
          "group_name": "privilege_group_name",
          "privilege": [
            {
              "privilege_id": 1,
              "privilege_name": "privilege_name",
              "path": "/manager/privilege/a",
              "method": "get"
            },
            {
              "privilege_id": 2,
              "privilege_name": "privilege_name",
              "path": "/manager/privilege/b",
              "method": "post"
            },
            {
              "privilege_id": 3,
              "privilege_name": "privilege_name",
              "path": "/manager/privilege/c",
              "method": "export"
            },
            {"...": "..."}
          ]
        },
        {
          "privilege_group_key": "privilege_group_key",
          "group_name": "privilege_group_name",
          "privilege": [
            {
              "privilege_id": 1,
              "privilege_name": "privilege_name",
              "path": "/manager/privilege/a",
              "method": "get"
            },
            {
              "privilege_id": 2,
              "privilege_name": "privilege_name",
              "path": "/manager/privilege/b",
              "method": "post"
            },
            {
              "privilege_id": 3,
              "privilege_name": "privilege_name",
              "path": "/manager/privilege/c",
              "method": "export"
            },
            {"...": "..."}
          ]
        }
      ]
    }
  }
}
```


根据管理员ID，获取其所对应的所有权限信息。

### HTTP Request

`GET /privilege/user/{id}`

### Content-type

`application/json`

### Query Parameters

请求参数 | 类型 | 必填? | 描述
-------- | ---- | ----- | ----
id | Int | true | 用户的ID