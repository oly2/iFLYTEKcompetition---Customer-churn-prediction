# iFLYTEKcompetition---Customer-churn-prediction
1. 赛题介绍
  随着市场饱和度的上升，电信运营商的竞争也越来越激烈，电信运营商亟待解决减少用户流失，延长用户生命周期的问题。对于客户流失率而言，每增加5%，利润就可能随之降低25%-85%。因此，如何减少电信用户流失的分析与预测至关重要。
  鉴于此，运营商会经常设有客户服务部门，该部门的职能主要是做好客户流失分析，赢回高概率流失的客户，降低客户流失率。某电信机构的客户存在大量流失情况，导致该机构的用户量急速下降。面对如此头疼的问题，该机构将部分客户数据开放，诚邀大家帮助他们建立流失预测模型来预测可能流失的客户。

2. 赛题任务
  给定某电信机构实际业务中的相关客户信息，包含69个与客户相关的字段，其中“是否流失”字段表明客户会否会在观察日期后的两个月内流失。任务目标是通过训练集训练模型，来预测客户是否会流失，以此为依据开展工作，提高用户留存。

3. 赛题数据
  赛题数据由训练集和测试集组成，总数据量超过25w，包含69个特征字段。为了保证比赛的公平性，将会从中抽取15万条作为训练集，3万条作为测试集，同时会对部分字段信息进行脱敏。

4. 特征字段
  客户ID、地理区域、是否双频、是否翻新机、当前手机价格、手机网络功能、婚姻状况、家庭成人人数、信息库匹配、预计收入、信用卡指示器、当前设备使用天数、在职总月数、家庭中唯一订阅者的数量、家庭活跃用户数、… 、过去六个月的平均每月使用分钟数、过去六个月的平均每月通话次数、过去六个月的平均月费用、是否流失

方案特点：
1. 均值、众数填充
2. 5-fold CV
3. Optuna基于贝叶斯调参的XGB模型
4. 最终预测AUC为0.866，排名前13%
