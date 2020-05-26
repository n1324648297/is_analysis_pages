<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getCourese  [返回](../README.md)
用例： [获取指定课程信息](../用例/获取指定课程.md),[选课](../用例/选课.md)

- 功能：
    查看指定学期已选课程。
    
- 权限：
    学生/老师：必须先登录，不能查看其他用户的课程信息。    
    
- API请求地址： 
    接口基本地址/v1/api/getCourse/<course_id>

- 请求方式 ：
    GET
      
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |course_id|课程的ID号。对应表COURSES.COURSE_ID的值|
  
- 返回实例：

学生：

        {         
            "status": true,
            "info": null,
            "term_id":2
            "course_id":"101",
            "course_name":"IS系统分析与设计",    
            "name":"张三",
            "class_dept":"软件工程1班"
            "github_username":"ABCD",
            "type":"学生"            
        }
        
老师:

        {         
            "status": true,
            "info": null,
            "term_id":3
            "course_id":"104",
            "course_name":"Oracle数据库",     
            "name":"赵卫东",
            "github_username":"ZWDgit",
            "type":"老师" 
            "class_dept":{"软件工程1班" ,"软件工程2班" }
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |course_id|课程编号|
  |course_name|课程名|
  |name|用户的真实姓名|  
  |class_dept|班级或者部门名称|
  |github_username|gitHub用户名|
  |type|用户类型：老师或者学生|

