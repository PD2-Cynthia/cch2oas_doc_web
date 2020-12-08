# 常態稽核記錄

{% api-method method="get" host="http://domain name/cch2oas" path="/usr/withdraw/audit" %}
{% api-method-summary %}
Get withdraw audit infomation for user 
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
        "beginDate": "2020-06-05 11:17:01",    //開始日期
        "endDate": "2020-07-27 17:19:44",      //結束日期    
        "auditViews": [
            {
                "crTime": "2020-07-27 16:05:46",  //建立日期
                "transType": "DEPOSIT",            //交易子科目
                "amount": "1,488",                 //交易金額
                "targetAmount": 1488.0,            //目標洗碼量
                "betAmount": "0",                  //累積有效洗碼量
                "adminFee": 148.8,                 //行政費用
                "isPass": false                    //稽核狀態
            }
        ],
        "couponView": [{        //執行中優惠
            "beginDate": "2020-07-28 16:26:16",    //優惠開始時間
            "endDate": "2020-07-29 16:26:16",      //優惠結束時間
            "validDays": 1,                        //執行天數
            "favorAmount": 50.0,                   //優惠金
            "effectiveBetAmount": 0.0,             //目前洗碼量
            "targetBetAmount": 250.0,              //目標洗碼量    
            "currentCoupon": 0.0,                  //目前優惠金
            "profit": 0.0,                         //優惠盈利
            "isCancelable": true                   //true：可取消優惠
        },
        {
                "beginDate": "2020-08-17 11:45:31",
                "endDate": "2020-08-18 11:45:31",
                "seqNo": 104,
                "validDays": 1,
                "favorAmount": 888.0,
                "effectiveBetAmount": 0.0,
                "targetBetAmount": 4440.0,
                "currentCoupon": 438.54,
                "profit": 0.0,
                "isCancelable": false,
                "status": "OVERDUE"
            },
            {
                "beginDate": "2020-08-13 15:55:04",
                "endDate": "2020-08-14 15:55:04",
                "seqNo": 103,
                "validDays": 1,
                "favorAmount": 555.0,
                "effectiveBetAmount": 0.0,
                "targetBetAmount": 2775.0,
                "currentCoupon": 555.0,
                "profit": 0.0,
                "isCancelable": false,
                "status": "CANCELED"
            }
            ],
        "totalEffectiveBetAmount": 0.0,            //總累積有效洗碼量
        "totalTargetAmount": 3406.01               //總目標洗碼量
    },
    "resourceKey": "api.response.code.getSuccess",
    "isOK": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

