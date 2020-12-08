# 會員註冊

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/add" %}
{% api-method-summary %}
Register a new member
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="role" type="string" required=true %}
MOBILE
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
Default : zh\_CN, please reference to OAS CCHAPI doc
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="partnerId" type="string" required=false %}
 推廣連結代入的partnerId
{% endapi-method-parameter %}

{% api-method-parameter name="vendorId" type="string" required=true %}
業主代碼
{% endapi-method-parameter %}

{% api-method-parameter name="siteId" type="string" required=true %}
 子網代碼
{% endapi-method-parameter %}

{% api-method-parameter name="account" type="string" required=true %}
 賬號
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
 密碼以Base64傳送
{% endapi-method-parameter %}

{% api-method-parameter name="url" type="string" required=true %}
功能頁面網址
{% endapi-method-parameter %}

{% api-method-parameter name="domain" type="string" required=true %}
server name \(ex. cc-bao.com\)，不需要給http or https and  "/"  
目前測試網址可以給cynthia.cchdev.com
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
註冊成功，API Server並同時登入，給予token，並回傳與登入相關的訊息內容
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "注册成功",
    "token": "eyJhbGciOiJIUzI1NiJ9.eyJ2ZW5kb3JJZCI6IkNDVEVTVCIsInNpdGVJZCI6IlNJVEUxIiwiYWNjb3VudCI6IkNBUFAwNCIsImV4cCI6MTU5NTQ3ODg2Mn0.nC_N9HEh0tyZwdh-z6E8Rlyr7U14lOXYeL1OwHRYRVA",
    "data": {
        "vendorId": "CCTEST",
        "siteId": "SITE1",
        "account": "CAPP04",
        "bankSet": false,
        "withdrawPasswordSet": false,
        "pause": "N",
        "quota": 0.0,
        "err": null,
        "gradeName": "VIP0"
    },
    "resourceKey": "api.response.code.addUserSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



