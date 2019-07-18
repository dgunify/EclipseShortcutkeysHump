# EclipseShortcutkeysHump
Eclipse Shortcutkeys Hump convert ，userId convert user_id and user_id convert userId

				字符骆驼命名转换快捷键,驼峰命名快捷键
一、使用目的
1.为了方便更好的开发，在我们页面或java实体类，一般命名都是userId，而数据库则是user_id。
2.那么在mybatis的sql里写sql时一会儿需要使用user_id,一会儿需要使用userId。例如select user_id as userId from user where user_id = #{userId}。这样写代码会很麻烦，我直接写成一样的，然后使用快捷去转换为对应的。如下案例

3.在页面表单提交数据，有时候也出现很多类似这样需要去转换，使用这样的快捷键很方便。

二、使用方法
	在eclipse中Ctrl+Shift+Y（转换为小写）,ctrl+shift+X（转换为大写）.我在源码处封装了一些代码。也是使用此快捷键，但是需要在转换的字符前面添加@符号。
	例如:@userId  ，然后使用鼠标选择此字符串，按住Ctrl+Shift+Y 就会替换为user_id。@user_id，按住Ctrl+Shift+X 就会替换为userId,@符号我也会替换成空。

三、安装方法
	1.找到eclipse安装目录下的plugins文件夹里。
	2.查找org.eclipse.ui.workbench.texteditor_xxxxx.jar后面是每个版本不一致，找前面就行相同就行。
	3.使用压缩文件打开（不解压，只是打开）。看下图
		

4.替换后重启eclipse你就可以试试了。
5.你可以反编译看看里面的源码。生成class后注释没有了。相信你读代码就可以读懂。

四、文件
在目录下有一个CaseAction.c l ass
  如果有问题email:zhangdegui123@163.com
	         qq:1151688451	


 五、其它说明（正常使用则忽略以下说明）
	如果你复制我的这个class进入还是不能使用或导致eclipse无法使用。那么你就把原有的找回来。然后打开你原有jar里的class反编译CaseAction.c l ass，也把我的反编译，复制我的代码进入你原有的代码里（不是所有代码，是替换时的代码）。
原因是每个eclipse版本不一样，类引入的包不一样或是有其它改动，就导致类里面引入的包找不到等等其它错误。
