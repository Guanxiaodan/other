# Charles
参考文档： https://www.jianshu.com/p/fb2bdde5b498

   https://www.cnblogs.com/mawenqiangios/p/8270238.html
   
> 是一款代理服务器，主要功能是：

 > ①：截取HTTP和HTTPS网络封包
 
 > ②：可以重发网络请求，方便后端调试
 
 > ③：可以修改网络请求参数
 
 > ④：可以截取网络请求并动态修改
 
 > ⑤：可以模拟慢速网络
 
 ## 一.安装使用
 Charles收费，但是没付费的用户也可使用，只不过就是过半小时需要重新启动一下。使用时需要关闭电脑防火墙。
 ### 1.链接手机和Charles
 ①：手机和安装Charles的电脑需要在同一个局域网中。
 
 ②：到手机端的WiFi设置那里进行代理的相关配置
     a.代理服务器地址写电脑的IP地址
     b.端口写8888（charles的默认端口）
     
 ③：配置完成后，charles会弹出一个允许手机连接的窗口，点击Allow。
 
 ### 2.安装证书来抓取HTTPS请求
 > 上面的步骤，只能抓到HTTP请求，因为HTTPS请求的安全性更高，所以要抓HTTPS的包，需要在电脑上和手机上下载安装证书，否则看到的都是乱码。
 
 ①：安装电脑证书
 ![电脑安装证书](./img/cpdevice.png)
 
 ②：安装手机证书
 在手机打开网址：http://www.charlesproxy.com/getssl 安装证书
 > 注意，同一个手机对应不同电脑上的Charles都要分别下载证书进行认证，因为手机的证书和电脑短的Charles是一一配对的。
 
 ![手机安装证书](./img/phone.png)
 
 ③：选择Proxy>SSL Proxying Steeings,点击add，添加443端口，点击OK。
 
  ### 3.Charles会自动抓取本机上打开的网页的数据
  
  ## 二.过滤请求
  通常，我们只需要向指定服务器发送的请求，这时候，就需要添加一些过滤条件。有下面几种方法：
  
  ### 方法一：
   在Filter中输入过滤关键字，如www.baidu.com
   
   ![filter过滤](./img/filter1.png)
   
  ### 方法二：
   选择 Proxy>Recording Setting>Include>add
   添加一个项目，填入需要监控的协议，主机地址，端口号。
   
  ### 方法三：
   先算了
   
  ## 三. 显示模式
  Charles有两种显示模式：structure和sequence
  
  ### 1.Structure
   优点：可以很清晰的看到请求的数据结构，且是以域名划分请求信息，可以清晰的分析处理数据。
  ### 2.Sequence
   优点： 可以看到全部请求，这里的结果一数据的请求顺序来显示，最新请求的数据显示在最下面
  每个sequence都有size，status等属性可以方便的定位这个请求的价值。
  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
