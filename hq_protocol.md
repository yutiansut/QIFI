## QIFI 行情协议


QIFI 使用Rabbitmq来推送行情, 行情推送模式分为两种


1. 直接订阅fanout行情
2. 订阅direct行情, 可以多订阅

直接订阅fanout行情一般是python的QARC_系列

订阅direct行情的是 rust的qamarket-rs 系列

