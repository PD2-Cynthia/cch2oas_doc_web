# 進行提現

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/withdraw/add" %}
{% api-method-summary %}
apply a new withdraw information
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
APP, MOBILE
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="amount" type="string" required=true %}
 數字，需大於0
{% endapi-method-parameter %}

{% api-method-parameter name="withdrawPassword" type="string" required=true %}
 資金密碼\(請以MD5編碼後傳送\)
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
    "data": {
        "withdrawNo": 2007271705018,    //提現單號
        "status": "WAIT",               //提現單狀態
        "amount": 500.0,                //提現金額
        "adminFee": 251,                //行政費用
        "usrFee": 0.0,                  //手續費
        "crTime": "2020-07-27 17:04:40",    //提現單建立時間
        "paidAmount": "249",
        "usrMsg":"測試留言"            
    },
    "resourceKey": "api.response.code.getSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

