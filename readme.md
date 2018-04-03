#   后盾框架学习

* #####    Model         （模型）表示应用程序核心（比如数据库记录列表）。
* #####   View           （视图）显示数据（数据库记录）。
* #####   Controller     （控制器）处理输入（写入数据库记录）。

##      文件目录
####        1、app                业务实现;应用目录，开发者
            ｜—home                      前台文件目录
                ｜—controller            控制器类
                ｜—view                  视图
            
            
            ｜—admin                     后台文件目录     
                ｜—controller            控制器类
                ｜—view                  视图       
            
####       2、frames             框架核心资源文件    
           ｜—core                       核心框架
               ｜—Controller.php         控制器类
               ｜—Boot.php               视图   
           
           ｜—model                      模块  
               ｜—Base.php               控制器类
               ｜—Model.php              视图     
            
           ｜—view                       视图层  
               ｜—Base.php               控制器类
               ｜—View.php               视图     
                          
           
####      3、public             公共支持
          ｜—view                        模板文件目录、静态资源
          
          ｜—index.php                   单一入口文件
              
####      4、system             配置
          ｜—model                       处理业务的各种模型类
                ｜—Stu.php               数据表文件
            
          ｜—config                      配置项文件
                ｜—database.php          数据库连接、初始化数据配置文件  
                ｜—view.php              文件后缀名配置文件
            
          ｜—helper.php                  助手函数文件
————————————————————————————————————————————————————————
————————————————————————————————————————————————————————
单一入口-》框架核心core控制器类-》前台控制器类-》框架核心view视图模板类-》前台视图模板文件
————————————————————————————————————————————————————————
————————————————————————————————————————————————————————
#                                  后台操作流程：

1.          创建班级数据库frame

2.          后台管理员表
create table admin(
a_id    int primary key auto_increment,
a_name   char(16) unique not null default '',
a_psw    varchar(100) not null default''
);
3.          班级表
create table grade(
g_id     int primary key auto_increment,
g_name   char(16) unique not null default ''
);

4.          学生表      
create table student(
s_id     int primary key auto_increment,
s_name   char(16) unique not null default '',
s_sex    enum('男','女') not null default '男',
s_age    tinyint(5) unsigned not null default 0,
g_id    int unsigned not null default 1
);



	//p (md5 ('admin888'));//加密后的密码 7fef6171469e80d32c0559f88b377245
	//p (md5 ('qq123456'));//d0dcbf0d12a6b1e7fbfa2ce5848f3eff


名将共有27位，分为三档：


李元霸、宇文成都、程咬金为第一档;



罗成、单雄信、裴元庆、秦琼、李靖、虬髯客、红拂女、空空儿为第二档;


平阳公主、昆仑奴、柴绍、长孙无忌、魏征、徐茂公、王伯当、樊梨花、玄奘、步飞烟、何仙姑、霍小玉、窦线娘、荆十三娘、聂隐娘、红线为第三档。

        
        