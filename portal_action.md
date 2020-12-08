# Portal介接手機版服務網址API

### Domain name

| 環境 | 網址 |
| :--- | :--- |
| 開發 | http://172.16.3.170:2135 |
| 測試 | http://172.16.2.23:2135 |
| 線上測試 | [https://cch2oas.ccsys.info](https://cch2oas.ccsys.info) |
| 正式區 | [https://cch2oas.ccsys.info](https://cch2oas.ccsys.info) |

{% api-method method="post" host="http://domain name/cch2oas" path="/portal/action" %}
{% api-method-summary %}
Get Url For 取得充值提現頁面url
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="lang" type="string" required=true %}
zh\_CN
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
Portal
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="portalVendorId" type="string" required=true %}
PortalVENDORID使用AES加密後\(AES/ECB/PKCS5Padding\)，再用Base64加密傳出
{% endapi-method-parameter %}

{% api-method-parameter name="portalKey" type="string" required=true %}
PortalVENDORKey使用AES加密後\(AES/ECB/PKCS5Padding\)，再用Base64加密傳出
{% endapi-method-parameter %}

{% api-method-parameter name="portalUserAccount" type="string" required=true %}
portal登入賬號
{% endapi-method-parameter %}

{% api-method-parameter name="actionPage" type="string" required=true %}
DEPOSIT：充值  
WITHDRAW：提現  
CS:在線客服
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
    "data": "http://m.cctestusr.cchdev.com/?txtToken=eyJhbGciOiJIUzI1NiJ9.eyJ2ZW5kb3JJZCI6IkNDVEVTVCIsInNpdGVJZCI6IlNJVEUxIiwiYWNjb3VudCI6IlJEMTAzIiwiZXhwIjoxNTk5NjM1Njg3fQ.rY4HOkvF9M0xOTffvBfCkOBK4BUPn9mApdOuBV39Lp4&txtPage=depositFrame",
    "resourceKey": "api.response.code.getSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}
VendorException（大股東錯誤）, 錯誤訊息會放在message
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=411 %}
{% api-method-response-example-description %}
AccountException（賬號錯誤）, 錯誤訊息會放在message
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



