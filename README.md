# ActiveMQ-MailSend
基于ActiveMQ的邮件发送demo
这个小demo是使用ActiveMQ生产者消费者模式发送邮件。

使用该demo需要
1、去官网下载Activemq的安装包，解压之后启动bin目录下的win64或win32位下面的activemq.bat（windows）
2、Demo中的activemq-provider代表生产者，用于生产邮件数据，并将想要发送邮件的内容和发送的接受者写好之后，放到ActiveMQ中。
在activemq-provider的TestProducer的mail.setTo("XXX@qq.com");写上你要接受邮箱地址。
3、Demo中的activemq-consumer代表消费者，用户在ActiveMQ中获得数据之后将内容发送给对应的邮箱。在config.properties的mail.username=XXX@163.com
mail.password=XXX（注：密码使用是授权码，并不是邮箱密码）填上正确的信息。(注：发送给邮箱的时候，可能会出现邮箱发送不成功的问题--535 Error: authentication failed，可能是由于没有配置smtp验证用的是授权码，不是密码
具体步骤：设置->POP3/SMTP/IMAP)
