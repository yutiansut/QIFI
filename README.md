# QIFI
Quantaxis Differential Information Flow for Finance Intergration


QIFI 协议 作为qatrader/ qapms的标准协议, 支持股票/期货市场


- 源于快期的 DIFF协议 (Differential Information Flow for Finance)
- 名称 QIFI   为 Quantaxis Differential Information Flow for Finance Intergration

- 核心字段
		-  'accounts'
		-  'events'
		-  'trades'
		-  'orders'
		-  'positions'
		-  'broker_name'
		
此协议是QUANTAXIS 未来1年以内的稳定版本, 不会更改



###  为什么要有这个协议:

主要目的是吧 策略  /  背后的账户实现解耦

策略无需关心背后的账户情况, 仅需相应的申请资源即可(如 申请模拟账户/ 申请回测账户/ 申请实盘账户/)
策略在申请完毕后, 可以直接去读取相应字段,  如 策略想获取持仓的时候 即可直接get('positions') 即为持仓字段

### 协议实例概览

```json
{
    "account_cookie" : "100010",
    "accounts" : {
        "user_id" : "100010",
        "currency" : "CNY",
        "pre_balance" : 0.0,
        "deposit" : 1000000.0,
        "withdraw" : 0.0,
        "WithdrawQuota" : 3.95252516672997e-322,
        "close_profit" : 0.0,
        "commission" : 6.84,
        "premium" : 0.0,
        "static_balance" : 1000000.0,
        "position_profit" : -80.0,
        "float_profit" : -80.0,
        "balance" : 999913.16,
        "margin" : 5472.0,
        "frozen_margin" : 5472.0,
        "frozen_commission" : 0.0,
        "frozen_premium" : 0.0,
        "available" : 988969.16,
        "risk_ratio" : 0.00547247522974895
    },
    "bank_password" : null,
    "bankid" : "SIM",
    "banks" : {
        "SIM" : {
            "id" : "SIM",
            "name" : "模拟银行",
            "bank_account" : "",
            "fetch_amount" : 0.0,
            "qry_count" : 0
        }
    },
    "broker_name" : "QUANTAXIS",
    "capital_password" : null,
    "event" : {
        "2019-09-06 21:01:36" : "登录成功",
        "2019-09-06 21:12:53" : "下单成功",
        "2019-09-06 21:14:25" : "下单成功",
        "2019-09-06 21:14:37" : "下单成功",
        "2019-09-06 21:14:57" : "成交通知,合约:SHFE.rb2001,手数:1",
        "2019-09-06 21:16:50" : "成交通知,合约:SHFE.rb2001,手数:1"
    },
    "investor_name" : "",
    "money" : 0.0,
    "orders" : {
        "QAOTG_5oAYRUI3" : {
            "seqno" : 8,
            "user_id" : "100010",
            "order_id" : "QAOTG_5oAYRUI3",
            "exchange_id" : "SHFE",
            "instrument_id" : "rb2001",
            "direction" : "SELL",
            "offset" : "OPEN",
            "volume_orign" : 1,
            "price_type" : "LIMIT",
            "limit_price" : 3426.0,
            "time_condition" : "GFD",
            "volume_condition" : "ANY",
            "insert_date_time" : NumberLong(1567775573528050636),
            "exchange_order_id" : "QAOTG_5oAYRUI3",
            "status" : "FINISHED",
            "volume_left" : 0,
            "last_msg" : ""
        },
        "QAOTG_xyVXjgcZ" : {
            "seqno" : 3,
            "user_id" : "100010",
            "order_id" : "QAOTG_xyVXjgcZ",
            "exchange_id" : "SHFE",
            "instrument_id" : "rb2001",
            "direction" : "SELL",
            "offset" : "OPEN",
            "volume_orign" : 1,
            "price_type" : "LIMIT",
            "limit_price" : 3480.0,
            "time_condition" : "GFD",
            "volume_condition" : "ANY",
            "insert_date_time" : NumberLong(1567775665377198042),
            "exchange_order_id" : "QAOTG_xyVXjgcZ",
            "status" : "ALIVE",
            "volume_left" : 1,
            "last_msg" : ""
        },
        "QAOTG_BIn7hPtG" : {
            "seqno" : 5,
            "user_id" : "100010",
            "order_id" : "QAOTG_BIn7hPtG",
            "exchange_id" : "SHFE",
            "instrument_id" : "rb2001",
            "direction" : "SELL",
            "offset" : "OPEN",
            "volume_orign" : 1,
            "price_type" : "LIMIT",
            "limit_price" : 3480.0,
            "time_condition" : "GFD",
            "volume_condition" : "ANY",
            "insert_date_time" : NumberLong(1567775677891881150),
            "exchange_order_id" : "QAOTG_BIn7hPtG",
            "status" : "ALIVE",
            "volume_left" : 1,
            "last_msg" : ""
        },
        "QAOTG_P4kEw2FJ" : {
            "seqno" : 13,
            "user_id" : "100010",
            "order_id" : "QAOTG_P4kEw2FJ",
            "exchange_id" : "SHFE",
            "instrument_id" : "rb2001",
            "direction" : "BUY",
            "offset" : "OPEN",
            "volume_orign" : 1,
            "price_type" : "LIMIT",
            "limit_price" : 3480.0,
            "time_condition" : "GFD",
            "volume_condition" : "ANY",
            "insert_date_time" : NumberLong(1567775810195686542),
            "exchange_order_id" : "QAOTG_P4kEw2FJ",
            "status" : "FINISHED",
            "volume_left" : 0,
            "last_msg" : ""
        }
    },
    "password" : "100010",
    "ping_gap" : 5,
    "portfolio" : "default",
    "positions" : {
        "SHFE_rb2001" : {
            "user_id" : "100010",
            "exchange_id" : "SHFE",
            "instrument_id" : "rb2001",
            "volume_long_today" : 1,
            "volume_long_his" : 0,
            "volume_long" : 1,
            "volume_long_frozen_today" : 0,
            "volume_long_frozen_his" : 0,
            "volume_long_frozen" : 0,
            "volume_short_today" : 1,
            "volume_short_his" : 0,
            "volume_short" : 1,
            "volume_short_frozen_today" : 0,
            "volume_short_frozen_his" : 0,
            "volume_short_frozen" : 0,
            "volume_long_yd" : 0,
            "volume_short_yd" : 0,
            "pos_long_his" : 0,
            "pos_long_today" : 1,
            "pos_short_his" : 0,
            "pos_short_today" : 1,
            "open_price_long" : 3434.0,
            "open_price_short" : 3426.0,
            "open_cost_long" : 34340.0,
            "open_cost_short" : 34260.0,
            "position_price_long" : 3434.0,
            "position_price_short" : 3426.0,
            "position_cost_long" : 34340.0,
            "position_cost_short" : 34260.0,
            "last_price" : 3432.0,
            "float_profit_long" : -20.0,
            "float_profit_short" : -60.0,
            "float_profit" : -80.0,
            "position_profit_long" : -20.0,
            "position_profit_short" : -60.0,
            "position_profit" : -80.0,
            "margin_long" : 2736.0,
            "margin_short" : 2736.0,
            "margin" : 5472.0
        }
    },
    "pub_host" : "localhost",
    "settlement" : {},
    "taskid" : null,
    "trade_host" : "127.0.0.1",
    "trades" : {
        "6" : {
            "seqno" : 7,
            "user_id" : "100010",
            "trade_id" : "6",
            "exchange_id" : "SHFE",
            "instrument_id" : "rb2001",
            "order_id" : "QAOTG_5oAYRUI3",
            "exchange_trade_id" : "6",
            "direction" : "SELL",
            "offset" : "OPEN",
            "volume" : 1,
            "price" : 3426.0,
            "trade_date_time" : NumberLong(1567775697237747424),
            "commission" : 3.42
        },
        "11" : {
            "seqno" : 12,
            "user_id" : "100010",
            "trade_id" : "11",
            "exchange_id" : "SHFE",
            "instrument_id" : "rb2001",
            "order_id" : "QAOTG_P4kEw2FJ",
            "exchange_trade_id" : "11",
            "direction" : "BUY",
            "offset" : "OPEN",
            "volume" : 1,
            "price" : 3434.0,
            "trade_date_time" : NumberLong(1567775810195972480),
            "commission" : 3.42
        }
    },
    "transfers" : {},
    "updatetime" : "2019-09-06 21:19:48.346640",
    "wsuri" : "ws://www.yutiansut.com:7988",
    "bankname" : "模拟银行",
    "trading_day" : "20190909",
    "status" : 200
 }
