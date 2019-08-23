# MailBox
邮件发送平台系统

#工程竣工总结
<br>
工程名：邮件发送系统(基于Maven+Servlet+Java Bean)，目前支持QQ/21cn/163/阿里云/新浪五种邮箱发送邮件．<br>

0.开发环境：Ubuntu
1.开发工具：Eclipse+Sublime Text+VS Code
2.管理工具:Maven
3.数据库:Sqlite v3.0
4.服务端服务器 Tomcat v9.0
5.客户端:Google Chrome/Firefox
6.邮件发送协议：SMTP

项目框架:无<br>

涉及的设计模式：单例模式<br>

所用语言
- 后端:Sqlite+java<br>
- 前端:HTML+CSS,JavaScript+JQuery,JSTL+JSP EL<br>

模块及其可用功能：<br>
+ 账户模块：<br>
<ol>
	<li>注册：注册资料包括用户名(无法重复)，第二邮箱，密码(MD5盐值加密)，性别，出生日期。<br>
	其中用户名必须按正式邮箱域名(username@domain.com)来注册，否则报错.<br>
	注：若想向外发送邮件成功，必须用已存在的真实邮箱账号．<br>
	<li>登录：用户名或密码有误会在当前页面提示；登录前须输入视图上正确的随机验证码，否则提醒报错。<br>
	登陆成功后，进入面板主页.
	<li>修改密码（新旧密码不可重复一致，否则提示用户操作失误）.
</ol>

* 邮件发送模块
<ol>
<li>编写一封新的信件，收件人、主题、内容必填，可上传附件发送，新邮件发送成功后，会自动移入发件箱．<br>
注：收件方最好应开通SMTP服务协议，如此方可收取邮件.<br>
</ol>

+ 发件箱
<ol>
<li>查看箱内全部已发送邮件的预览信息(收信者/标题/附件名/发信时间)<br>
<li>查看一封邮件的详情内容，并编辑此封邮件，可将编辑好的信件再次重新发送；或移至回收站；或将一封邮件存至草稿箱<br>
<li>可多选将多份信件移至回收站<br>
<li>可多选彻底删除多份邮件<br>
</ol>

+ 草稿箱
<ol>
<li>查看箱内全部草稿信件的预览信息(收信者/标题/附件名/信件创建时间/上次改动时间)<br>
<li>查看一封草稿邮件的详情，并可将该封信件再次重新发送，或者编辑这封草稿(编辑好之后，可再次重新发送，或移至回收站)。<br>
<li>可多选将多份信件移至回收站<br>
<li>可多选彻底删除多份草稿信件<br>
</ol>

+ 垃圾箱
<ol>
<li>查看箱内全部信件的预览信息(发件者/收信者/标题/附件名/移至垃圾箱时间)<br>
<li>查看一封垃圾邮件的详情，并可将该封信件再次重新发送，或者编辑这封草稿(编辑好之后，可再次重新发送，或移至回收站)。<br>
<li>可多选彻底删除多份垃圾邮件<br>
<li>可多选将多份垃圾邮件恢复至收件箱/发件箱/草稿箱<br>
</ol>
__________________________________________________________
