# PublicFiles
Public Project documents

# PublicFiles
本仓库用于存储源代码和各类文档，发布规范参考信息，方便协作。

2021.09.23更新

## 重要事项

### 近期Deadline: 

2020.1.01


### 近期重点任务:

#### 开会流程
1.	回顾报告上周工作
-	确认主持人和秘书, 以及会议时间
-	报告已完成工作
-	待完成issues确认
-	确认未完成工作
2.	本周任务讨论
-	讨论本周待完成任务
-	分配任务和人员
3.	下周事务安排
-	确认主持人和秘书
4.	项目总览
-	Gantt 及 timeline回顾更新
5.	会后事项
-	主持人更新timeline中该周工作, 记录遇到的问题, 总结反思
-	主持人发送该周完成的任务给XXX(图片和文字)
-	秘书更新issues, 分配给相应人员
-	秘书整理好任务在群里也发一份, 名字-任务
-	主持人和秘书根据需求定下周的房间


## 邮箱

方便抄送用:

KEXUAN ZHANG 19103255 KEXUAN.ZHANG.2020@MUMAIL.IE 

HONGZE CHEN 19103191 HONGZE.CHEN.2020@MUMAIL.IE 

YICHEN HU 19105053 YICHEN.HU.2020@MUMAIL.IE 

YIHUI SHI 19103981 YIHUI.SHI.2020@MUMAIL.IE 

ZHENGYANGWANG 19104634 ZHENGYANG.WANG.2020@MUMAIL.IE 

XU ZHANG 19105215 XU.ZHANG.2020@MUMAIL.IE

## Division of labour

- **Team Leader:** Yihui Shi
- **Product Manager:** Zhengyang Wang
- **UI Designer:** Kexuan Zhang, YiChen Hu
- **Software Enginners:** Yihui Shi, YiChen Hu(Front-end); Hongzhe Chen (Back-end)
- **Quality Assurance Leader:** Xu Zhang
- **Report Editor:** Zhengyang Wang, Hongzhe Chen, Yihui Shi
- **Repository Master:** Hongzhe Chen, Yihui Shi
- **Monitor (Tester):** Xu Zhang, Zhengyang Wang

## 语言规范

中文(CN)：规范使用中国大陆官方简体中文

英文(GB)：规范使用英国英文




## Commit 规范

`<type>(<scope>): <subject>`

其中type以及subject为必须要的部分，请注意冒号后的空格，实际使用时不需要"<>", 例如：

`docs(README): fix grammar`

`fix(Main): fix function call`

#### type

用于说明commit的类别，有以下七种

- feat: 新功能，代指feature

- fix: 修补问题bug

- docs: 文档类，如更新readme，模板，会议记录等

- style: 仅改变格式，没有其他影响

- refactor: 重构，不新增，也并非是修改bug

- test: 增加测试

- chore: 构建过程或辅助工具的变动

#### scope（可以省略）

用于说明 commit 影响的范围（暂未清晰）

- 可以是Java 某个类等

#### subject

简单描述具体做了什么

- 动词开头，第一人称单数一般现在时，如add，change

- 首字母小写

- 不加句号

  

## 注释规范

注释规范分为文档注释，测试注释。因为暂未选定语言，因此注释规范暂定



## 代码规范

#### 前端：



#### 后端：
1、MySQL规约：
     1.【强制】在代码中写分页查询逻辑时，若count为0应直接返回，避免执行后面的分页语句。

     2.【推荐】当只要一行数据时请使用 LIMIT 1;

     说明：MySQL数据库引擎会在找到一条数据后停止搜索，而不是继续往后查下一条符合记录的数据。

     3 .【强制】数据订正时，删除和修改记录时，要先select，避免出现误删除，确认无误才能 执行更新语句。

     4. 【推荐】in操作能避免则避免，若实在避免不了，需要仔细评估in后边的集合元素数量，控制在1000个之内。

     5. 【推荐】避免使用or链接条件,建使用union all代替 or,当数据大的时候， union all比 or 性能快上几十倍甚至更高。

     6. 【强制】拆分大的 DELETE 或 INSERT或 UPDATE 语句（小而美），

     说明：这类操作会锁表，要尽量减少锁表时间， 每次操作不宜超过1000条数据。

     7. 【强制】后台分页 count(*) 记录数和 select 数据 的 where 条件必须用同一个;

     说明：经常会发生修改一个忘记了另外一个sql的情况（经常发生）。

     8. 【强制】查询的记录数要控制在可控范围内，不然会处方OOM。

     9. 【推荐】非特殊情况不做for循环调用数据库，批量执行的思想很重要。
2、命名规范
     类名以英文单词取名，使用大驼峰式命名法，首字母大写，多个英文单词以大写字母间隔，尽量避免使用缩写；类名中不允许‘_’、‘-’等特殊符号。

## 服务器相关

#### 后端：
* 服务器项目链接：http://106.14.240.36:8081/SHBM/
* 服务器swagger链接：http://106.14.240.36:8081/SHBM/swagger-ui.html
* 服务器数据库：1、主机：106.14.240.36，2、端口：3306 3、数据库名SecondHandMarket


## Change log规范

change log包括三个部分，对应了commit的内容，在每次新版本发布时需要

- New features
- Bug fixes
- Breaking changes



## [会议记录](/Minutes/)

本文件夹存放会议记录文件，以 .md 文件保存。

Markdown 格式简洁美观，导出 PDF 容易，方便记录。

### 文件名规范

#### 模版 ([Template](/Template/))

模版单独放在Template文件夹中，因为以后可能需要修改。

中文模板：`模板_最后修改人缩写_时间_版本.md`

如：`模板_TYM_1014_v1.md`

英文模板：`Template_name_time_version.md`

如：`Template_TYM_0930_v1.md`

在使用时，取版本号最新的模版。

#### 会议记录

中文： `次数_时间_是否正式_主持人缩写记录人缩写_版本.md`

如：`3_0930_否_CSLHRZ_Final.md`, 

英文： `No._Time_WhetherFormal_names_Version.md`

如： `5_1014_T_TYMJYT_Final.md`

- 是否正式：是否有 Supervisor 参与。是的话填T/是，否的话填F/否。
- 版本：由于会议记录有三个流程（Chairperson 写 Agenda (A)、Sec 写Minutes (M)、Chairperson 写 Comments），请将每个上传到本仓库的会议记录标记版本（A (Agenda)、M (Minutes)、Final），方便之后整理。A和M非必须上传，Final版本必须上传。
- 语言：CN（中文）和GB（英文）。



##  [竞标文件](/Final/)

最终项目文档



## [Documents](/Documents/)

本文件夹存放未分类的实用文件或暂时无法分类的文件。存放的文件请在此处大致表明原用途。





## [Others](/Others/)

本文件夹存放已无用但仍暂时保留的文件。存放的文件请在此处大致表明原用途。

- [Project_16](/Others/Project_16/)：搜索到的以前其他组做过的P16的源代码。



## 项目时间线

No.01_20211003_Syh

了解小组成员，初步分配工作

Team leader : ShiYihui

Product manager:WangZhengyang

UI/UX : ZhangKexuan,HuYichen

Front-end : ShiYihui,HuYichen

Back-end : ChenHongzhe,ShiYihui

Testing : ZhangXu

No.02_20211006_Syh

各自提出项目想法，进行讨论，准备Sprint 1

初步定项“二手书城”，备选项目“图书管理系统”

No.03_20211013_Chz

“二手书城项目”确定，github仓库建立，获取仓库编辑权限

No.04_20211020_Hyc

UI和登录注册功能，设计个人页面，讨论项目的各种功能，编写用户故事

编写用户故事20条

讨论管理员账户和一般用户账户的区分，考虑可能使用不同地址

No.05_20211027_Zkx

注册登录功能初步完成，首页设计完成，设计搜索页

前端与UI讨论，对稿子进行微调

No.06_20211027_Zx

实现搜索功能，设计购物车页面与商品详情

讨论商品详情页的展示内容和功能

No.07_20211103_Wzy

实现购物车页面，个人页面

敲定个人页面展示细节

No.08_20211110_Syh

讨论设计后台管理系统，相应的功能和需要展示的数据。

No.09_20211117_Chz

完成购物车页面，再次讨论商品详情页，讨论测试模块

No.10_20211201_Hyc

完成商品详情页，后台管理系统仍在实现，决定统一登录界面，通过区分用户ID来区别管理员和一般用户

No.11_20211208_Zkx

基本实现后台管理系统，开始测试功能

No.12_20211215_Zx

测试功能，修补一些连接的小问题

No.13_20211222_Wzy

测试功能完成，项目主题完成，进入视频拍摄和文档编辑部分。

