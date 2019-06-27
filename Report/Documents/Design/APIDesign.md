# API 说明文档

该文档给出 api 使用介绍。

api 网址：`api.buke.zophyr.com`

## User

### 新增一个 user

> api.buke.zophyr.com/user

| 接口  | 方法 |       传参       |
| :---: | :--: | :--------------: |
| /user | POST | application/json |

```json
{
  "name": "user name",
  "open_id": "id from wechat"
}
```

### 新增 todo 到 user 中

> api.buke.zophyr.com/user/:id/todo

|   key | value                       |
| ----: | :-------------------------- |
|  接口 | /user/:id/todo              |
|  方法 | POST                        |
|  传参 | application/json            |
| `:id` | 要操作的 user 对应的 obj_id |

```json
{
  "user": ["which users will add to this user", "is array with obj_id"]
}
```

### 删除 user

> api.buke.zophyr.com/user/:id

|   key | value                       |
| ----: | :-------------------------- |
|  接口 | /user/:id                   |
|  方法 | DELETE                      |
|  传参 | application/json            |
| `:id` | 要操作的 user 对应的 obj_id |

```json
{
  "user": ["which users will delete", "is array with obj_id"]
}
```

## Todo

### 新增一个 todo

> api.buke.zophyr.com/todo

| 接口  | 方法 |       传参       |
| :---: | :--: | :--------------: |
| /todo | POST | application/json |

```json
{
  "title": "todo name",
  "receive_group": "which group will accept this todo, obj_id",
  "receive_user": ["which users will accept this todo", "is array with obj_id"],
  "owner": "which create this todo, obj_id"
}
```

### 新增用户到 todo 中

> api.buke.zophyr.com/todo/:id/user

|   key | value                       |
| ----: | :-------------------------- |
|  接口 | /todo/:id/user              |
|  方法 | POST                        |
|  传参 | application/json            |
| `:id` | 要操作的 todo 对应的 obj_id |

```json
{
  "receive_user": ["which users will add to this group", "is array with obj_id"]
}
```

### 删除 todo

> api.buke.zophyr.com/todo/:id

|   key | value                       |
| ----: | :-------------------------- |
|  接口 | /todo/:id                   |
|  方法 | DELETE                      |
|  传参 | application/json            |
| `:id` | 要操作的 todo 对应的 obj_id |

```json
{
  "todo": ["which todo will delete", "is array with obj_id"]
}
```

## Group

### 新增一个 group

> api.buke.zophyr.com/group

|  接口  | 方法 |       传参       |
| :----: | :--: | :--------------: |
| /group | POST | application/json |

```json
{
  "name": "group name",
  "owner": "which create this group, obj_id",
  "members": ["which users will accept this todo", "is array with obj_id"]
}
```

### 添加成员到 group 中

> api.buke.zophyr.com/group/:id/user

|   key | value                     |
| ----: | :------------------------ |
|  接口 | /group/:id/user           |
|  方法 | POST                      |
|  传参 | application/json          |
| `:id` | 要操作的群组对应的 obj_id |

```json
{
  "members": ["which users will add to this group", "is array with obj_id"]
}
```

### 删除 group 中的成员

> api.buke.zophyr.com/group/:id/user

|   key | value                     |
| ----: | :------------------------ |
|  接口 | /group/:id/user           |
|  方法 | DELETE                    |
|  传参 | application/json          |
| `:id` | 要操作的群组对应的 obj_id |

```json
{
  "members": ["which users will delete from this group", "is array with obj_id"]
}
```
