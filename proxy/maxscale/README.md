# windmysql

### 1、说明
<pre><code>
主要存放关于maxscale相关文档
</code></pre> 
### 2、配置过程中出现过的问题
<pre><code>
1、按官方文档配置好，并启动后出现以下的错误
Read-Write Service: login attempt for user 'dbusername'@client:54287, authentication failed.
主要是因为连接maxscale的客户端跟maxscale主机所在的网段不一致引起的
2、如果配置文件中使用加密的密码需要执行以下命令
$maxkeys /pathtomaxscale/
$sudo chown maxscale.maxscal /pathtomaxscale/.secrets
$sudo restorecon -Rv /pathtomaxscale/
$maxpasswd /pathtomaxscale/ your_password
</code></pre>
