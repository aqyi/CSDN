<h1 align="center">VS code+Marp实现Markdown转换成PPT格式</h1>

~哈喽，大家好，我是阿木又~

写在前面：

用惯了Markdown，就会用到导出为Word、Pdf等格式，就想能不能用Markdown转换成PPT格式的文件，网上查找一番后发现Marp、Slidev两个解决方案。由于Slidev生成的类似HTML的演讲，所以本片介绍Marp。如有更好方法请评论区告诉我，先谢为敬！（文章配有gif演示，Marp指令不做特别说明）

可参照[Marp官方文档](https://marpit.marp.app/)



# VSCode下载和安装

1. 下载Microsoft Visual Studio Code

[VSCode官网](https://code.visualstudio.com/)下载

![VSCode官网](https://raw.githubusercontent.com/aqyi/picture-file/main/202302131748150.png)

2. 安装VSCode

   ~安装示意图借用CSDN黄化的多多~

![img](https://img-blog.csdnimg.cn/img_convert/47115f0b141d8ca8e6b8a8e819fd1feb.png#pic_center)

![img](https://img-blog.csdnimg.cn/img_convert/2d4d916c09416b9cdfcf4efb9b244154.png#pic_center)

![img](https://img-blog.csdnimg.cn/img_convert/b96712b38b9981ab1604a6af15158d98.png#pic_center)

![img](https://img-blog.csdnimg.cn/img_convert/6a9477329213c63c4903901a4974085b.png#pic_center)

![img](https://img-blog.csdnimg.cn/img_convert/578bbac7db7ffe617a774c04bd708dcb.png#pic_center)

![img](https://img-blog.csdnimg.cn/img_convert/9c96c7e239b15163188094a0cd7d7ea0.png#pic_center)

# 配置所需插件

1. 安装中文插件

![image-20230213175706500](https://raw.githubusercontent.com/aqyi/picture-file/main/202302131757351.png)

2. 安装Markdown插件

![image-20230213180040654](https://raw.githubusercontent.com/aqyi/picture-file/main/202302131800818.png)

3. 安装Marp插件

![image-20230213180249501](https://raw.githubusercontent.com/aqyi/picture-file/main/202302131802956.png)

# 认识Marp

![Marpit](D:/%E8%87%AA%E5%AA%92%E4%BD%93/11_28%E9%80%89%E5%93%81/%E6%97%A9%E5%AE%89/202302170923926.png)

1. 指令的使用方法

Marp提供两种使用方法：

* HTML comment

这种需要在`theme`等指令前后添加<!-- -->。  `VSCode快捷键Ctrl+/`

```
<!--
theme: default
paginate: true
-->
```

* Front-matter

第二种则是直接在Markdown文档的开头（就是将marp:true写在一起），此时无须再添加<!-- -->

```
---
marp: ture
theme: default
paginate: true
---
```

2. 指令类型

指令类型（Type of directives）可分为全局指令（Global directives）和局部指令。

其中，全局指令是整个幻灯片设定值，例如 theme、headingDivider、style。在全局指令前面添加前缀 $，就可以实现对整个幻灯片的设定。

而局部指令用以设置当前幻灯片页面以及后续页面。例如，我们用<!-- backgroundColor: aqua --> 设置幻灯片的背景颜色。



| Marp官方内置主题 |         指令为          |
| :--------------: | :---------------------: |
| Default（违约）  | <!-- theme: default --> |
|   Gaia（盖亚）   |  <!-- theme: gaia -->   |
|  Uncover（揭）   | <!-- theme: uncover --> |



全局指令（Global directives）

|      Name      |      Description      |
| :------------: | :-------------------: |
|     theme      |   指定幻灯片的主题    |
|     style      | 指定用于调整主题的CSS |
| headingDivider |  指定标题分隔符选项   |

局部指令（Local directives）

|        Name        |              Description              |
| :----------------: | :-----------------------------------: |
|      paginate      |            显示幻灯片页码             |
|       header       |        指定该幻灯片页眉的内容         |
|       footer       |         指定幻灯片页脚的内容          |
|       class        |   指定幻灯片元素的HTML类`<section>`   |
|  backgroundColor   |  设置幻灯片的样式`background-color`   |
|  backgroundImage   |  设置幻灯片的样式`background-image`   |
| backgroundPosition | 设置幻灯片的样式`background-position` |
|  backgroundRepeat  |  设置幻灯片的样式`background-repeat`  |
|   backgroundSize   |   设置幻灯片的样式`background-sixe`   |
|       color        |        设置幻灯片的样式`color`        |

背景大小

| 关键词  | 描述                         | 例                         |
| ------- | ---------------------------- | -------------------------- |
| cover   | 缩放图像以填充幻灯片（默认） | ！[bg cover] (image.jpg)   |
| contain | 缩放图片以适合幻灯片         | ! [bg contain] (image.jpg) |
| fit     | 别名，与套牌集兼容           | ! [bg fit] (image.jpg)     |
| auto    | 不缩放图像，并使用原始大小   | ! [bg auto] (image.jpg)    |
| x%      | 按百分比值指定比例因子       | ! [bg 150%] (image.jpg)    |



# 开始使用

1. 创建文档

![创建文档](https://raw.githubusercontent.com/aqyi/picture-file/main/202302161304698.gif)



2. 演示

2.1 简单分页

![分页](https://raw.githubusercontent.com/aqyi/picture-file/main/202302171702213.gif)

2.2 简单使用

![演示](https://raw.githubusercontent.com/aqyi/picture-file/main/202302172032724.gif)

2.3 保存项目

![保存](https://raw.githubusercontent.com/aqyi/picture-file/main/202302172036018.gif)

2.4 导出pptx

![导出](https://raw.githubusercontent.com/aqyi/picture-file/main/202302172148247.gif)

如果遇到导出失败，请退出以管理员身份运行VSCode。

2.5 成功打开![打开预览](https://raw.githubusercontent.com/aqyi/picture-file/main/202302172152303.gif)
