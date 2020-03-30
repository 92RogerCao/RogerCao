# RogerCao

## 整体说明
Git中展示的是本人在唯都工作时期做过的部分项目代码，其中已经删除敏感信息，同时也与简历中项目经验一栏对应。

代码根据对应项目不同，使用SQL或Python完成。其中前者在SQLserver环境中取数完成。后者主要使用数据分析与建模的模块，如numpy, pandas, scipy, sklearn等。

数据分析项目与报表自动化项目代码的产出结果为各类报告，下文会说明。数据建模项目的结果直接回传到数据库。

## 对代码的简要说明
使用Python的代码均已将功能模块封装在自建包中并引用，为方便查看将所有代码整理到一起。SQL代码则根据分析思路整理。其中：
+ 数据分析类项目：数据均存放于数据库中，所有取数与分析均在SQLserver环境中进行，并将结论以Excel或PPT形式展示
+ 报表自动化类项目：从Excel或数据库中拉取数据数据并根据报表逻辑处理数据后将结果刷入Excel或PPT中展示。
+ 数据建模类项目：训练的模型通过sklearn固化保存。项目上线后，客户将数据以数据流形式传入，通过设置定时任务自动从调用Python拉取数据并进行处理，最后回传数据库。另外代码中没有建模调参的过程，但提供了用于查看调参结果的函数。

## 对项目报告的简要说明
Git中代码对应的数据建模与自动化报告代码，前者没有对应报告，后者是现有报告逻辑的自动化，展示的是代码能力并不体现分析思路，故均不展示报告。

文件名带有"数据分析"的两个项目，这些项目都是通过sql拉取数据，随后根据需求与自己的分析思路形成的报告。另外报告中删除真实数据，大部分以"XXX"表示，有其中有数字的部分也是后期更改以确保保密性。

### 报告业务简要说明
这两个项目对应的业务均是某美妆品牌，而唯都是该品牌CRM部门服务商。该公司每年都会举办不间断的小样申领活动，如A小样的申领期为1.1-2.1，B小样的申领期为2.2-3.1，如此不间断举行。

报告中涉及到的业务字段说明：
+ 申领&核销：用户线上线下等多个渠道均能进行小样申领，但申领后核销渠道**只能是线下门店**。唯都数据库中有所有活动的申领和核销数据明细。
+ 已购买：数据库中没有用户购买明细，而仅有其他服务商推送的用户属性标签用以判断。已购买人数为Active，lapse，history User三类标签数总和，其中Active又可分进一步为HV/MV/LV三类。


### 客户价值盘点报告


#### 客户需求&报告展示内容说明



关于微信公众号与会员数的总体数据查看

这张PPT用于区分用户价值，且已经按照分析结果，将用户按不同指标进行拆解。

其中将客户分别按照申领次数与是否购买分别切分，随后按照已购买客户与潜客的各自行为或标签进行进一步拆解以形成体系，如下图：
| 按是否购买划分 | 按申领次数划分 |
|----|----|
| 已购买 | 按照标签进一步拆解 |
| 未购买 | 按照行为进一步拆解 |

该PPT是上图中关于小样申领次数的进一步分析，查看用户交叉申领的指标情况。

同样是图二的细分，查看每个活动的转化漏斗。



#### 报告分页展示

PPT1
![](https://github.com/92RogerCao/RogerCao/blob/master/photofile/ppt1.png)
PPT2
![](https://github.com/92RogerCao/RogerCao/blob/master/photofile/PPT2.png)
PPT3
![](https://github.com/92RogerCao/RogerCao/blob/master/photofile/PPT3.png)
PPT4
![](https://github.com/92RogerCao/RogerCao/blob/master/photofile/PPT4.png)



### 延迟推送效果报告





