# 變更密碼

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/password" %}
{% api-method-summary %}
Change user password
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
系統核發的合法連線token
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
MOBILE
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
default is zh\_CN, please reference to OAS CCHAPI
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="password" type="string" required=true %}
會員的舊密碼,，encode by MD5
{% endapi-method-parameter %}

{% api-method-parameter name="newPassword" type="string" required=true %}
 會員的新密碼，encode by Base64
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "密码设定成功",
    "token": null,
    "data": null,
    "resourceKey": "api.response.code.passwordSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

