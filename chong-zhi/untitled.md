# 建立充值單

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/deposit/add" %}
{% api-method-summary %}
create a deposit form for bank
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
domain name, ex. cchd12.com
{% endapi-method-parameter %}

{% api-method-parameter name="depositor" type="string" required=true %}
充值人 
{% endapi-method-parameter %}

{% api-method-parameter name="payType" type="string" required=true %}
該管道的屬性, Bank\(轉賬\) or Payment\(支付\)
{% endapi-method-parameter %}

{% api-method-parameter name="entryNo" type="integer" required=true %}
管道流水碼
{% endapi-method-parameter %}

{% api-method-parameter name="remark" type="string" required=true %}
會員提示
{% endapi-method-parameter %}

{% api-method-parameter name="depositType" type="string" required=true %}
充值方式
{% endapi-method-parameter %}

{% api-method-parameter name="vendorBankPaymentNo" type="integer" required=true %}
 業主轉賬支付帳戶流水號
{% endapi-method-parameter %}

{% api-method-parameter name="amount" type="integer" required=true %}
 數字，整數
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
        "applyNo": 20032515209151,        //充值單號
        "depositApplyNo": 5190,           //充值流水碼
        "status": "NOTICEABLE",							//狀態，可參照OAS CCHAPI章節說明
        "cancelDepositFlag":false,,
        "payType": "BANK",								//付款方式
        "depositType": "ALI",							//充值方式	
        "depositNo": "123459781213",					//戶號
        "depositName": "王大名",						//戶名
        "bank": "支付寶",								//銀行或支付方名稱
        "branch": "eeeeeeeeeeeee",						//網關
        "province": "2222222222",						//省
        "city": "wwwwwwwwwwww",							//市
        "remark": null,									//備註
        "arrivalDepositAmount": 2525,					//充值金額
        "arrivalAmount": 2562.88,						//到賬金額
        "orderPayAmount": 0,							//訂單付款金額（支付用）
        "fee": 0,										//手續費計算基準
        "feeUnit": "PERCENT",							//手續費計算單位：PERCENT %, DOLLOR  元
        "rewardRatio": 1.5,								//回饋金比例
        "orderRemark": "49801",							//在轉賬時為附言，在支付時為訂單編號
        "remarkFromBank": null,							//轉賬會員提示
        "currency": "RMB",
        "arrivalBankReward": 37.88,						//回饋金額
        "arrivalFee": 0,								//手續費        
        "pipeBelongToAli": true,						//管道是否為支付寶
        "showImage": true,								//是否顯示二維碼圖檔
        "urlSelfImage": "http://cchd12.com/CCHUSR/EPCH306022.action?txtVendorBankNo=289", //自行上傳圖檔網址
        "urlAli2AliImage": "alipays://platformapi/startapp?appId=09999988&actionType=toAccount&goBack=NO&amount=2525.0&userId=8534477756988&memo=49801",// 支付寶轉銀行的二維條碼網址
        "urlAli2BankImage": null,						//支付寶轉銀行的二維條碼網址
        "payFlag": null,								//Y:為已付款, N:未付款
        "paymentMethod": null,							//付款網址轉址方式
        "payUrl": null,									//付款網址
        "map": null,									//付款參數
        "paymentNo": 0,
        "frontEndType": "DEFAULT"
    },
    "siteDepositMessage": "业主后台充值设定",     //業主充值設定訊息
    "resourceKey": "api.response.code.getSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

