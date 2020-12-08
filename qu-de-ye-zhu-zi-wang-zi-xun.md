# 取得業主子網資訊

{% api-method method="get" host="http://domain name/cch2oas/usr" path="/site?domain={serverName}" %}
{% api-method-summary %}
Get vendor ID and site ID
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="lang" type="string" required=true %}
Default : zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
MOBILE
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="serverName" type="string" required=true %}
會員連結的網址server name，例如cc-bao.com  
測試時，可用host設定你的網站名稱為cynthia.cchdev.com
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "code": 200,
    "exceptionCode": 0,
    "message": "OK",
    "token": null,
    "data": {
        "vendorId": "CCTEST",
        "siteId": "SITE1",
        "userAgent": null,
        "ip": null,
        "desktop_url": "cctestusr2.cch.com"      //導向的桌機版會員網址
    },
    "resourceKey": "取得资料成功",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



