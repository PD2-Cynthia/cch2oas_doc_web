# 會員聊天

{% api-method method="get" host="http://domain name/cch2oas" path="/usr/message/new" %}
{% api-method-summary %}
Member talk to get customer service url from CCH platform
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
系統核發的合法連線驗證資訊
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
Default : zh\_CN, please reference to OASCCHAPI doc
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
    "data": "http://bolivb01.com/CCHUSR/EPCH330202.action?txtWebKey=f0be816dea6acc998cc733bea30bb2f7&txtMessageType=U",
    "resourceKey": "api.response.code.getSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

