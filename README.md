# Protocol

---

## 1. Login
### 1.1 Request
``` json
{
	"protocol":1,
	"token":"",
	"loginRequest":{
		"mobilePhone":"",
		"password":""
	}
}
```

### 1.2 Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success; 1: user not exist; 2: password error; 3: other",
	"loginResponse":{
		"token":"",
		"accountId":""
	}
}
```

---

## 2. Request Detail
### 2.1 Request
``` json
{
	"protocol":1,
	"token":"",
	"!!!commentHere":"I think that when trying to get user details, we need to identify user as well.",
	"userDetailRequest":{
		"userId":""
	}
}
```

### 2.2 Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success;1: user not exist; 2: password error; 3: other",
	"userDetailResponse": {
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
### 3.1 Request
``` json
{
	"protocol":1,
	"token":"",
	"registRequest":{
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
	"registResponse":{
		"token":"",
		"accountId":""
	}
}
```

---

## 4. Add Detail
### 4.1 Request
``` json
{
	"protocol":1,
	"token":"",
	"createUserDetailRequest": {
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

### 4.2 Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success; 1: failed",
	"createUserDetailResponse":{
		"userId":""
	}
}
```

##5. Get user id by account id
### 5.1 Request
``` json
{
	"protocol":1,
	"token":"",
	"GetUserIdRequest": {
		"accountId":""
	}
}
```

### 5.2 Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success; 1: failed",
	"GetUserIdResponse":{
		"userId":""
	}
}
```
