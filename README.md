# Protocol

---

## 1. Login
### 1.1 Request
``` json
{
	"protocol":1,
	"token":"",
	"useId":"",
	"userInfo":{
		"mobileNumber":"",
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
	"token":"",
	"userId":""
}
```

---

## 2. Request Detail
### 2.1 Request
``` json
{
	"protocol":1,
	"token":"",
	"userId":"",
	"!!!commentHere":"I think that when trying to get user details, we need to identify user as well.",
	"userInfo":{
		"mobile":"",
		"password":""
	}
}
```

### 2.2 Response
``` json
{
	"protocol":1,
	"status":0,
	"!!!commentHere":"for status, 0: success;1: user not exist; 2: password error; 3: other",
	"userDetails": {
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
	"useId":"",
	"userInfo":{
		"mobile":"",
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
	"token":"",
	"userId":""
}
```

---

## 4. Add Detail
### 4.1 Request
``` json
{
	"protocol":1,
	"token":"",
	"useId":"",
	"userDetails": {
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
}
```