<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getOneTestResults  [返回](../README.md)
用例： [评定单个实验成绩](../用例/评定单个实验成绩.md),[评定总成绩](../用例/评定总成绩.md)

- 功能：
    查看一个学生的单个实验成绩和评语。  
    
- 权限：
    老师/学生：老师可以查看所有学生的成绩，学生只能查看自己的成绩
    
- API请求地址： 
    接口基本地址/v1/api/etOneStudentResults

- 请求方式 ：
    GET
 
- 返回实例：  

        { 
            "status": true,
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
        

- 返回参数说明:       
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |student_id|学号|
  |data|实验的成绩和评语|
  |test_id|实验编号|
  |total|本实验总成绩，可以为空，为空表示没有批改。|
  |memo|本实验老师的评价，可以为空|   
  |status|bool类型，true表示正确的返回，false表示有错误|
- 返回实例：

        {         
            "status": true,
            "info": null
        }



