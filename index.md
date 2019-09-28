## Simple Minecraft Launcher

<em>
  欢迎使用SML 1.6.5 启动器!
  
  这是个简洁的启动器，使用了易语言和Jmccc编写。
</em>
<script>
  function Download() {
  window.open("https://github.com/leadsoft-ware/SMLRelease/releases/download/InsiderPreview/Insider_Preview_beta1.exe","","")
  
}
</script>


<a href="javascript:Download()">前往下载</a>

源码
```
.版本 2

.程序集 窗口程序集_启动窗口
.程序集变量 Jmccc, Jmccc

.子程序 __启动窗口_创建完毕

子程序_查找所有文件 (取运行目录 () ＋ “\.minecraft\versions\”)
组合框1.现行选中项 ＝ 0
编辑框1.内容 ＝ 读配置项 (取运行目录 () ＋ “\smlconfig.ini”, “Game”, “Player”, )

.子程序 子程序_查找所有文件
.参数 文件目录, 文本型
.局部变量 文件名, 文本型

.如果真 (取文本右边 (文件目录, 1) ≠ “\”)
    文件目录 ＝ 文件目录 ＋ “\”
.如果真结束
文件名 ＝ 寻找文件 (文件目录 ＋ “*.*”, 1 ＋ 2 ＋ 4 ＋ 16 ＋ 32)
.判断循环首 (文件名 ≠ “”)
    .如果真 (文件名 ＝ “.” 或 文件名 ＝ “..”)
        文件名 ＝ 寻找文件 (, 1 ＋ 2 ＋ 4 ＋ 16 ＋ 32)
        到循环尾 ()
    .如果真结束
    组合框1.加入项目 (文件名, )
    文件名 ＝ 寻找文件 (, 1 ＋ 2 ＋ 4 ＋ 16 ＋ 32)
.判断循环尾 ()

.子程序 _编辑框1_内容被改变

写配置项 (取运行目录 () ＋ “\smlconfig.ini”, “Game”, “Player”, 编辑框1.内容)

.子程序 _按钮1_被单击
.局部变量 text, 子程序指针
```
