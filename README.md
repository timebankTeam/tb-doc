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
	"idNumber":"",
	"sign":"",
	"profession":"",
	"creditLevel":3,
	"timeCoin":20
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
	"status":0,
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
	"accountId":"",
	"idNumber":"",
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
	"campaignStatus":1,
	"campaignId":"",
	"isJoined":"true"
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
	/campaigns/my_joined
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
	"campaignStatus":1,
	"campaignId":""
}
```


## 6.5 Get campaigns I created
### Url
	/campaigns/my_created
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
	"campaignStatus":1,
	"campaignId":""
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
	"appraiser":"",
	"campaignId":"",
	"appraisee":"",
	"content":"",
	"score":9,
        "dateTime":100000000
}
```

### Response
``` json
{
	"status":0
}
```

## 6.7 Quit Campaign 
### Url
	/campaign/cancel
### Method
	POST
### Request
``` json
{
	"userId":"",
	"campaignId":""
}
```

### Response
``` json
{
	"status":0,
	"errorMsg":""
}
```

## 6.8 User evaluation
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

## 6.9 Get Campaign Evaluation
### Url
	/campaign/evaluations
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
        [
            {
                "avatarUrl":"",
                "content":"",
                "appraiser":"",
                "campaignId":"",
                "appraisee":"",
                "nickName":"",
                "dateTime":10000000,
                "score":10
            },
            ...
        ]
}
```

## 7. User Avatar
### 7.1 Upload Avatar
### Url
       /user/avatar
### Method
       POST
### Request
```
{
        "userId":"",
        "image":"imageFileName", fileBytes[]
}
```
### Response
``` json
{
        "status":0
}
```

### 7.2 Get Avatar
### Url
        /user/avatar
### Method
        GET
### Request
``` json
{
        "userId":""
}
```
### Response
```
fileBytes[]
```

## 8.Evalution push content
### 评价内容json格式
``` json
{
	evalutionContent:"", appraiser:"评价人的id号", appraisee:"被评价人的id"
}
```
