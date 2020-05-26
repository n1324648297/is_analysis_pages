<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setOneStudentResults  [返回](../README.md)
用例： [评定单个实验成绩](../用例/评定单个实验成绩.md)

- 功能：
    设置一个学生的单个实验成绩和评语。
    
    输入参数total不为空，自动设置update_date为当前日期，表示同时设置批改日期。
    
    输入参数total为空，自动设置update_date为空，表示未批改。
    
- 权限：
    老师：可以修改所有学生的成绩。
    
- API请求地址： 
    接口基本地址/v1/api/etOneStudentResults

- 请求方式 ：
    POST
 
- 请求实例：  

        { 
            "student_id": "201710414131", 
            "test_id":1011,
            "data": {
                "document":18
                "design":20
                "ui":19
                "integrityi":17
                "uniformity": 18
                "total": 92, 
                "memo":"还有待改进",
                }
        }
                



- 请求参数说明:       
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |student_id|学号|
  |data|实验每一项得分点的分数和评语|
  |test_id|实验编号|
  |total|该实验总成绩，之前5个得分项之和|
  |memo|本实验老师的评价，可以为空|   
 
- 返回实例：

        {         
            "status": true,
            "info": 评阅成功!
        }

- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|


