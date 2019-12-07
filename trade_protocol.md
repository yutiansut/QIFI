# QIFI Trade

交易协议

本协议支持股票和期货市场

## 概述:


qifi的交易协议主要是包括:

- 从eventmq上接受订单
- 从http[RESTful API] 上接受订单


- 通过websocket发送出去


## sendorder

sendorder 是发单选项, 里面有一些固定参数:


- account_cookie  账户名称
- order_direction 订单方向
- order_offset    订单属性
- volume          数量
- order_id        订单id
- code            品种
- exchange_id     交易所id
- price           价格


## cancel_order

- account_cookie  账户id
- order_id        订单id


## transfer 

- account_cookie    账户id
- capital_password  资金密码
- bankid       银行id
- bankpassword 银行密码
- amount   转账的钱数(>0  转入  <0 转出)


## query_bank

- account_cookie    账户id
- bank_id           银行id
- capital_password  资金密码
- bankpassword      银行密码

## query_settlement

- account_cookie   账户id
- day              日期 yyyymmdd 格式

## change_password

- account_cookie   账户id
- newPass          新密码
- password         旧密码
