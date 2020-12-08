# 設定提現賬戶資訊

{% api-method method="post" host="http://domain name/cch2oas" path="/usr/withdrawBank" %}
{% api-method-summary %}
設定提現賬戶資料
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
系統核發的合法連線驗證資訊
{% endapi-method-parameter %}

{% api-method-parameter name="role" type="string" required=true %}
MOBILE
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
Default : zh\_CN, please reference to OAS CCHAPI doc
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="telAreaCode" type="string" required=false %}
mobile area code
{% endapi-method-parameter %}

{% api-method-parameter name="telPhoneNo" type="string" required=false %}
mobile phone no
{% endapi-method-parameter %}

{% api-method-parameter name="bankAccountName" type="string" required=true %}
戶名
{% endapi-method-parameter %}

{% api-method-parameter name="bankNo" type="string" required=true %}
 銀行流水碼
{% endapi-method-parameter %}

{% api-method-parameter name="bankAccountNo" type="string" required=true %}
 銀行賬號
{% endapi-method-parameter %}

{% api-method-parameter name="bankBranch" type="string" required=true %}
 銀行網關
{% endapi-method-parameter %}

{% api-method-parameter name="bankProvince" type="string" required=true %}
 省代碼
{% endapi-method-parameter %}

{% api-method-parameter name="bankCity" type="string" required=true %}
 市代碼
{% endapi-method-parameter %}

{% api-method-parameter name="bankOther" type="string" required=false %}
 其他銀行名稱，若選不到銀行，則手動輸入銀行名稱，bankNo請帶"0"
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
 提現賬戶設定成功
{% endapi-method-response-example-description %}

```javascript
{
    "message": "提现账户设定成功",
    "data": null,
    "exceptionCode": 0
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{   "message": "Header中没有token可验证，请确认",
    "data": null,
	  "exceptionCode": 90004
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=408 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{   "message": "Request Timeout",
    "data": null,
    "exceptionCode": 90003
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=411 %}
{% api-method-response-example-description %}
不能重複送出提現賬戶設定
{% endapi-method-response-example-description %}

```javascript
{
    "message": "欲变更请联络客服",
    "data": null,
    "exceptionCode": 10902
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{    "message": "系统问题，请联络管理员",
     "token": null,    "data": null,
	 "exceptionCode":0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



