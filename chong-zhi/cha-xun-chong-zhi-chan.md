# 查詢充值單

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/deposit/data" %}
{% api-method-summary %}
取得特定單號的付款資訊
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
{% api-method-parameter name="client\_host" type="string" required=true %}
 會員登入的domain name
{% endapi-method-parameter %}

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
內容欄位同建立充值單回傳後的相關資訊，請參照之
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": {
        "applyNo": 0,
        "status": "CANCELED",
        "payType": "BANK",
        "depositType": "ALI",
        "depositNo": "123459781213",
        "depositName": "王大名",
        "bank": "支付寶",
        "branch": "eeeeeeeeeeeee",
        "province": "2222222222",
        "city": "wwwwwwwwwwww",
        "remark": null,
        "arrivalDepositAmount": 2525,
        "arrivalAmount": 2562.88,
        "orderPayAmount": 0,
        "fee": 0,
        "feeUnit": "PERCENT",
        "rewardRatio": 1.5,
        "orderRemark": "39744",
        "remarkFromBank": null,
        "currency": "RMB",
        "arrivalBankReward": 37.88,
        "arrivalFee": 0,
        "pipeBelongToAli": true,
        "showImage": true,
        "urlSelfImage": "http://cchd12.com/CCHUSR/EPCH306022.action?txtVendorBankNo=289",
        "urlAli2AliImage": "alipays://platformapi/startapp?appId=09999988&actionType=toAccount&goBack=NO&amount=2525.0&userId=8534477756988&memo=39744",
        "urlAli2BankImage": null,
        "payFlag": null,
        "paymentMethod": null,
        "payUrl": null,
        "map": null,
        "paymentNo": 0,
        "frontEndType": "DEFAULT",
        "siteDepositMessage": "业主后台充值设定",
        "cancelDepositFlag": false
    },
    "resourceKey": "api.response.code.getSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

