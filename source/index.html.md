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

>Json Request Via POST

```json
{
	"sessionId":"1086953601",
    "productId":"123",
    "transactionId":"3424243",
    "type":"",
    "exceptions": ""
}
```

>Json Response

```json
{
  "api": "user/signup",
  "status": "OK",
  "apiMessage": "User registered successfully.",
  "packageData": {
    "txnId": "14214124",
    "subscriptionId": "213121244",
    "userId": "11567",
    "termiteAlarm": "",
    "expireDate": ""
  }
}
```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/saveTransaction

### Subscription Details

>Json Request Via POST

```json
{
	"sessionId":"1086953601",
    "type":"Single"
}
```

>Json Response

```json
{
  "api": "user/getSubscriptionDetails",
  "status": "OK",
  "apiMessage": "Subscription package fetched successfully",
  "subscriptions": [
    {
      "id": "4",
      "subscriptionId": "com.termite.1search",
      "packName": "1 Search Credit",
      "description": "1 Consumable Search Credit",
      "userType": "",
      "cost": "1.49",
      "searchCredit": "1",
      "termiteAlarm": "0",
      "packType": "Single",
      "isDisabled": "0"
    }
  ]
}
```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/saveTransaction



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

>Json Request Via POST

```json
{
  "sessionId": "76dc366a842d8ed27d27e7c44d77ef1102bf8b31",
  "productId": "1",
  "exceptions": []
}
```
>Json Response


```json
{
  "api": "user/buySubscription",
  "status": "OK",
  "apiMessage": "You Can buy This Package.",
  "expire": "0",
  "buy": "1"
}
```

<p>Description</p>

Returns a list of user purchasses, the exception param is the id's of purchases you dont want.

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/buySubscription

### Get User Action

>Json Request Via POST

```json
{
	"sessionId":"b791d232d18821d682a4f173c4b01d5d16eaada2",
    "action":"click",
    "reportId":"9200"
}
```
>Json Response


```json
{
  "api": "user/getUserAction",
  "status": "OK",
  "apiMessage": "Action Added Sucessfully"
}
```

<p>Description</p>

Returns a list of user notifications, the exception param is the id's of notifications you dont want.

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/getUserAction

### Count Notifications

>Json Request Via POST

```json
{
	"sessionId":"b791d232d18821d682a4f173c4b01d5d16eaada2",
    "action":"click",
    "reportId":"9200"
}
```
>Json Response


```json
{
  "api": "user/countNotification",
  "status": "OK",
  "apiMessage": "Notifications fetched successfully",
  "data": [],
  "notificationCount": 0
}
```

<p>Description</p>

Returns a list of user notifications, the exception param is the id's of notifications you dont want.

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/countNotification


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

>Json Request Via Post

```
{
    "sessionId": "3075bf3695c76340f2d294dc87a58389ef0bda9b"
}

```

>Json Response

```
{
  "api": "post/getInvestorSearchCount",
  "status": "OK",
  "apiMessage": "User search count fetched successfully",
  "searchCount": "1"
}

```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/getInvestorSearchCount

## Inspector Fuctions
### Get Credit Count

>Json Request Via Post

```
{
    "sessionId": "3075bf3695c76340f2d294dc87a58389ef0bda9b"
}

```

>Json Response

```
{
  "api": "inspector/getCreditCount",
  "status": "OK",
  "apiMessage": "Inspector credit count fetched successfully",
  "creditCount": "2729"
}
```
<p>Description</p>


Used to show the remaining alarm credits for the Inspectors Business Admin account.

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/getCreditCount


### Add Report

>Json Request Via Post

```
{
	"sessionId":"e67a7a0f51a08c9d301ec191a355219a72d5c883",
    "latitude":"-37.4029541",
    "longitude":"144.9731761",
    "locationTitle":"pas",
    "refrenceId": "245670",
    "termiteFound": "1",
    "termiteInPremises":"0",
    "streetNumber": "14 pretty sally drive",
    "locality":"wallan",
    "state":"victoria",
    "country":"australia",
    "postalCode":"3756"
}

```

>Json Response

```
{
  "api": "inspector/addInspectorReport",
  "status": "OK",
  "apiMessage": "Inspector report added successfully",
  "sessionId": "e67a7a0f51a08c9d301ec191a355219a72d5c883",
  "creditCount": "2729",
  "userCount": 4,
  "isNotify": 1
}
```
<p>Description</p>


This endpoint is used by Inspectors to add a termite report to Termite Registers system. It also saves the notification ready to be sent to the user with the next api call.
<p>Function</p>


Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/addInspectorReport


### Send Notification

>Json Request Via Post

```
{
	"sessionId":"e67a7a0f51a08c9d301ec191a355219a72d5c883",
    "latitude":"-37.4029541",
    "longitude":"144.9731761",
    "locationTitle":"pas",
    "refrenceId": "245670",
    "termiteFound": "1",
    "termiteInPremises":"0",
    "streetNumber": "14 pretty sally drive",
    "locality":"wallan",
    "state":"victoria",
    "country":"australia",
    "postalCode":"3756"
}

```

>Json Response

```
{
  "api": "inspector/sendNotification",
  "status": "OK",
  "apiMessage": "Notification sent.",
  "creditCount": 2725
}
```
<p>Description</p>

This endpoint is used by Inspectors send the notifications previously created to users that have alarms in a 500m radius of the report.

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/sendNotification
### Report Search

>Json Request Via Post

```
{
	"sessionId":"c2873a9a60c026fc43fecd6675964c05ce64b567",
    "latitude":"-37.4029541",
    "longitude":"144.9731761",
    "keyword":"14 pretty sally drive wallan",
    "exceptions": []
}

```

>Json Response

```
{
  "api": "inspector/inspectorReportSearch",
  "status": "OK",
  "apiMessage": "Records fetched successfully",
  "reports": [
    {
      "id": "522",
      "termiteFound": "1",
      "latitude": "-37.40295410",
      "longitude": "144.97317610",
      "businessName": "Sample",
      "termiteInPremises": "0",
      "comment": "Termites Found",
      "created_at": "2017-02-04 13:53:47",
      "businessOwnerId": "1297",
      "address": "pas",
      "locationTitle": "pas"
    }
  ],
  "reportCount": 1,
  "termiteCount": 1,
  "businessOwnerId": "1297",
  "searchCount": 3,
  "lastSearchDate": "2017-02-04"
}
```
<p>Description</p>

This endpoint is used by Inspectors send the notifications previously created to users that have alarms in a 500m radius of the report.

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/inspectorReportSearch

### Get Company Details

>Json Request Via Post

```
{
	"sessionId":"c2873a9a60c026fc43fecd6675964c05ce64b567",
    "businessOwnerId":"1297"
}

```

>Json Response

```
{
  "api": "inspector/getCompanyDetail",
  "status": "OK",
  "apiMessage": "Records fetched successfully",
  "business": [
    {
      "businessName": "Sample",
      "email": "biz1@termiteregister.com.au",
      "phone1": "15204679470",
      "isDisabled": "0",
      "image": "https://s3-ap-southeast-2.amazonaws.com/termite-staging/ecard/57c7cb76888b98.90986782.jpg"
    }
  ]
}
```
<p>Description</p>

This endpoint is used by Inspectors send the notifications previously created to users that have alarms in a 500m radius of the report.

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/getCompanyDetail


### Search Count

>Json Request Via Post

```
{
    "sessionId": "3075bf3695c76340f2d294dc87a58389ef0bda9b"
}

```

>Json Response

```
{
  "api": "inspector/getInspectorSearchCount",
  "status": "OK",
  "apiMessage": "User search count fetched successfully",
  "searchCount": "5",
  "lastSearchDate": "2017-02-04"
}

```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /user/getInspectorSearchCount


## User Property Functions
### Add Property

>Json Request Via Post

```
{
	"sessionId":"527a777f438df98dfe449cd7b802af8de9a7c85b",
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

```
{
  "api": "userProperty/addProperty",
  "status": "error",
  "errorCode": 99,
  "apiMessage": "You do not have enough termite alarm credit, Please purchase a new subscription plan."
}

```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /userProperty/addProperty
### Delete Property

>Json Request Via Post

```
{
	"sessionId":"527a777f438df98dfe449cd7b802af8de9a7c85b",
	"propertyId": "65910"
}

```

>Json Response

```
{
  "api": "userProperty/deleteProperty",
  "status": "OK",
  "apiMessage": "User Property deleted successfully"
}

```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /userProperty/deleteProperty


### Get User Property

>Json Request Via Post

```
{
    "sessionId": "3075bf3695c76340f2d294dc87a58389ef0bda9b"
}

```

>Json Response

```
{
  "api": "userProperty/getUserProperty",
  "status": "OK",
  "apiMessage": "Records fetched successfully",
  "properties": [
    {
      "address": "14 pretty sally",
      "isDisabled": "0",
      "latitude": "-37.40295410",
      "longitude": "144.97317610",
      "propertyName": "pas",
      "expireDate": null,
      "created_at": "2017-01-30 04:22:32",
      "image": null,
      "thumb": null,
      "propertyId": "65910",
      "days": null
    },
    {
      "address": "9 Pontisford Ct Kilmore VIC 3764 Australia",
      "isDisabled": "0",
      "latitude": "-37.29195638",
      "longitude": "144.93996888",
      "propertyName": "lol",
      "expireDate": "2017-08-18 04:07:23",
      "created_at": "2016-09-06 01:47:48",
      "image": "https://staging.termiteregister.com.au/images/user/57ce2044acaa63.07345327.jpg",
      "thumb": "https://staging.termiteregister.com.au/images/user/thumb/57ce2044acaa63.07345327.jpg",
      "propertyId": "65613",
      "days": "195"
    }
  ],
  "userType": "Investor"
}

```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /userProperty/getUserProperty


### Get Expired User Property

>Json Request Via Post

```
{
	"sessionId":"527a777f438df98dfe449cd7b802af8de9a7c85b"
}

```

>Json Response

```
{
  "api": "userProperty/getExpiredProperties",
  "status": "OK",
  "apiMessage": "User Property fetched successfully",
  "propertyList": []
}

```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /userProperty/getExpiredProperties


## Termite Report Function
### Get Report by property id

>Json Request Via Post

```
{
	"sessionId":"1477f498e0dca9ae721b53ac5d02bcd436e7338f",
	"propertyId":"65911",
	"exceptions":[]
}

```

>Json Response

```
{
  "api": "termiteReport/getReportbyPropertyId",
  "status": "OK",
  "apiMessage": "Records fetched successfully",
  "reports": [
    {
      "name": "Sample",
      "businessOwnerId": "1297",
      "id": "522",
      "latitude": "-37.40295410",
      "longitude": "144.97317610",
      "address": "pas",
      "locationTitle": "pas",
      "comment": "Termites Found",
      "termiteFound": "1",
      "termiteInPremises": "0",
      "created_at": "2017-02-04 13:53:47"
    }
  ]
}

```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /termiteReport/getReportbyPropertyId


### Get Inspector Report

>Json Request Via Post

```
{
	"sessionId":"2d94c475cea6f50613a385ab490e30931b275b0e",
    "exceptions":[]
}

```

>Json Response

```
{
  "api": "termiteReport/getInspectorReport",
  "status": "OK",
  "apiMessage": "Records fetched successfully",
  "reports": [
    {
      "id": "522",
      "termiteFound": "1",
      "comment": "Termites Found",
      "refrenceId": "245670",
      "created_at": "2017-02-04 13:53:47",
      "termiteInPremises": "0",
      "latitude": "-37.40295410",
      "longitude": "144.97317610",
      "address": "pas",
      "locationTitle": "pas"
    }
  ]
}

```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /termiteReport/getReportbyPropertyId


### Get Report By Lat Long

>Json Request Via Post

```
{
	"sessionId":"1477f498e0dca9ae721b53ac5d02bcd436e7338f",
    "latitude":"-37.4029541",
    "longitude":"144.9731761",
    "exceptions":[]
}

```

>Json Response

```
{
  "api": "termiteReport/getReportbyLatLong",
  "status": "OK",
  "apiMessage": "Records fetched successfully",
  "reports": [
    {
      "id": "522",
      "termiteFound": "1",
      "termiteInPremises": "0",
      "latitude": "-37.40295410",
      "longitude": "144.97317610",
      "comment": "Termites Found",
      "created_at": "2017-02-04 13:53:47",
      "name": "Sample",
      "businessOwnerId": "1297",
      "address": "pas"
    }
  ],
  "termiteCount": 1,
  "reportCount": 1,
  "searchCount": 0
}

```
<p>Description</p>

<p>Function</p>
Request Part | Value
---------- | -------
`Type` | POST
`URL` | /termiteReport/getReportbyPropertyId
