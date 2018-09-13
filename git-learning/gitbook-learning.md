# <center>GitBook制作电子书</center>
## 安装npm
1. 进入[node.js](https://nodejs.org/en/)的官网;
2. 下载最新的安装程序，即可完成Node.js以及npm(Node Package Manager)的安装;
## 通过npm安装GitBook
1. npm install gitbook -g：安装完后花10分钟阅读下Gitbook的帮助文档;
2. 了解Gitbook的基本规则:
> 两个基本文档：README.md 和 SUMMARY.md  
> 其中，README.md 是关于你的书的介绍，而SUMMARY.md 中则包含了书目，即章节结构，大致格式是：  
>  * [第一章]（c1.md）  
>  &emsp;&emsp; * [第一节]（c1s1.md）  
>  &emsp;&emsp; * [第二节]（c1s2.md）  
>  * [第二章]（c1.md）  
>  &emsp;&emsp; * [第一节]（c2s1.md）  
>  &emsp;&emsp; * [第二节]（c2s2.md）

剩下来的东西就很好理解了，只需要编写相应章节即可。在编辑完上面两个文件后，可以运行一下命令：  
<code> gitbook serve -p 8080</code>  
Gitbook 首先根据你的Markdown文件编译为HTML文件，并根据SUMMARY.md生成书的目录。所有生成的文件均保存在当前目录下一个名为_book的子目录中。完成这个工作后，gitbook会作为一个HTTP Server运行，并在8080端口监听HTTP请求。  
运行以上命令后，打开浏览器，在地址栏输入：http://localhost:8080 即可看到你的书页了。 
