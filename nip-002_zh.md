## NIP - 002: IPAL 扩展

```
Number:  NIP-002
Title:  IPAL 扩展
Type:    Standard
Status:  Draft
Authors: iavl <z6521256@gmail.com>
Created: 2020-04-09
```

## 简要说明

关于IPAL声明中的扩展字段"extension"使用标准。

## 动机

为了客户端根据业务变更需要，IPAL声明中增加扩展字段"extension"。

## 规范

"extension"内容为字符串，约定为json格式。

### 增加communication_visable

communication_visable 为bool类型，如果值为false，则表示不展示在客户端通讯服务器列表中。

如果该字段不存在于extension中，则默认表示展示在客户端通讯服务器列表中。

### 增加application_visable

application_visable 为bool类型，如果值为false，则表示不展示在客户端应用服务器列表中。

如果该字段不存在于extension中，则默认表示展示在客户端应用服务器列表中。


## 示例

extension字段示例：

```json
{
	"communication_visable": false,
	"application_visable": false
}
```