<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>

[2020Typora小白完全使用教程 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/293557841)

[这个更全更好一点](https://blog.csdn.net/qq_41261251/article/details/102817673)

## Markdown语法简介

Markdown是一种轻量级标记语言，排版语法简洁，让人们更多地关注内容本身而非排版。它使用易读易写的纯文本格式编写文档，可与HTML混编，可导出 HTML、PDF 以及本身的 .md 格式的文件。因简洁、高效、易读、易写，Markdown被大量使用，如Github、Wikipedia、简书等。（以上来自官方教程）

[Markdown语法官方教程链接](https://markdown.com.cn/basic-syntax/)

下面介绍使用Typora+PicGo+Github图床让Markdown起飞起来

## Typora安装

Tpypora安装很简单

[安装文件](https://pan.baidu.com/s/1RhFRciPPvignG5MeZ2AVbA)

提取码：weit

![安装文件](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627092426466.png)

安装文件如图，按照使用说明直接安装即可

## PicGo安装

1. 为什么要用PicGO呢（可以不装，装了会更加好用 ）

   Typora的不足：在使用Typora时，对于文档里面的图片，在将文档迁移到其他电脑上面展示时需要将图片一起复制过去带来成本的增加。

   而PicGo是一款图片的上传工具，支持的有微博图床、七牛图床、GitHub图床等等，正好能解决这一问题。其解决问题的大概思路是，将本地的文件或者是剪切板上面的截图发送到图床，然后生成在线图片的链接，这样就可以让Markdown起飞。

2. 下载PicGo

   PicGo下载安装巨简单，直接去GitHub上下载即可，以下放链接，这里下载的2.3.0版本，Window用户直接下载这个即可

   ![下载文件](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627094627875.png)

   [PicGo2.3.0](https://github.com/Molunerfinn/PicGo/releases/t	ag/v2.3.0)

## GitHub图床

> 注：github访问会比较慢，加速的方法有许多，最直接暴力的就是花钱买vpn了，然后还有就是使用更改hosts的方法，在后面会单独介绍一下更改hosts加速github的方法

1. 注册/登录GitHub账号

  ![GitHub注册](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627100634973.png)

  注册很简单，进入github后点击sign up直接按照提示 进行注册即可。

2. 创建Repository

   - 点击New按钮

     ![第一步](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627100949885.png)

   - 出现如下界面，按照1、2、3、4进行即可，1、2中按照自己的想法取名和说明即可，3中为生成README文档，非必选，他这里创建的默认分支名为main(后面进行配置的时候会用到这个名字，因为默认分支名的原因在进行配置时我出现了很多错误)

     ![开始创建库](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627101532047.png)

3. 生成操作repository的一个私人访问token(最为重要的一个步骤)

   - 点击setting

     ![第一步](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627102002701.png)

   - 下拉到Developer settings

     <img src="https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627102144445.png" alt="第二步" style="zoom:80%;" />

   - 点击Personal access tokens按钮并生成新的token

     ![第三步](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627102421764.png)

   - 跳转到这个页面后进行一些token的配置

     Note为对该token的说明

     Expiration为该token的使用期限

     勾选只勾选repo即可

     随后点击generate token

     ![第四步](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627102818888.png)

     > 注：生成的token最好保存一下，生成之后再次查看是看不到的

## PicGo与GitHub图床设置

- PicGO设置

  1. 运行PicGo后点击PicGo设置，下拉到最下面点击选择GitHub图床

     ![PicGo设置](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627103517146.png)

  2. 随后点击到图床设置

     ![图床设置](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627103427526.png)

     > 设定仓库名：格式为github账户名/在创建的Github图床步骤中的仓库名。
     >
     > 设定分支名：这里默认创建的分支名为main，我们应该可以将分支名写为main(若写为master的话会报错上传失败，需要后续在仓库中创建一个master的分支）。
     >
     > 设定token：即为生成保存的token。
     >
     > 指定存储路径，这样写会创建一个img的文件夹，上传的图片都在这个文件夹里面
     >
     > 自定义域名：作用为图片上传成功后，PicGo会将自定义域名+上传的图片名生成的访问链接放在剪切板上，自定义域名可以写为https://cdn.jsdelivr.net/gh/用户名/仓库名

  3. 最后设置一些快捷键让使用更加方便

     ![设置快捷键](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627104524289.png)

- Typora设置

  1. 在文件->偏好设置中进行设置（或者直接ctrl+,打开）

  2. 点击图像，进行如下设置

     ![Typora设置](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627105005302.png)

     > 这里建议是选择PicGo(app)，不要选择命令行，个人觉得更好用
     >
     > 最上面下拉栏的那个选项的意思在当前目录下创建一个文件夹用来存放当前这个文档用到的图片

  3. 设置好后点击验证图片上传选项按钮，上传成功会出现如图

     ![上传成功](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627110216297.png)

  4. 对于上传出现的一些问题，最好的解决方法是查看日志然后找原因

     ![查看日志1](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627110454266.png)

     ![查看日志2](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627110532361.png)

     - 这个问题的解决方法是将github图床设置为默认

       ![遇到的问题1](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627105538096.png)

     - 这个问题的解决方法是github不支持上传同名文件

       ![遇到问题2](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627110854467.png)

## GitHub加速

主要介绍了采用更改hosts的方法来进行加速github访问的方法

1. 打开文件C:\Windows\System32\drivers\etc\hosts(一般选择用记事本打开)

   ![打开文件](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/image-20220627125059174.png)

2. 将一下粘贴在文件末尾（不能用了之后自行去找可用地址）

   ```IP
   140.82.113.3 http://github.com
   140.82.113.3 http://github.global.ssl.fastly.net
   185.199.108.133 raw.githubusercontent.com
   185.199.108.154 pkg-containers.githubusercontent.com
   185.199.108.133 cloud.githubusercontent.com
   185.199.108.133 gist.githubusercontent.com
   185.199.108.133 marketplace-screenshots.githubusercontent.com
   185.199.108.133 repository-images.githubusercontent.com
   185.199.108.133 user-images.githubusercontent.com
   185.199.108.133 desktop.githubusercontent.com
   185.199.108.133 avatars.githubusercontent.com
   185.199.108.133 avatars0.githubusercontent.com
   185.199.108.133 avatars1.githubusercontent.com
   185.199.108.133 avatars2.githubusercontent.com
   185.199.108.133 avatars3.githubusercontent.com
   185.199.108.133 avatars4.githubusercontent.com
   185.199.108.133 avatars5.githubusercontent.com
   185.199.108.133 avatars6.githubusercontent.com
   185.199.108.133 avatars7.githubusercontent.com
   185.199.108.133 avatars8.githubusercontent.com
   ```

3. 保存文件，覆盖掉原来的hosts文件，可能会报错没有权限，去属性里面更改下权限即可

## Typora基本技巧

### 常用快捷键

1. **加粗：ctrl+B**

   **weitermachen**

2. **撤销：ctrl+Z**

3. **字体倾斜：ctrl+I**

   *weitermachen*

4. **下划线：ctrl+u**

   <u>weitermachen</u>

5. **多级标题：ctrl+1~6**

   # weitermachen 

6. **有序列表：ctrl+shift+[**

7. **无序列表：ctrl+shift+]**

8. 增加缩进：tab

9. 减少缩进：shift+tab

10. 插入链接：ctrl+k

    [weitermachen](https://zhuanlan.zhihu.com/p/293557841)

11. **插入公式：ctrl+shift+M**

$$
\lim_{x\to\infty}\exp(-x)=0
$$

12. **行内代码：ctrl+shift+K**
13. **插入图片：ctrl+shift+I**
14. 返回顶部/底部：ctrl+home/end
15. 创建表格：ctrl+T
16. 选中某句话：ctrl+L
17. 选中某个单词：ctrl+d
18. 选中相同格式的文字：ctrl+E
19. 搜索：CTRL+F
20. 搜索并替换：ctrl+h
21. 删除线：alt++shift+5

​		~~weitermachen~~

22. 引用：ctrl+shift+q
23. 生成目录：[toc]+enter

注：一些实体符号需要在实体符号前面加\才能够显示

### 菜单

输入[TOC]即可产生菜单，菜单会自动更新

### 区域元素

YAML FONT Matters

在文章的最上方输入---，按换行键产生，然后在里面输入内容即可

### 段落

按换行键[enter]建立新的一行，按shift+enter可以创建一个比段落间距更小的行间距。可在行尾部插入打断线，禁止向后插入

打断线<br/>后面的内容将会自动换行

### 标题

开头#的个数表示，空格+文字。标题有1~6个级别，#表示开始，换行键结束

#一级标题 快捷键为ctrl+1

##二级标题 快捷键为ctrl+2

......

### 字体

1. 斜体以**或_括住

​	*这是斜体字1* _这是斜体字2_

2. 加粗 以**或__括住

   **这是加粗字1** __这是加粗字2__

3. 删除线 以~~括住

   ~~这是删除线~~

4. 下划线 <u></u>

   <u>这是下划线</u>

   <u>这是下划线</u>

5. 高亮 以==括住（需要在自己的偏好中打开设置）

   ==这是高亮==

### 代码

行内输入代码块快捷键 ：ctrl+shift+K

1. 开头```+语言名字，开启代码块，换行键换行，光标下移键跳出（好像快捷键不太管用）该符号为1左边那个键

   ``` python 
   print('Hello World!')
   ```

   

2. 用两个’在正常段落中表示代码 (好像也不太管用)

   use the `print()` function

### 数字公式

打开Typora选择数字模块

- 点击“段落”->“公式块”

- 快捷键ctrl+shift+m

- “$$”+回车

  以上三种方式都能打开数学公式的编辑栏

1. 下标/上标 下标使用~括住内容公式中用单个_表示，上标使用’^‘括住内容（需要在偏好中打开该功能）

   H~2~O

   y^2^=4

2. $数学公式$表示行内公式（内联公式），即可以将公式插入到一行中，比如 $1+2=3$这样的公式。

   $$数学公式$$表示行间公式（外联公式），即可以将公式插入到行与行之间，单独占据一行或者数行的空间，并且居中放置

3. 根号 我们可以使用\sqrt{}来表示根号，如：

   $\sqrt{2},\sqrt{5}$

   我们也可以使用\sqrt[]{}来表示更具体的根号信息：

   $\sqrt[3]{8}$

4. 下/上划线 我们可以使用\underline{},\overline{}来表示下上划线，如：$下水平线：\underline{a+b}$，$上水平线：\overline{a+b}$

5. 上下水平大括号 我们可以使用\overbrace{}和\underbrace{}来表示上下大括号，如：$上大括号：\overbrace{x_1+x_2+x_3}$，$下大括号：\underbrace{a+b}$

6. 向量符号 我们可以使用\vec{}来表示单个字母向量，其实也可以表示多个字母，但不美观，另两个命令\overrightarrow{}和\overleftarrow{}在定义从A到B的向量时非常有用。如
   $$
   \vec{a}
   \\\vec{AB}
   \\\vec{ABC}
   \\\overrightarrow{AB}
   \\\overleftarrow{AB}
   $$

7. 分数 我们可以使用\frac{}{}来表示分数，如：
   $$
   \frac{1}{2}
   \\\frac{\sqrt[3]{8}}{4}
   $$

8. 积分运算 积分运算符用\int来生成，用\int_{}^{}来表示上下界，如：
   $$
   \int
   \\\int_{1}^{2}
   $$

9. 求和运算符 可以使用\sum来生成，用sum_{}^{}来表示求和上下界，如：
   $$
   \sum
   \\\sum_{i=1}^{10}x_i
   $$
   注意：求和符号的上下标渲染显示在内联和外联公式中不同，以上是外联公式，内联公式为$\sum_{i=1}^{10}x_i$

10. 连乘运算符 用\prod{}表示，上下标用\prod_{}^{}表示，如：
    $$
    \prod
    \\\prod_{i=1}^{10}x_i
    $$

11. 特殊符号
    $$
    \alpha
    \\\beta
    \\\gamma
    \\\rho
    \\\lambda
    \\\mu
    \\\delta
    \\\Delta
    \\\pi
    \\\Omega
    \\\omega
    $$

    > 注：对应的首字符大写为该特殊符号的大写

12. 加减乘除
    $$
    + -
    \\\times
    \\\div
    $$

13. 矩阵表示
    $$
    \left[\begin{matrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    \end{matrix}\right]
    $$

    - `\begin{matrix}`和`\end{matrix}`说明在它们之间的是矩阵

    - `1 & 2 & 3\\`表示第一行的元素，其中用`&`来分割每一个元素，用`\\`来换行

    - \left[ 、\right]表示给矩阵加入括号

    - 另外一种显示矩阵的写法
      $$
      \left|\begin{matrix}
      1 & 2 & 3 \\
      4 & 5 & 6 \\
      \end{matrix}\right|
      $$

14. 方程组
    $$
    \begin{equation}
    \left\{
    			\begin{array}{1l}
    			x=\dfrac{3\pi}{2}(1+2t)\cos{\dfrac{3\pi}{2}(1+2t)}&, 
    			\\
    			\\y=s&,0\leq s\leq L,|t|\leq1.
    			\\
    			\\z=\dfrac{3\pi}{2}(1+2t)\sin(\dfrac{3\pi}{2}(1+2t))&,
    			\end{array}
    \right.
    \end{equation}
    $$
    现在我们一一来解释：

    - begin{equation}与\end{euqation}表示它们之间的为方程组。
    - \left\{和\right.表示在方程组的左边加上{，在右边加上.，因为{在外联公式中有特殊的意义，因此需要在其前面加上转义字符\。
    - \begin{array}和\end{array}表示它们之间的是数组，其实这也可以用来表示矩阵。
    - {lr}表示有两列，第一列的值靠左排列，用l表示，第二列的值靠右排列，用r表示，如果是中间对齐则为c。
    - 然后下面三行是方程式，用&分割，用\\换行。

15. 分段函数
    $$
    y=
    \begin{equation}
    	\left\{
    		\begin{array}{1r}
    		x-1 &, x\leq0
    		\\x+1 &, x>0
    		\end{array}
    	\right.
    \end{equation}
    $$

### 表情

typora语法支持添加emoji表情，输入不同的符号码（两个冒号包围的字符）可以显示出不同的表情

以：开始，然后输入表情的英文单词，以：结尾，直接输入该表情

:smile:

### 表格

开头|+列名+|+列名+|+换行键，创建一个2*2表格，ctrl+enter可建立新行

| 第一列 | 第二列 |
| ------ | ------ |
|        |        |
|        |        |

### 分割线

输入 *** 或者---，按换行键换行，即可绘制一条水平线

***

---

### 引用

开头>表示，空格+文字，按换行键换行，双按换行键跳出

> 引注1
>
> ...
>
> 引注n
>
> 还有一行，双按换行键跳出

1. 普通引用

   空格+引用文字：在引用的文字前加>+空格即可，引用可以嵌套

   > 引用文本前使用[大于号+空格]
   >
   > 这行可以不加，新起一行都要加上
   >
   > 这是引用的内容
   >
   > > 这是引用的内容

2. 列表中使用

- 第一项

  > 引用1

- 第二项

  > 引用2

  3. 引用嵌套列表

    > - 这是引用里嵌套的一个列表
    > - 还可以有子列表
    >   - 子列表需要从-之后延四个空格开始

  4. 引用里嵌套代码块

    > ​	同样的，在前面加四个空格形成代码块
    >
    > ”‘	

### 脚注

在需要添加脚注的文字后面+[+^+序列+]，注释的产生可以鼠标放置其上单击自动生成，添加信息 或人工添加+[+^+序列+]+：

脚注的产生方法[^footnote]

### 链接

1. 链接 输入网址，单击链接，展开后可编辑 快捷键：CTRL+K

- 打开网页链接

​	[Typora教程](https://zhuanlan.zhihu.com/p/293557841)

- 打开本地文件

  [pdf](E:\3D_reconstruction.pdf)

2. 高级链接技巧

   使用[+超链接文字+]+[+标签+]，创建可定义链接

   这是[百度][id][id][id]:https://www.baidu.com

### 图片

> Typora文本文档中有使用图片内容，如果需要发布在各个兼容的Markdown的软件平台，需要预先上传文档中的图片至图床，再通过对图床的图片的链接调用，才能正常显示，否则各个平台将无法看到该文档图片。

1. 方法一，手动添加：跟链接的方法区别在于前面加了一个感叹号！

![checkerboard](https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/checkerboard.jpg)

2. 方法二：通过标签`<img src=url/>`来插入图片，如

   > 采用src方法使用的是本地图片，暂时不知道如何使用图床上的图片，使用该方法的主要好处是可以自定义图片的一些属性，以下图片使用的全是checkboard这个图片

   <img src='https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/checkerboard-16563101430451.jpg'/>

   - 我们可以改变<img>标签的属性，来改变图片的大小,以下为将长宽均设置为100

   <img src='https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/checkerboard-16563101743672.jpg' width=100 height=100/>

   - 也可以改变图片的位置，如：

     图片在左边:

     <img src='https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/checkerboard-16563101889193.jpg' width=100 height=100 style='float:left'>				





​			   图片在右边：

​				<img src='https://cdn.jsdelivr.net/gh/weitermachen/Figurebed/img/checkerboard-16563101962904.jpg' width=100 heigth=100 style='float:right'>

​				



### 改变字体颜色及大小

我们可以使用<font></font>标签来改变字体颜色和大小，如：

<font size=3 color='red'>字体颜色为红色，大小为3</font>

<font size=4 color='blue'>字体颜色为蓝色，大小为4</font>

<font size=6 color='violet'>字体颜色为紫罗兰，大小为6</font>

### 改变字体的对齐方式

我们可以使用标签<p></p>加上属性align，如：

<p align='left'>左对齐</p>

<p align='center'>中间对齐</p>

<p align='right'>右边对齐</p>
