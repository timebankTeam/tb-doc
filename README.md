# Protocol

---

## 1. Login
### Url
	/login
### Method
	Post
### Request
``` json
{
	"protocol":1,
	"token":"",
	"request":{
		"mobilePhone":"",
		"password":""
	}
}
```

### Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success; 1: user not exist; 2: password error; 3: other",
	"response":{
		"token":"",
		"accountId":""
	}
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
	"protocol":1,
	"token":"",
	"!!!commentHere":"I think that when trying to get user details, we need to identify user as well.",
	"request":{
		"userId":""
	}
}
```

### Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success;1: user not exist; 2: password error; 3: other",
	"response": {
		"nickName":"",
		"name":"",
		"sex":0,
		"!!!commentHere":"0:boy; 1: girl",
		"age":24,
		"mobilePhone":"",
		"sign":"",
		"profession":"",
		"creditLevel":"",
		"timeCoin":""
	}
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
	"protocol":1,
	"token":"",
	"request":{
		"mobilePhone":"",
		"password":""
	}
}
```

### 3.2 Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success; 1: user already exist; 2: failed",
	"response":{
		"token":"",
		"accountId":""
	}
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
	"protocol":1,
	"token":"",
	"request": {
		"accountId":"",
		"nickName":"",
		"name":"",
		"sex":0,
		"!!!commentHere:":"for sex, 0:boy; 1: girl",
		"age":24,
		"mobilePhone":"",
		"sign":"",
		"profession":"",
		"creditLevel":"",
		"timeCoin":""
	}
}
```

### Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success; 1: failed",
	"response":{
		"userId":""
	}
}
```

## 5. Get user id by account id
### Url
	/user/id
### Method
	Get
### Request
``` json
{
	"protocol":1,
	"token":"",
	"request": {
		"accountId":""
	}
}
```

### Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success; 1: failed",
	"response":{
		"userId":""
	}
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
	"protocol":1,
	"token":"",
	"request": {
		"campaignOwner":"",
		"campaignName":"",
		"startDate":"",
		"length":50,!!!单位为小时
		"timeCoin":50,
		"location":"",
		"max":20,
		"min":10,
		"contactPerson":"",
		"mobilePhone":"",
		"description":""
	}
}
```

### Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success; 1: failed",
	"response":{
		"campaignId":""
	}
}
```

## 6.2 Get activities
### Url
	/activities/list
### Method
	Get
### Request
``` json
{
	"protocol":1,
	"token":"",
	"request": {
		"campaignType":2 !!!个人活动
	}
}
```

### Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success; 1: failed",
	"response":{
		"campaignOwner":
		"campaignName":"",
		"campaignTye":2,
		"startDate":"",
		"length":50,###单位为小时
		"timeCoin":50,
		"location":"",
		"max":20,
		"min":10,
		"contactPerson":"",
		"mobilePhone":"",
		"description":"",
		"campaignStatus":1 !!!1.报名中 2.报名已满 3.进行中 4.活动结束
	}
}
```

## 6.3 Join activities
### Url
	/activities/join
### Method
	Post
### Request
``` json
{
	"protocol":1,
	"token":"",
	"request": {
		"activityId":"",
		"userId":""
	}
}
```

### Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success; 1: failed",
	"response":{
		"activityId":""
	}
}
```
