# git自动提交批处理
## 前置
> git可以直接写出命令，以批处理的方式运行。  
> 因此，写如下批处理文件：  
> @echo on  
> @title bat 交互执行批处理文件  
> cd C:\Users\Administrator\Desktop\mygit  
> git add .  
> git commit -m %date:~0,4%年%date:~5,2%月%date:~8,2%日  
> git push origin master
## 自动任务执行
* 在搜索中输入“任务计划程序”  
* 创建基本任务
* 选择触发器
* 选择时间
* 选择启动程序
* 完成