﻿<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 基于GitHub的实验管理平台的分析与设计

### 成都大学信息科学与工程学院

|学号|班级|姓名|照片|
|:-------:|:-------------: | :----------:|:---:|
|201710414131|软件(本)17-1|周宏|![flow1](../me.jpg)|

## 1. 概述
原:
- 基于GitHub的实验管理平台的作用是在线管理实验成绩的Web应用系统。学生和老师的实验内容均存放在GitHUB
页面上。
- 学生的功能主要有：一是设置自己的GitHub用户名，二是查询自己的实验成绩。学生的GitHub用户名是公开的，但成绩不公开。
- 老师的功能主要有：一是批改每个学生的成绩，二是查看每个学生的成绩。
- 老师和学生都能通过本系统的链接方便地跳转到学生的每个GitHUB实验目录，以便批改实验或者查看实验情况。
- 实验成绩按数字分数计算，每项实验的满分为100分，最低为0分。
- 系统自动计算每个学生的所有实验的平均分。


改进后新增:
- 三单改为三多（多学期，多课程，多评分项）:
一个老师可以上多门课，每个老师只能维护老师自己的课程及成绩。
一个同学可以上多门课，每个同学只能查询同学自己的课程的实验成绩。

- 选课，老师和同学都可以选多门课程
- 原实验为单评分项实验，要求改为多评分项实验，即每个实验的实验成绩细分为多个评分项，每个评分项对应各自的评分标准。 老师在批改实验的时候，对每个评分项进行评分并输入对应的文字评价，系统自动计算出所有评分项的成绩之和为该实验的总成绩。
- 有多个学期，每个学期都有不同的实验。
    
## 2. 系统总体结构
![](系统总体结构.png)

界面设计参见：https://n1324648297.github.io/is_analysis_pages/test6/ui/index.html
    
## 3. 用例图设计 [源码](src/UseCase.puml)
![](UseCase.png)

## 4. 类图设计 [源码](src/class.puml)
![](./class.png)

## 5. 数据库设计
###[参见数据库设计](./数据库设计.md)

## 6. 用例及界面详细设计
### [“学生列表”用例](./用例/学生列表.md),[界面](https://n1324648297.github.io/is_analysis_pages/test6/ui/index.html)
### [“评定总成绩”用例](用例/评定总成绩.md),[界面](https://n1324648297.github.io/is_analysis_pages/test6/ui/评定总成绩.html)
### [“查看成绩”用例](用例/查看总成绩.md),[界面](https://n1324648297.github.io/is_analysis_pages/test6/ui/查看成绩.html)
### [“修改密码”用例](./用例/修改密码.md),[界面](https://n1324648297.github.io/is_analysis_pages/test6/ui/顶部菜单.html)
### [“修改用户信息”用例](./用例/修改用户信息.md),[界面](https://n1324648297.github.io/is_analysis_pages/test6/ui/顶部菜单.html)
### [“查看用户信息”用例](./用例/查看用户信息.md),[界面](https://n1324648297.github.io/is_analysis_pages/test6/ui/顶部菜单.html)
### [“登出”用例](./用例/登出.md),[界面](https://n1324648297.github.io/is_analysis_pages/test6/ui/顶部菜单.html)
### [“登录”用例](./用例/登录.md),[界面](https://n1324648297.github.io/is_analysis_pages/test6/ui/登录.html)
### [“获取指定课程”用例](./用例/登录.md),[界面](https://n1324648297.github.io/is_analysis_pages/test6/ui/顶部菜单.html)
### [“评定单个实验成绩”用例](./用例/登录.md),[界面](https://n1324648297.github.io/is_analysis_pages/test6/ui/评定单个实验成绩.html)
### [“选课”用例](./用例/登录.md),[界面](https://n1324648297.github.io/is_analysis_pages/test6/ui/选课.html)
    