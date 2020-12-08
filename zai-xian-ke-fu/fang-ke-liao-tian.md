# 訪客聊天

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/guest/message/new" %}
{% api-method-summary %}
Guest talk to get customer service url from CCH platform
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="lang" type="string" required=true %}
Default : zh\_CN, please reference to OASCCHAPI doc
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
MOBILE
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="vendorId" type="string" required=true %}
業主id
{% endapi-method-parameter %}

{% api-method-parameter name="siteId" type="string" required=true %}
Site id
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
訪客稱呼
{% endapi-method-parameter %}

{% api-method-parameter name="phoneNumber" type="string" required=false %}
telphone number
{% endapi-method-parameter %}

{% api-method-parameter name="qq" type="string" required=false %}
qq account
{% endapi-method-parameter %}

{% api-method-parameter name="wechat" type="string" required=false %}
微信account
{% endapi-method-parameter %}

{% api-method-parameter name="client\_host" type="string" required=true %}
user登入的domain name, 範例: cchd12.com
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

