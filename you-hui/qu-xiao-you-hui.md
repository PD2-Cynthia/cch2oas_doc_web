# 取消優惠

{% api-method method="post" host="http://domain name/cch2oas" path="/coupon/cancel" %}
{% api-method-summary %}
cancel coupon
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="role" type="string" required=true %}
APP
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=true %}
請代入合法token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="seqNo" type="number" required=true %}
coupon優惠序號\(常態稽核時若有優惠，請帶優惠回傳的序號seqNo\) 
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

