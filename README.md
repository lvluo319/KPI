**概述** 
====
KPI异常检测模型。核心网在整个移动运营商网络中占据着举足轻重的地位，一旦故障，会对全网的服务质量造成很大影响，需要及时快速发现核心网的风险，在影响范围扩大之前及时消除故障。关键性能指标（KPI）反应了网络性能和质量，利用核心网KPI进行异常检测，能够及时发现网络质量劣化风险。

**模型使用方法**
----
**输入**  

| 参数 | 描述 | 类型 |
| :-----: | :-----: | :-----: |
| KPI_INFO | 待处理数据文件 | csv文件 | 

待处理数据文件中各列的描述信息如下所示： 

| 列名 | 描述 | 类型 |
| :----- | :----- | :----- |
| 开始时间 | KPI统计开始时间 | date | 
| 结束时间 | KPI统计结束时间 | date |
| 网元位置 | 网元编码 | string |
| VOLTE用户数 | 时间段内VOLTE用户数 | integer |
| 初始注册成功率(%) | 时间段内初始注册成功率 | float |
| 刷新注册成功率(%) | 时间段内刷新注册成功率 | float |
| 注销成功率(%) | 时间段内注销成功率 | float |
| 平均会话建立时长(秒) | 时间段内平均会话建立时长 | float |
| 应答话务量(Erl) | 时间段内应答话务量 | float |
| 其他失败次数 | 时间段内其他失败次数 | integer |
| 终端不可及次数 | 时间段内终端不可及次数 | integer |
| 被叫一号通未应答次数 | 时间段内被叫一号通未应答次数 | integer |
| 呼叫限制次数 | 时间段内呼叫限制次数 | integer |
| 被叫侧平均占用时长(秒) | 时间段内被叫侧平均占用时长 | float |
| 分业务平均响应时长(秒) | 时间段内分业务平均响应时长 | float |
| 多方通话撤消总次数 | 时间段内多方通话撤消总次数 | integer |
| 多方通话登记总次数 | 时间段内多方通话登记总次数 | integer |
| 呼叫保持撤消总次数 | 时间段内呼叫保持撤消总次数 | integer |
| 呼叫保持登记总次数 | 时间段内呼叫保持登记总次数 | integer |
| Rf接口开始计费成功率(%) | 时间段内Rf接口开始计费成功率 | float |
| Rf接口停止计费成功率(%) | 时间段内Rf接口停止计费成功率 | float |
| AS SH通知回应(PNA)失败次数 | 时间段内AS SH通知回应(PNA)失败次数 | integer |
| AS SH订阅回应(SNA)失败次数 | 时间段内AS SH订阅回应(SNA)失败次数 | integer |
| AS SH更新回应(PUA)失败次数 | 时间段内AS SH更新回应(PUA)失败次数 | integer |
| AS SH查询回应(UDA)失败次数 | 时间段内AS SH查询回应(UDA)失败次数 | integer |
| 发送NOTIFY消息成功率(%) | 时间段内发送NOTIFY消息成功率 | float |
| 接收NOTIFY消息成功率(%) | 时间段内接收NOTIFY消息成功率 | float |
| 发送SUBSCRIBE消息成功率(%) | 时间段内发送SUBSCRIBE消息成功率 | float |
| 接收SUBSCRIBE消息成功率(%) | 时间段内接收SUBSCRIBE消息成功率 | float |
| 发送MESSAGE消息成功率(%) | 时间段内发送MESSAGE消息成功率 | float |
| 发送OPTIONS消息成功率(%) | 时间段内发送OPTIONS消息成功率 | float |
| 接收OPTIONS消息成功率(%) | 时间段内接收OPTIONS消息成功率 | float |
| 发送INFO消息成功率(%) | 时间段内发送INFO消息成功率 | float |
| 接收INFO消息成功率(%) | 时间段内接收INFO消息成功率 | float |
| 发送UPDATE消息成功率(%) | 时间段内发送UPDATE消息成功率 | float |
| 发送REFER消息成功率(%) | 时间段内发送REFER消息成功率 | float |
| 接收REFER消息成功率(%) | 时间段内接收REFER消息成功率 | float |
| 主叫接通率(%) | 时间段内主叫接通率 | float |
| 主叫应答率(%) | 时间段内主叫应答率 | float |
| 被叫接通率(%) | 时间段内被叫接通率 | float |
| 被叫应答率(%) | 时间段内被叫应答率 | float |
| eSRVCC切换成功率(%) | 时间段内eSRVCC切换成功率 | float |
| 振铃前呼叫的eSRVCC切换成功率(%) | 时间段内振铃前呼叫的eSRVCC切换成功率 | float |
| 振铃态呼叫的eSRVCC切换成功率(%) | 时间段内振铃态呼叫的eSRVCC切换成功率 | float |
| 稳态呼叫的eSRVCC切换成功率(%) | 时间段内稳态呼叫的eSRVCC切换成功率 | float |
| SH查询成功率(%) | 时间段内SH查询成功率 | float |
| SH更新成功率(%) | 时间段内SH更新成功率 | float |
| SH订阅成功率(%) | 时间段内SH订阅成功率 | float |
| SH通知成功率(%) | 时间段内SH通知成功率 | float |
| 主叫平均响应时长(秒) | 时间段内主叫平均响应时长 | float |
| 数据库空间占用率(%) | 时间段内数据库空间占用率 | float |

**输出** 

| 参数 | 描述 | 类型 |
| :----- | :----- | :----- |
| StartTime | 开始时间 | date | 
| EndTime | 结束时间 | date |
| ElementCode | 网元位置 | string |
| Label | 预测标签 | bool |

**示例** 
----
**输入示例** 

请参考样例数据。 

注意：输入数据必须包含样例数据中4个网元至少一天（当日0点至当日23点）的数据。

**输出示例** 

| StartTime | EndTime | ElementCode | Label |
| :-----: | :---------: | :-----------: | :-------: |
| 2020/3/29 19:00:00 | 2020/3/29 20:00:00 | JS_NJ_VOLTEAS13_ZX_V | 0 |
