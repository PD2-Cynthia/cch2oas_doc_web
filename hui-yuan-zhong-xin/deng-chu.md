# 登出

{% api-method method="get" host="http://domain name" path="/oascchapi/usr/logout" %}
{% api-method-summary %}
logout
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
系統核發的合法連線驗證資訊
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
MOBILE
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
Default : zh\_CN
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
 成功登出
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "已完成登出",
    "token": null,
    "data": null,
    "resourceKey": "api.response.code.logout",
    "isOK": false
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=408 %}
{% api-method-response-example-description %}
 token expired, token invalid, need to relogin
{% endapi-method-response-example-description %}

```javascript
{
    "code": 408,
    "exceptionCode": 90005,
    "message": "请重新登入",
    "token": null,
    "data": null,
    "resourceKey": "api.response.token.relogin",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



