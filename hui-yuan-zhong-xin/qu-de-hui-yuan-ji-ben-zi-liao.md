# 取得會員基本資料

### 2020/10/7 modified:

realName-&gt;nickName 

isValidateName移除

{% api-method method="get" host="http://domain name/cch2oas" path="/usr/data" %}
{% api-method-summary %}
Get member's data
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
系統核發的合理連線驗證資訊
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
Default : zh\_CN, please reference to OAS CCHAPI doc
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
MOBILE
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": {
        "account": "CAPP06",
        "yearBirthday": "",
        "monthBirthday": "",
        "dayBirthday": "",
        "nickName": "APP06先生",
        "telAreaCode": "86",
        "telPhoneNo": "078457789",
        "email": "",
        "weChat": "",
        "qqAccount": "",
        "isValidateMail": false,
        "isValidateTel": false,
        "isValidateWechat": false,
        "isValidateQQ": false,
        "isValidateWithdraw": false
    },
    "resourceKey": "api.response.code.getSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

