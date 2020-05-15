**概述** 
====
网络投诉预测模型。

**模型使用方法**
----
**输入**  

| 参数 | 描述 | 类型 |
| :-----: | :-----: | :-----: |
| KPI_INFO | 待处理数据文件 | csv文件 | 

待处理数据文件中各列的描述信息如下所示： 

| 列名 | 描述 | 类型 |
| :----- | :----- | :----- |
| kpi_dnsressuccratio | DNS解析成功率 | float | 
| kpi_avgdnsresdelay | DNS解析平均时延 | float |
| kpi_dnsserverfailure | DNS服务器错误次数 | integer |
| kpi_dnsnameerror | DNS域名错误次数 | integer |
| kpi_dnsrefused | DNS服务器拒绝次数 | integer |
| kpi_dnsnotres | DNS无响应次数 | integer |
| kpi_tcpconnsuccratio | TCP建立成功率 | float |
| kpi_avgtcpconndelay | TCP建立平均时延 | float |
| kpi_tcplostratio | TCP掉线率 | float |
| kpi_tcpullostpacketratio | 上行TCP丢包率 | float |
| kpi_tcpdllostpacketratio | 下行TCP丢包率 | float |
| kpi_tcpulrttdelay | 上行RTT总时延 | float |
| kpi_tcpdlrttdelay | 下行RTT总时延 | float |
| kpi_nbrservicepv | 业务访问量 | integer |
| kpi_webresratio | 页面响应成功率 | float |
| kpi_webresdelay | 页面响应总时延 | float |
| kpi_nbrwebopenratio | 页面显示成功率 | float |
| kpi_web_e2e_excellentrate | 端到端业务优秀率 | float |
| kpi_web_over3scnt | 业务响应时延>=3s业务次数 | integer |
| kpi_web_e2e_promptnessrate | 端到端业务建立及时率 | float |
| kpi_initbuffersuccratio | 视频播放成功率 | float |
| kpi_videobufferrate | 视频业务卡顿率 | float |
| kpi_webpostsuccratio | POST响应成功率 | float |
| kpi_avgwebpostdelay | POST响应平均时长 | float |
| user_age | 用户年龄 | integer |
| user_sex | 用户性别 | string |
| user_status | 用户状态 | string |
| user_bill | 用户账单 | float |

**输出** 

| 参数 | 描述 | 类型 |
| :----- | :----- | :----- |
| kpi_dnsressuccratio | DNS解析成功率 | float | 
| kpi_avgdnsresdelay | DNS解析平均时延 | float |
| kpi_dnsserverfailure | DNS服务器错误次数 | integer |
| kpi_dnsnameerror | DNS域名错误次数 | integer |
| kpi_dnsrefused | DNS服务器拒绝次数 | integer |
| kpi_dnsnotres | DNS无响应次数 | integer |
| kpi_tcpconnsuccratio | TCP建立成功率 | float |
| kpi_avgtcpconndelay | TCP建立平均时延 | float |
| kpi_tcplostratio | TCP掉线率 | float |
| kpi_tcpullostpacketratio | 上行TCP丢包率 | float |
| kpi_tcpdllostpacketratio | 下行TCP丢包率 | float |
| kpi_tcpulrttdelay | 上行RTT总时延 | float |
| kpi_tcpdlrttdelay | 下行RTT总时延 | float |
| kpi_nbrservicepv | 业务访问量 | integer |
| kpi_webresratio | 页面响应成功率 | float |
| kpi_webresdelay | 页面响应总时延 | float |
| kpi_nbrwebopenratio | 页面显示成功率 | float |
| kpi_web_e2e_excellentrate | 端到端业务优秀率 | float |
| kpi_web_over3scnt | 业务响应时延>=3s业务次数 | integer |
| kpi_web_e2e_promptnessrate | 端到端业务建立及时率 | float |
| kpi_initbuffersuccratio | 视频播放成功率 | float |
| kpi_videobufferrate | 视频业务卡顿率 | float |
| kpi_webpostsuccratio | POST响应成功率 | float |
| kpi_avgwebpostdelay | POST响应平均时长 | float |
| user_age | 用户年龄 | integer |
| user_sex | 用户性别 | string |
| user_status | 用户状态 | string |
| user_bill | 用户账单 | float |
| label | 预测标签 | bool |

**示例** 
----
**输入示例** 

请参考样例数据，每一行对应一个用户（号码）的数据。 

注意：统计用户过去四天（包括当天）的KPI数据，其中，成功率类数据取四天内最小值，时延类数据取四天内最大值；用户年龄取值区间为10-100，若为空则填0；用户状态取值为“正常/异常/未知”；用户性别取值为“男/女/未知”。

**输出示例** 

| kpi_dnsressuccratio | kpi_avgdnsresdelay | kpi_dnsserverfailure | kpi_dnsnameerror | ...... | label |
| :-------: | :-------: | :-------: | :-------: | :-------: | :-------: |
| 100 | 4.24 | 0 | 0 | ...... | 0 |

