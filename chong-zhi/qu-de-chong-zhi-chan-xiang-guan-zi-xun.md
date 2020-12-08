# 取得充值單相關資訊

{% api-method method="get" host="http://domain name/cch2oas" path="/usr/deposit/data" %}
{% api-method-summary %}
Get deposit form info
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
系統核發的合理連線驗證資訊
{% endapi-method-parameter %}

{% api-method-parameter name="lang" type="string" required=true %}
Default : zh\_CN, please reference to OAS CCHAPI doc
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
可填寫充值單時回傳
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": {
        "isApplyPending": false,              //是否可申請
        "depositType": {                      //充值方式
            "TRANSFER": "网银",                
            "UNIONPAY": "云闪付",
            "ALI": "支付宝",
            "WECHAT": "微信",
            "UNION": "银联"
        },
        "bankAccountName": "李小姐",                //充值人，預帶戶名
        "pipeInfo": {						 //各充值方式內含的所有管道列表
            "TRANSFER": [
                {
                    "ePayment": "PAYMENT",			//支付方式, BANK是轉賬,PAYMENT是第三方支付
                    "regionId": "CN",			
                    "entryNo": 14,					//銀行或支付管道代碼
                    "rewardRatio": 0,				//回饋金比例
                    "minLimit": 50,					//可充值最小金額
                    "maxLimit": 1000,				//可充值最大金額
                    "vendorBankPaymentNo": 367,		//銀行或支付廠商代碼
                    "fee": 10,						//手續費
                    "feeUnit": "DOLLAR",			//手續費計價單位, DOLLOR是元, PERCENT是百分比
                    "name": "中國工商銀行"			//銀行或管道顯示名稱
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 1,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 1100,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "建设银行"
                },
                {
                    "ePayment": "BANK",
                    "regionId": "CN",
                    "entryNo": 1,
                    "rewardRatio": 3.1,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 292,
                    "fee": 0,
                    "feeUnit": null,
                    "name": "建设银行"
                },
                {
                    "ePayment": "BANK",
                    "regionId": "CN",
                    "entryNo": 31,
                    "rewardRatio": 3.1,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 291,
                    "fee": 0,
                    "feeUnit": null,
                    "name": "民生银行"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 2,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "光大银行"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 3,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "美国银行"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 9,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "微信支付"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 10,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "中信銀行"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 12,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "支付寶"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 13,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 364,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "TEST"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 13,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 366,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "TEST"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 15,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "中国银行"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 21,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "邮政储蓄"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 26,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "上海银行"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 31,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "民生银行"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 32,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "华夏银行"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 35,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 10,
                    "feeUnit": "DOLLAR",
                    "name": "广东发展银行"
                },
                {
                    "ePayment": "BANK",
                    "regionId": "CN",
                    "entryNo": 14,
                    "rewardRatio": 3.1,
                    "minLimit": 50,
                    "maxLimit": 69770,
                    "vendorBankPaymentNo": 297,
                    "fee": 0,
                    "feeUnit": null,
                    "name": "中國工商銀行"
                }
            ],
            "UNIONPAY": [
                {
                    "ePayment": "BANK",
                    "regionId": "CN",
                    "entryNo": 57,
                    "rewardRatio": 2.6,
                    "minLimit": 50,
                    "maxLimit": 5000,
                    "vendorBankPaymentNo": 299,
                    "fee": 0,
                    "feeUnit": null,
                    "name": "雲閃付"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 133,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 364,
                    "fee": 0.8,
                    "feeUnit": "PERCENT",
                    "name": "雲閃付掃碼"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 133,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 365,
                    "fee": 0.8,
                    "feeUnit": "PERCENT",
                    "name": "雲閃付掃碼"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 133,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 366,
                    "fee": 0.8,
                    "feeUnit": "PERCENT",
                    "name": "雲閃付掃碼"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 134,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 365,
                    "fee": 0.8,
                    "feeUnit": "PERCENT",
                    "name": "雲閃付"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 142,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 365,
                    "fee": 0.8,
                    "feeUnit": "PERCENT",
                    "name": "雲閃付H5"
                }
            ],
            "ALI": [
                {
                    "ePayment": "BANK",
                    "regionId": "CN",
                    "entryNo": 12,
                    "rewardRatio": 1.5,
                    "minLimit": 50,
                    "maxLimit": 12000,
                    "vendorBankPaymentNo": 289,
                    "fee": 0,
                    "feeUnit": null,
                    "name": "支付寶"
                },
                {
                    "ePayment": "BANK",
                    "regionId": "CN",
                    "entryNo": 1,
                    "rewardRatio": 1.5,
                    "minLimit": 50,
                    "maxLimit": 30000,
                    "vendorBankPaymentNo": 295,
                    "fee": 0,
                    "feeUnit": null,
                    "name": "建设银行"
                },
                {
                    "ePayment": "BANK",
                    "regionId": "CN",
                    "entryNo": 31,
                    "rewardRatio": 1.5,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 291,
                    "fee": 0,
                    "feeUnit": null,
                    "name": "民生银行"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 12,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 1.5,
                    "feeUnit": "PERCENT",
                    "name": "支付寶"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 137,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 364,
                    "fee": 1.5,
                    "feeUnit": "PERCENT",
                    "name": "支付寶掃碼"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 137,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 365,
                    "fee": 1.5,
                    "feeUnit": "PERCENT",
                    "name": "支付寶掃碼"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 137,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 366,
                    "fee": 1.5,
                    "feeUnit": "PERCENT",
                    "name": "支付寶掃碼"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 138,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 365,
                    "fee": 1.5,
                    "feeUnit": "PERCENT",
                    "name": "支付寶H5"
                },
                {
                    "ePayment": "BANK",
                    "regionId": "CN",
                    "entryNo": 14,
                    "rewardRatio": 1.5,
                    "minLimit": 50,
                    "maxLimit": 69770,
                    "vendorBankPaymentNo": 297,
                    "fee": 0,
                    "feeUnit": null,
                    "name": "中國工商銀行"
                }
            ],
            "WECHAT": [
                {
                    "ePayment": "BANK",
                    "regionId": "CN",
                    "entryNo": 43,
                    "rewardRatio": 2.1,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 298,
                    "fee": 0,
                    "feeUnit": null,
                    "name": "微信"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 11,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 367,
                    "fee": 0.5,
                    "feeUnit": "DOLLAR",
                    "name": "微信"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 135,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 365,
                    "fee": 0.5,
                    "feeUnit": "DOLLAR",
                    "name": "微信掃碼"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 135,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 366,
                    "fee": 0.5,
                    "feeUnit": "DOLLAR",
                    "name": "微信掃碼"
                },
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 136,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 365,
                    "fee": 0.5,
                    "feeUnit": "DOLLAR",
                    "name": "微信H5"
                }
            ],
            "UNION": [
                {
                    "ePayment": "PAYMENT",
                    "regionId": "CN",
                    "entryNo": 139,
                    "rewardRatio": 0,
                    "minLimit": 50,
                    "maxLimit": 50000,
                    "vendorBankPaymentNo": 365,
                    "fee": 0.5,
                    "feeUnit": "PERCENT",
                    "name": "快捷支付"
                }
            ]
        },
        "hadDepositAmounts": [								//最近三次成功充值數字
            355,
            209,
            155
        ],
        "bankMessage": "转账充值设定文字",					//轉賬充值時應顯示的文字
        "depositApplyList": [								//最近五次的充值記錄
            {
                "depositApplyNo": 20022716390054,			//充值單號
                "payType": "PAYMENT",						//充值型態
                "crDate": "2020-02-27 16:54:09",			//建單日
                "remark": "銀聯支付是html 頁面",			//充值單備註
                "status": "APPROPRIATION",					//充值狀態
                "cancelDepositFlag": false,        //是否可撤單            
                "depositType": "UNION",						//充值方式
                "arrivalDepositAmount": 355,				//處理中充值金額
                "arrivalBankReward": 0,						//處理中回饋金
                "arrivalFee": 1.78,							//處理中手續費
                "arrivalAmount": 353.22,					//處理中的入賬金額
                "amount": 355,								//已充值或取消的預計充值金額
                "actualDepositAmount": 355,					//已充值或取消的實際充值金額
                "expectBankReward": 0,						//已充值或取消的預計回饋金
                "actualBankReward": 0,						//已充值或取消的實際回饋金
                "expectFee": 1.78,							//已充值或取消的預計手續費
                "actualFee": 1.78,							//已充值或取消的的實際手續費
                "expectAmount": 353.22,						//已充值或取消的預計入賬額度
                "actualAmount": 353.22,						//已充值或取消的實際入賬額度
                "currency": "RMB"							//幣別
            },
            {
                "depositApplyNo": 20022716380052,
                "payType": "PAYMENT",
                "crDate": "2020-02-27 16:52:03",
                "remark": "網銀支付成功",
                "status": "APPROPRIATION",
                "depositType": "TRANSFER",
                "arrivalDepositAmount": 209,
                "arrivalBankReward": 0,
                "arrivalFee": 10,
                "arrivalAmount": 199,
                "amount": 209,
                "actualDepositAmount": 209,
                "expectBankReward": 0,
                "actualBankReward": 0,
                "expectFee": 10,
                "actualFee": 10,
                "expectAmount": 199,
                "actualAmount": 199,
                "currency": "RMB"
            },
            {
                "depositApplyNo": 20022715770059,
                "payType": "PAYMENT",
                "crDate": "2020-02-27 15:06:35",
                "remark": "User Cancel",
                "status": "CANCELED",
                "depositType": "ALI",
                "arrivalDepositAmount": 0,
                "arrivalBankReward": 0,
                "arrivalFee": 0,
                "arrivalAmount": 0,
                "amount": 165,
                "actualDepositAmount": 0,
                "expectBankReward": 0,
                "actualBankReward": 0,
                "expectFee": 2.48,
                "actualFee": 0,
                "expectAmount": 162.52,
                "actualAmount": 0,
                "currency": "RMB"
            },
            {
                "depositApplyNo": 20022715760052,
                "payType": "PAYMENT",
                "crDate": "2020-02-27 15:05:25",
                "remark": "User Cancel",
                "status": "CANCELED",
                "depositType": "UNIONPAY",
                "arrivalDepositAmount": 0,
                "arrivalBankReward": 0,
                "arrivalFee": 0,
                "arrivalAmount": 0,
                "amount": 165,
                "actualDepositAmount": 0,
                "expectBankReward": 0,
                "actualBankReward": 0,
                "expectFee": 1.32,
                "actualFee": 0,
                "expectAmount": 163.68,
                "actualAmount": 0,
                "currency": "RMB"
            },
            {
                "depositApplyNo": 20022715750057,
                "payType": "PAYMENT",
                "crDate": "2020-02-27 15:04:35",
                "remark": "User Cancel",
                "status": "CANCELED",
                "depositType": "UNIONPAY",
                "arrivalDepositAmount": 0,
                "arrivalBankReward": 0,
                "arrivalFee": 0,
                "arrivalAmount": 0,
                "amount": 165,
                "actualDepositAmount": 0,
                "expectBankReward": 0,
                "actualBankReward": 0,
                "expectFee": 1.32,
                "actualFee": 0,
                "expectAmount": 163.68,
                "actualAmount": 0,
                "currency": "RMB"
            }
        ],
        "depositExpireFlag": "Y",                //是否顯示充值單有效期限
        "ExpireTime": 8084                       //倒數秒數

    },
    "siteDepositMessage": "业主后台充值设定",    //業主後台充值設定訊息
    "resourceKey": "api.response.code.getSuccess",
    "isOK": false
}

尚有審核單回傳範例
{
    "code": 200,
    "exceptionCode": 0,
    "message": "取得资料成功",
    "token": null,
    "data": {
        "isApplyPending": true,
        "depositType": null,
        "pipeInfo": null,
        "realName": "李小姐",
        "hadDepositAmounts": [
            355,
            209,
            155
        ],
        "bankMessage": "转账充值设定文字",
        "depositApplyList": [
            {
                "depositApplyNo": 20030308681056,
                "payType": "BANK",
                "crDate": "2020-03-03 08:49:28",
                "remark": "test",
                "status": "NOTICEABLE",
                "depositType": "ALI",
                "arrivalDepositAmount": 150,
                "arrivalBankReward": 2.25,
                "arrivalFee": 0,
                "arrivalAmount": 152.25,
                "amount": 150,
                "actualDepositAmount": 0,
                "expectBankReward": 2.25,
                "actualBankReward": 0,
                "expectFee": 0,
                "actualFee": 0,
                "expectAmount": 152.25,
                "actualAmount": 0,
                "currency": "RMB"
            },
            {
                "depositApplyNo": 20030213771050,
                "payType": "BANK",
                "crDate": "2020-03-02 13:36:49",
                "remark": "User Cancel",
                "status": "CANCELED",
                "depositType": "ALI",
                "arrivalDepositAmount": 0,
                "arrivalBankReward": 0,
                "arrivalFee": 0,
                "arrivalAmount": 0,
                "amount": 152,
                "actualDepositAmount": 0,
                "expectBankReward": 2.28,
                "actualBankReward": 0,
                "expectFee": 0,
                "actualFee": 0,
                "expectAmount": 154.28,
                "actualAmount": 0,
                "currency": "RMB"
            },
            {
                "depositApplyNo": 20030213761057,
                "payType": "BANK",
                "crDate": "2020-03-02 13:36:12",
                "remark": "User Cancel",
                "status": "CANCELED",
                "depositType": "ALI",
                "arrivalDepositAmount": 0,
                "arrivalBankReward": 0,
                "arrivalFee": 0,
                "arrivalAmount": 0,
                "amount": 152,
                "actualDepositAmount": 0,
                "expectBankReward": 2.28,
                "actualBankReward": 0,
                "expectFee": 0,
                "actualFee": 0,
                "expectAmount": 154.28,
                "actualAmount": 0,
                "currency": "RMB"
            },
            {
                "depositApplyNo": 20030211151057,
                "payType": "BANK",
                "crDate": "2020-03-02 11:56:16",
                "remark": "User Cancel",
                "status": "CANCELED",
                "depositType": "ALI",
                "arrivalDepositAmount": 0,
                "arrivalBankReward": 0,
                "arrivalFee": 0,
                "arrivalAmount": 0,
                "amount": 152,
                "actualDepositAmount": 0,
                "expectBankReward": 2.28,
                "actualBankReward": 0,
                "expectFee": 0,
                "actualFee": 0,
                "expectAmount": 154.28,
                "actualAmount": 0,
                "currency": "RMB"
            },
            {
                "depositApplyNo": 20030211141056,
                "payType": "BANK",
                "crDate": "2020-03-02 11:54:22",
                "remark": "User Cancel",
                "status": "CANCELED",
                "depositType": "ALI",
                "arrivalDepositAmount": 0,
                "arrivalBankReward": 0,
                "arrivalFee": 0,
                "arrivalAmount": 0,
                "amount": 152,
                "actualDepositAmount": 0,
                "expectBankReward": 2.28,
                "actualBankReward": 0,
                "expectFee": 0,
                "actualFee": 0,
                "expectAmount": 154.28,
                "actualAmount": 0,
                "currency": "RMB"
            }
        ],
        "depositExpireFlag": "Y",                //是否顯示充值單有效期限
        "ExpireTime": 211                       //倒數秒數
    },
    "siteDepositMessage": "业主后台充值设定",    //業主後台充值設定訊息
    "resourceKey": "api.response.code.getSuccess",
    "isOK": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

