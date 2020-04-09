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

communication_visable 为bool类型。

如果值为false，则表示不展示在客户端通讯服务器列表中。

如果值为true或者字段不存在，则表示展示在客户端通讯服务器列表中。

### 增加application_visable

application_visable 为bool类型。

如果值为false，则表示不展示在客户端应用服务器列表中。

如果值为true或者字段不存在，则表示展示在客户端应用服务器列表中。

## 示例

extension字段示例：

```json
{
	"communication_visable": false,
	"application_visable": false
}
```

完整的IPAL声明：

```json
  {
  	"operator_address": "nch10jzpt32gwradv9mcnr6fuuj0tnx7rq0psmmtju",
  	"moniker": "netcloth-official",
  	"website": "netcloth.org",
  	"details": "netcloth-official",
  	"extension": "{\"communication_visable\": false,\"application_visable\": true}",
  	"endpoints": [{
  			"type": "1",
  			"endpoint": "http://47.104.189.5"
  		},
  		{
  			"type": "3",
  			"endpoint": "http://47.90.5.138"
  		},
  		{
  			"type": "4",
  			"endpoint": "{\"miniAppDomains\":[{\"moniker\":\"NetCloth Blog\",\"domain\":\"https://blog.netcloth.org\"},{\"moniker\":\"链闻社\",\"domain\":\"https://www.chainnews.com/\"},{\"moniker\":\"非小号\",\"domain\":\"https://feixiaohao.com\"},{\"moniker\":\"金财快讯\",\"domain\":\"https://m.jinse.com/lives\"},{\"moniker\":\"NetCloth Blog\",\"domain\":\"https://medium.com/@NetCloth/\"},{\"moniker\":\"Coindesk\",\"domain\":\"https://www.coindesk.com\"},{\"moniker\":\"Coinmarketcap\",\"domain\":\"https://www.coinmarketcap.com \"}]}"
  		}
  	],
  	"bond": {
  		"denom": "pnch",
  		"amount": "0"
  	}
  }
  ```