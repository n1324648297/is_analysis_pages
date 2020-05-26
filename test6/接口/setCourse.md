<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setCourse  [返回](../README.md)
用例： [选课](../用例/选课.md)

- 功能：
    用户(老师，学生)选课
    
- 权限：
    学生/老师：必须先登录。    
    
- API请求地址： 
    接口基本地址/v1/api/setCourse

- 请求方式 ：
    POST

- 请求实例：

        {
            "user_id":"201710414131",
            "name":"周宏",
            "course_id":"101",  
            "course_name":"系统分析与设计"         
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|用户的ID号。对应表USERS.USER_ID的值|
  |user_name|用户名| 
  |course_id|课程ID号。对应表COURSES.COURSES_ID的值|
  |user_name|用户名| 
  
- 返回实例：

        {         
            "status": true,
            "info": 选课成功
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|


