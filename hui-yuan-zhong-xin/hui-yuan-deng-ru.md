# 會員登入

{% api-method method="post" host="http://domain name" path="/cch2oas/usr/login" %}
{% api-method-summary %}
User Login
{% endapi-method-summary %}

{% api-method-description %}
Login in CCBao platform
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="role" type="string" required=true %}
Mobile page is "MOBILE"
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
Default is zh\_CN. Reference to OAS CCHAPI doc.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="vendorId" type="string" required=true %}
暫時先帶CYNTHIA 
{% endapi-method-parameter %}

{% api-method-parameter name="siteId" type="string" required=true %}
 暫時先帶RC
{% endapi-method-parameter %}

{% api-method-parameter name="account" type="string" required=true %}
會員賬號
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
會員輸入的密碼，encoded by MD5 
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
login success
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "会员登入成功.",
    "token": "eyJhbGciOiJIUzI1NiJ9.eyJ2ZW5kb3JJZCI6IkNDVEVTVCIsInNpdGVJZCI6IlNJVEUxIiwiYWNjb3VudCI6IkNBUFAwMiIsImV4cCI6MTU5NTQyNTY1NH0.1SslzYhpKAp0NVmLMGxYkZjtaZtSgQvQSDUWzymrFcw",
    "data": {
        "vendorId": "CCTEST",
        "siteId": "SITE1",
        "account": "CAPP02",
        "bankSet": false,
        "withdrawPasswordSet": false,
        "pause": "N",
        "quota": 0.0,
        "err": null,
        "gradeName": "VIP0",
        "unreadCount": 0  //未讀訊息個數
    },
    "resourceKey": "api.response.code.loginSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=411 %}
{% api-method-response-example-description %}
日code = 411 and exceptionCode = 10111, 10102, 10109時，data會回傳業主設定會員站連續鎖定密碼錯誤次數
{% endapi-method-response-example-description %}

```javascript
{
    "code": 411,
    "exceptionCode": 10111,
    "message": "账号不存在或密码错误",
    "token": null,
    "data": {
        "usrWrongPasswordTimes": 5
    },
    "resourceKey": "Exception.Account.AccountIsNotExistedOrPasswordError",
    "isOK": false
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "message": "系统问题，请联络管理员",
    "token": null,
    "data": null,
    "exceptionCode":0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Response body description

| 欄位 | 型態 | 說明 |
| :--- | :--- | :--- |
| vendorId | 文字 | 業主id |
| siteId | 文字 | 子網id |
| account | 文字 | 會員賬號 |
| bankSet | boolean | 銀行卡已設定，true為已設定 |
| withdrawPasswordSet | boolean | 提現密碼已設定，true為已設定 |
| pause | 文字 | Y：賬戶凍結，會員可登入、可查報表、可存提款。app需卡控不可作錢包轉換及玩遊戲。其他值:表正常狀態 |
| quota | 數字 | 錢包總額，顯示到小數點第二位 |
| personalCoupons | JSON | 依錢包代碼提供可使用優惠序號 |
| err | JSON | keyword:錢包代碼，message:錯誤訊息 |
| gradeName | String | 會員等級名稱 |

