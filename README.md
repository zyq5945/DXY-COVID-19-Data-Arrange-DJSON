
## 1.介绍说明

本项目是使用[diseasedataarrange](https://github.com/zyq5945/diseasedataarrange)程序，针对BlankerL发布的[DXY-COVID-19-Data](https://github.com/BlankerL/DXY-COVID-19-Data)的最新DXYArea.csv文件，自动生成整理后的字典JSON格式文件数据。

若你对生成的数据有疑问，或者认为汇总的数据有误，请向[BlankerL反馈异常数据](https://github.com/BlankerL/DXY-COVID-19-Crawler/issues/34)

## 2.不同平台访问地址

针对可能对不同网站访问速度有快慢问题，酌情可以考虑以下最快的访问地址：

#### [github.com 仓库地址](https://github.com/zyq5945/DXY-COVID-19-Data-Arrange-DJSON)

#### [gitee.com  仓库地址](https://gitee.com/zyq5945/DXY-COVID-19-Data-Arrange-DJSON)

#### [github.io 网站地址](https://zyq5945.github.io/DXY-COVID-19-Data-Arrange-DJSON)

#### [gitee.io  网站地址](https://zyq5945.gitee.io/dxy-covid-19-data-arrange-djson/)

注: gitee.io的子文件地址和github.io的寻址方式不一样，请自行在浏览器中测试调整

注：gitee.io不是动态更新的，需要使用gitee.io最新数据请自行克隆仓库后再手动发布


## 3.查看生成的文件

### [查看地址](FILELINK.md)


## 4.生成文件的说明

### 4.1 文件目录说明

| 目录名 |  说明 |
|---|---|
|  ChildDetail | 各个子按日期升序排序的详细情况目录，其下是各父名称目录，父目录下才是子文件 |
|  ParentDetail | 各个父按日期升序排序的详细情况目录 |
|  ParentLastChildren | 各个子按日期降序排序的最后更新情况目录，其下是各父名称目录，父目录下才是子文件 |


### 4.2 固定文件名称说明

| 文件名 |  说明 |
|---|---|
|  Total | 最后更新汇总的情况 |
|  LastParents | 最后更新的所有父情况 |
|  LastChildren | 最后更新的所有子情况 |


### 4.3 文件的各字段说明

注：标准化是指将值缩放到浮点数是0-1之间的值

| 字段 |  说明 |
|---|---|
|  TimeOffset | 浮点型的天数时间偏移 |
|  UpdateTime | 更新时间 |
|  ParentName | 父名称 |
|  ParentConfirmedCount | 父确诊数 |
|  ParentSuspectedCount | 父疑似数 |
|  ParentCuredCount | 父康复数 |
|  ParentDeadCount | 父死亡数 |
|  ParentTreatingCount | 父正在治疗数 |
|  ParentCuredRate | 父康复率 |
|  ParentDeadRate | 父死亡率 |
|  ParentTreatingRate | 父正在治疗率 |
|  ParentDeadDivideCured | 父死亡除以康复数 |
|  ParentCuredDivideDead | 父康复除以死亡数 |
|  ParentConfirmedNorm | 父确诊数标准化 |
|  ParentSuspectedNorm | 父疑似数标准化 |
|  ParentCuredNorm | 父康复数标准化 |
|  ParentDeadNorm | 父死亡数标准化 |
|  ParentTreatingNorm | 父正在治疗数标准化 |
|  ParentDeadRateEx | 父康复数与父死亡数推算出的死亡率 |
|  ParentCuredRateEx | 父康复数与父死亡数推算出的康复率 |
|  ParentTatalConfirmedNorm | 总计的父确诊数标准化 |
|  ParentTatalSuspectedNorm | 总计的父疑似数标准化 |
|  ParentTatalCuredNorm | 总计的父康复数标准化 |
|  ParentTatalDeadNorm | 总计的父死亡数标准化 |
|  ParentTatalTreatingNorm | 总计的父正在治疗数标准化 |
|  ChildName | 子名称 |
|  ChildConfirmedCount | 子确诊数 |
|  ChildSuspectedCount | 子疑似数 |
|  ChildCuredCount | 子康复数 |
|  ChildDeadCount | 子死亡数 |
|  ChildTreatingCount | 子正在治疗数 |
|  ChildCuredRate | 子康复率 |
|  ChildDeadRate | 子死亡率 |
|  ChildTreatingRate | 子正在治疗率 |
|  ChildDeadDivideCured | 子死亡除以康复数 |
|  ChildCuredDivideDead | 子康复除以死亡数 |
|  ChildConfirmedCountRate | 子确诊数相对父占比率 |
|  ChildSuspectedCountRate | 子疑似数相对父占比率 |
|  ChildCuredCountRate | 子确康复数相对父占比率 |
|  ChildDeadCountRate | 子确死亡数相对父占比率 |
|  ChildTreatingCountRate | 子正在治疗数相对父占比率 |
|  ChildConfirmedNorm | 子确诊数标准化 |
|  ChildSuspectedNorm | 子疑似数标准化 |
|  ChildCuredNorm | 子康复数标准化 |
|  ChildDeadNorm | 子死亡数标准化 |
|  ChildTreatingNorm | 子正在治疗数标准化 |
|  ChildDeadRateEx | 子康复数与子死亡数推算出的死亡率 |
|  ChildCuredRateEx | 子康复数与子死亡数推算出的康复率 |
|  ChildTatalConfirmedNorm | 总计的子确诊数标准化 |
|  ChildTatalSuspectedNorm | 总计的子疑似数标准化 |
|  ChildTatalCuredNorm | 总计的子康复数标准化 |
|  ChildTatalDeadNorm | 总计的子死亡数标准化 |
|  ChildTatalTreatingNorm | 总计的子正在治疗数标准化 |


## 5.数据排序问题

中文有多音字的情况，比如重庆的“重”可能会按读音zhòng来进行排序，所以排序会有些问题。

## 6.一些个人的DXY-COVID-19数据分析心得


[《使用OriginLab的Boltzmann模型拟合仿真预测中国COVID-19(2019-nCov)疫情康复情况》](https://zyq5945.github.io/zyq5945/blog_13.html)
