---
title: Termite Register Api Reference Documents

language_tabs:
  - Json

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Termite Register API endpoint Documentation, here we will demonstrate ways you can connect to our API to interact with the Termite Register data sets.
Our Api is REST Based.

At this current time we only have Raw Json Information with other language bindings in the works.

# API Authentication

> To authorize, use this code:

```json
{
    "credentials": {
    "institution": "bank_of_captcha",
    "username": "12345678",
    "password": "TestMyMoney",
    "captcha": "D49ZHN"
    }
}

```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>


# Api Function
## User Authentication
### Login

>Json Request Via POST

```json
{
    "deviceToken":"354321073229033",
    "deviceType":"android",
    "email":"test@example.com",
    "password":"helloworld1"
}
```
>Json Response


```json
{
  "api": "user/signin",
  "status": "OK",
  "apiMessage": "User signed in successfully",
  "user": {
    "id": "1298",
    "role": "Inspector",
    "userType": null,
    "email": "test@example.com",
    "address": null,
    "facebookId": null,
    "name": "jack",
    "lastName": null,
    "image": null,
    "subscriptionId": null,
    "businessOwnerId": "1297",
    "alarmLimit": "0",
    "usedAlarm": "0",
    "phone1": "9182123123123",
    "abn": null,
    "licenceNo": "123123123123123123",
    "inspectorLimit": "0",
    "renew": "0",
    "status": "0",
    "paymentDone": "0",
    "isDisabled": "0",
    "disableReason": null,
    "isConfirmed": "1",
    "confirmationCode": null,
    "isPassReset": "0",
    "searchCredit": "5",
    "lastSearchDate": "2017-01-27",
    "termiteAlarm": "0",
    "assetAlarm": "0",
    "propertyAdded": "0",
    "created_at": "2016-08-18 03:14:59",
    "updated_at": "2017-01-27 06:13:58",
    "reportCount": "7",
    "paymentExpire": "2017-08-17",
    "isNotify": "0"
  },
  "sessionId": "b3b1a9beaf9a51f739853266f8e17f79445dac5d"
}
```

<p><b>DESCRIPTION</b></p>

This Signs you into Termite Registers system.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>


<p><b>FUNCTION</b></p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/signin

<p><b>REQUEST BODY</b></p>

<p><b>RESPONSE</b></p>

### Sign Up

>Json Request Via POST

```json
{
    "email": "test@example.com",
    "password": "helloworld1",
    "name": "john smith",
    "password": "helloworld1",
    "address": "123 smith street",
    "deviceToken": "12345678",
    "deviceType": "android"
}
```

>Json Response

```json
{
  "api": "user/signup",
  "status": "OK",
  "apiMessage": "User registered successfully.",
  "user": {
    "id": "1537",
    "role": "User",
    "userType": "Standard",
    "email": "test@example.com",
    "address": null,
    "facebookId": null,
    "name": "john smith",
    "lastName": null,
    "image": null,
    "subscriptionId": "1",
    "businessOwnerId": null,
    "alarmLimit": "0",
    "usedAlarm": "0",
    "phone1": null,
    "abn": null,
    "licenceNo": null,
    "inspectorLimit": "0",
    "renew": "1",
    "status": "0",
    "paymentDone": "0",
    "isDisabled": "0",
    "disableReason": null,
    "isConfirmed": "0",
    "confirmationCode": "TKXS9pHrnyrw",
    "isPassReset": "0",
    "searchCredit": "1",
    "lastSearchDate": null,
    "termiteAlarm": "0",
    "assetAlarm": "0",
    "propertyAdded": "1",
    "created_at": "2017-01-27 14:34:30",
    "updated_at": "2017-01-27 14:34:30",
    "reportCount": "0",
    "paymentExpire": null,
    "isNotify": "0"
  },
  "sessionId": "3075bf3695c76340f2d294dc87a58389ef0bda9b"
}
```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/signup

### Sign In With Facebook

>Json Request Via POST

```json
{
	"facebookId":"59017154",
    "deviceToken":"354321073229033",
    "deviceType":"android",
    "email":"dylan.aird595@gmail.com"
}
```
>Json Response


```json
{
  "api": "user/signin",
  "status": "OK",
  "apiMessage": "User signed in successfully",
  "user": {
    "id": "1298",
    "role": "Inspector",
    "userType": null,
    "email": "test@example.com",
    "address": null,
    "facebookId": null,
    "name": "jack",
    "lastName": null,
    "image": null,
    "subscriptionId": null,
    "businessOwnerId": "1297",
    "alarmLimit": "0",
    "usedAlarm": "0",
    "phone1": "9182123123123",
    "abn": null,
    "licenceNo": "123123123123123123",
    "inspectorLimit": "0",
    "renew": "0",
    "status": "0",
    "paymentDone": "0",
    "isDisabled": "0",
    "disableReason": null,
    "isConfirmed": "1",
    "confirmationCode": null,
    "isPassReset": "0",
    "searchCredit": "5",
    "lastSearchDate": "2017-01-27",
    "termiteAlarm": "0",
    "assetAlarm": "0",
    "propertyAdded": "0",
    "created_at": "2016-08-18 03:14:59",
    "updated_at": "2017-01-27 06:13:58",
    "reportCount": "7",
    "paymentExpire": "2017-08-17",
    "isNotify": "0"
  },
  "sessionId": "b3b1a9beaf9a51f739853266f8e17f79445dac5d"
}
```

<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/signin

### Logout

>Json Request Via Post

```
{
    "sessionId": "3075bf3695c76340f2d294dc87a58389ef0bda9b"
}

```

>Json Response

```
{
  "api": "user/logout",
  "status": "OK",
  "apiMessage": "User logged out successfully."
}

```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/logout



## Email And Password Functions
### Validate Email

>Json Request Via Post

```
{
    "email": "test@email.com"
}

```

>Valid Email Json Response

```
{
  "api": "user/validateEmail",
  "status": "OK",
  "apiMessage": "Email is unique"
}

```

>Invalid Email Json response

```
{
  "api": "user/validateEmail",
  "status": "error",
  "errorCode": 99,
  "apiMessage": "The email has already been taken."
}


```

<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/validateEmail

### Resend Email

>Json Request Via Post

```
{
    "email": "test@email.com"
}

```

>Valid Email Json Response

```
{
  "api": "user/resendEmail",
  "status": "OK",
  "apiMessage": "We have sent you a verification link to your email address. Please verify your email address."
}

```

>Invalid Email Json response

```
{
  "api": "user/resendEmail",
  "status": "error",
  "errorCode": 99,
  "apiMessage": "Email does not exist."
}


```

<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/resendEmail

### Email Subscription

>Json Request Via Post

```
{
	"subscribe": "1",
	"sessionId": "4ffbc4d8ace74c8d384041381b28cd653e4789da"
}

```

>Valid Email Json Response

```
{
  "api": "user/emailSubscription",
  "status": "OK",
  "apiMessage": "Your have successfully unsubscribed email notification alert.",
  "isNotify": "1"
}

```

<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/emailSubscription

### Reset Passsword

>Json Request Via Post

```
{
	"email":"test@emample.com"
}

```

>Valid Email Json Response

```
{
  "api": "user/changePassword",
  "status": "OK",
  "apiMessage": "We have emailed your temporary password. Please note that you have consumed 1 of 5 attempts today."
}

```

<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/resetPassword

### Change Password

>Json Request Via Post

```
{
	"oldPassword":"helloworld1",
	"newPassword":"helloworld2",
	"sessionId": "4ffbc4d8ace74c8d384041381b28cd653e4789da"
}

```

>Valid Email Json Response

```
{
  "api": "user/changePassword",
  "status": "OK",
  "apiMessage": "Password changed"
}

```

<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/changePassword


## User Functions
### Update Location

>Json Request Via POST

```json
{
    "sessionId":"76dc366a842d8ed27d27e7c44d77ef1102bf8b31",
    "name":"John",
    "address":"14 pretty sally drive wallan",
    "latitude":"-37.4029541",
    "longitude":"144.9731761",
    "propertyName":"pas",
    "propertyAddress":"14 pretty sally",
    "locality":"wallan",
    "state":"victoria",
    "country":"australia",
    "postalCode":"3756",
    "streetAddress":"14 pretty sally drive"
}
```
>Json Response


```json
{
  "api": "user/updateLocation",
  "status": "OK",
  "apiMessage": "User registered successfully",
  "user": {
    "id": "1221",
    "role": "User",
    "userType": "Investor",
    "email": "dylan.aird595@gmail.com",
    "address": "14 pretty sally drive wallan",
    "facebookId": "59017154",
    "name": "John",
    "lastName": null,
    "image": null,
    "subscriptionId": "17",
    "businessOwnerId": null,
    "alarmLimit": "0",
    "usedAlarm": "0",
    "phone1": null,
    "abn": null,
    "licenceNo": null,
    "inspectorLimit": "0",
    "renew": "0",
    "status": "0",
    "paymentDone": "0",
    "isDisabled": "0",
    "disableReason": null,
    "isConfirmed": "1",
    "confirmationCode": null,
    "isPassReset": "2",
    "searchCredit": "1",
    "lastSearchDate": null,
    "termiteAlarm": "0",
    "assetAlarm": "0",
    "propertyAdded": "1",
    "created_at": "2016-08-02 00:00:33",
    "updated_at": "2017-01-30 04:23:16",
    "reportCount": "0",
    "paymentExpire": "2017-08-18",
    "isNotify": "0"
  },
  "sessionId": "76dc366a842d8ed27d27e7c44d77ef1102bf8b31"
}
```

<p>Description</p>

Updates user property and registers the user after confirmation email has been sent.

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/updateLocation




### Get Notification

>Json Request Via POST

```json
{
  "sessionId": "76dc366a842d8ed27d27e7c44d77ef1102bf8b31",
  "exceptions": [ "0", "1"]
}
```
>Json Response


```json
{
  "api": "user/getNotification",
  "status": "OK",
  "apiMessage": "Notifications fetched successfully",
  "notifications": [
    {
      "companyName": "klo",
      "id": "21753",
      "receiverId": "1221",
      "reportId": "474",
      "message": "lol",
      "userId": "1281",
      "propertyId": "65613",
      "isCalled": "0",
      "isEmailed": "0",
      "isClicked": "1",
      "isCancelled": "1",
      "callDateTime": null,
      "emailDateTime": null,
      "clickDateTime": "2017-01-29 12:16:13",
      "cancelDateTime": "2017-01-29 12:16:14",
      "isNotified": "1",
      "isEmailSent": "0",
      "isRead": "1",
      "status": "1",
      "termiteFound": "1",
      "created_at": "2016-10-07 08:23:08"
    },
    {
      "companyName": "YOUR BUSINESS NAME",
      "id": "17950",
      "receiverId": "1221",
      "reportId": "243",
      "message": "lol",
      "userId": "1190",
      "propertyId": "65613",
      "isCalled": "0",
      "isEmailed": "0",
      "isClicked": "1",
      "isCancelled": "1",
      "callDateTime": null,
      "emailDateTime": null,
      "clickDateTime": "2016-09-08 15:37:10",
      "cancelDateTime": "2016-09-08 15:37:14",
      "isNotified": "1",
      "isEmailSent": "0",
      "isRead": "1",
      "status": "1",
      "termiteFound": "1",
      "created_at": "2016-09-07 03:22:13"
    }
  ]
}
```

<p>Description</p>

Returns a list of user notifications, the exception param is the id's of notifications you dont want.

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/getNotifications


### Save Transaction
### Subscription Details
### Current Status

>Json Request Via Post

```
{
	"sessionId": "4ffbc4d8ace74c8d384041381b28cd653e4789da"
}

```

>Valid Email Json Response

```
{
  "api": "user/getCurrentStatus",
  "status": "OK",
  "apiMessage": "Subscription package fetched successfully",
  "searchCredit": "1",
  "availableAlarm": 1,
  "remainingAlarm": "0",
  "isExpired": 0,
  "freePropertyCount": 0
}

```

<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/getCurrentStatus


### Purchase History

>Json Request Via POST

```json
{
  "sessionId": "76dc366a842d8ed27d27e7c44d77ef1102bf8b31",
  "exceptions": [ "0", "1"]
}
```
>Json Response


```json
{
  "api": "user/getPurchaseHistory",
  "status": "OK",
  "apiMessage": "Purchanse History fetched successfully",
  "purchaseHistory": [
    {
      "id": "53",
      "quantity": "1",
      "packName": "1 Residential Property Alarm",
      "packType": "Annual",
      "description": "Alarm Notification Subscription for 1 Residential Building",
      "created_at": "2016-09-06 01:47:48",
      "expireDate": "2017-08-18 04:07:23"
    }
  ]
}
```

<p>Description</p>

Returns a list of user purchasses, the exception param is the id's of purchases you dont want.

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/getPurchaseHistory

### Purchase Subscription
### Get User Action
### Count Notifications
### Reset User Badage

>Json Request Via POST

```json
{
  "sessionId": "76dc366a842d8ed27d27e7c44d77ef1102bf8b31"
}
```
>Json Response


```json
{
  "api": "user/resetUserBadage",
  "status": "OK",
  "apiMessage": "User badage reset successfully"
}
```

<p>Description</p>

Returns a list of user notifications, the exception param is the id's of notifications you dont want.

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/getNotifications
### Restore Transaction
### Investor Search Count

## Inspector Fuctions
### Get Credit Count
### Add Report
### Send Notification
### Report Search
### Inspector Company Details
### Get Company Detail
### Search Count
## User Property Functions
### Add Property
### Delete Property
### Get User Property
### Get Expired User Property
## Termite Report Function
### Get Report
### Get Inspector Report
### Get Report By Lat Long
