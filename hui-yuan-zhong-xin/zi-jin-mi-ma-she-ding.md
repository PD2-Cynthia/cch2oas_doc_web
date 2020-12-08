# 資金密碼設定

{% api-method method="post" host="http://domain name/oascchapi" path="/usr/withdrawPassword" %}
{% api-method-summary %}
設定資金密碼
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
{% api-method-parameter name="withdrawPassword" type="string" required=true %}
 新資金密碼，請以Base64編碼傳送
{% endapi-method-parameter %}

{% api-method-parameter name="withdrawPasswordOrg" type="string" required=false %}
  若曾經設定過資金密碼，需輸入原資金密碼，比對沒問題才能更新，請以Base64編碼傳送
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
  資金密碼設定成功
{% endapi-method-response-example-description %}

```javascript
{
    "message": "密码设定成功",
    "data": null,
    "exceptionCode": 0
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{   
	"message": "Header中没有token可验证，请确认",
    "data": null,
	"exceptionCode": 90004
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=408 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{   
	  "message": "Request Timeout",
    "data": null,
    "exceptionCode": 90003
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=411 %}
{% api-method-response-example-description %}
賬戶相關錯誤訊息
{% endapi-method-response-example-description %}

```javascript
{
    "message": "旧资金密码错误，请确认",
    "data": null,
    "exceptionCode": 0
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{    
	"message": "系统问题，请联络管理员",
    "token": null,    "data": null,
	"exceptionCode":0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



