# 取消充值單

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/deposit/cancel" %}
{% api-method-summary %}
cancel a deposit information
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
Default : zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
MOBILE
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="depositApplyNo" type="integer" required=true %}
 數字
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
    "message": "取消成功",
    "token": null,
    "data": null,
    "resourceKey": "api.response.code.cancelWithdrawSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

