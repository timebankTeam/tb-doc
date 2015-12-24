# Protocol
## 1.GetValidationCode
### Url
	/validationCode
### Method
	Get
### Request
``` json
{
	"mobilePhone":"xxxxxx"
}
```
### Response
``` json
{
	"validationCode":"",
	"status":
}
```
---

## 2. Request Detail
### Url
	/user/detail
### Method
	Get
### Request
``` json
{
	"userId":"xxxxxx"
}
```

### Response
``` json
{
	"nickName":"",
	"name":"",
	"sex":0,
	"age":24,
	"mobilePhone":"",
	"sign":"",
	"profession":"",
	"creditLevel":"",
	"timeCoin":""
}
```

---

## 3. Regist
### Url
	/regist
### Method
	Post
### Request
``` json
{
	"mobilePhone":"",
	"validationCode":"xxxxx"

}
```

### 3.2 Response
``` json
{
	"status":0
	"userId":"xxxxxxx"
}
```

---

## 4. Add Detail
### Url
	/user/detail
### Method
	Post
### Request
``` json
{
	"nickName":"",
	"name":"",
	"sex":0,
	"age":24,
	"mobilePhone":"",
	"sign":"",
	"profession":""
}
```

### Response
``` json
{

	"userId":""

}
```

# 6.campaigns
## 6.1 Create campaign
### Url
	/campaigns/create
### Method
	Post
### Request
``` json
{
	"campaignOwner":"",
	"campaignName":"",
	"startDate":"",
	"length":50,
	"timeCoin":50,
	"location":"",
	"max":20,
	"min":10,
	"contactPerson":"",
	"mobilePhone":"",
	"description":""
}
```

### Response
``` json
{
	"status":""
}
```

## 6.2 Get campaigns
### Url
	/campaigns/list
### Method
	Get
### Request
``` json
{
	"campaignType":2
}
```

### Response
``` json
{
	"campaignOwner":"",
	"campaignName":"",
	"campaignTye":2,
	"startDate":1400000000,
	"length":50,
	"timeCoin":50,
	"location":"",
	"max":20,
	"min":10,
	"contactPerson":"",
	"mobilePhone":"",
	"description":"",
	"campaignStatus":1
}
```

## 6.3 Join campaigns
### Url
	/campaigns/join
### Method
	Post
### Request
``` json
{
	"campaignId":"",
	"userId":""
}
```

### Response
``` json
{
	"status":
}
```


## 6.4 Get my campaigns
### Url
	/campaigns/joined
### Method
	Get
### Request
``` json
{
	"userId":""
}
```

### Response
``` json
{
	"campaignOwner":"",
	"campaignName":"",
	"campaignTye":2,
	"startDate":1400000000,
	"length":50,
	"timeCoin":50,
	"location":"",
	"max":20,
	"min":10,
	"contactPerson":"",
	"mobilePhone":"",
	"description":"",
	"campaignStatus":1
}
```


## 6.5 Get campaigns I created
### Url
	/campaigns/created
### Method
	Get
### Request
``` json
{
	"userId":""
}
```

### Response
``` json
{
	"campaignOwner":"",
	"campaignName":"",
	"campaignTye":2,
	"startDate":1400000000,
	"length":50,
	"timeCoin":50,
	"location":"",
	"max":20,
	"min":10,
	"contactPerson":"",
	"mobilePhone":"",
	"description":"",
	"campaignStatus":1
}
```

## 6.6 Campaign evaluation
### Url
	/campaign/evaluation
### Method
	POST
### Request
``` json
{
	"userId":"",
	"campaignId":"",
	"campaignOwner":"",
	"comments":"",
	"starLevel":""
}
```

### Response
``` json
{
	"status":0
}
```


## 6.7 User evaluation
### Url
	/user/evaluation
### Method
	POST
### Request
``` json
{
	"userId":"",
	"campaignId":"",
	"campaignOwner":"",
	"comments":"",
	"starLevel":""
}
```

### Response
``` json
{
	"status":0
}
```

## 6.8 Evaluation
### Url
	/campaign/users
### Method
	GET
### Request
``` json
{
	"campaignId":""
}
```

### Response
``` json
{
	"userId":"",
	"userName":"",
	"nickName":""
}
```
