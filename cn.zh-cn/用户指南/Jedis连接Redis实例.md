# Jedis连接Redis实例<a name="ZH-CN_TOPIC_0126076982"></a>

介绍使用同一VPC内弹性云服务器ECS上的Jedis连接Redis实例的方法。更多的客户端的使用方法，请参考https://redis.io/clients。

## 前提条件<a name="section1502270695932"></a>

-   已成功申请Redis实例，且状态为“运行中”。
-   已创建弹性云服务器，创建弹性云服务器的方法，请参见《弹性云服务器用户指南》。
-   如果弹性云服务器为Linux系统，该弹性云服务器必须已经安装gcc编译环境。

## 操作步骤<a name="section1336235611596"></a>

1.  <a name="li695671074019"></a>查看并获取待连接Redis实例的IP地址/域名和端口。

    具体步骤请参见[查看缓存实例信息](查看缓存实例信息.md)。

2.  登录弹性云服务器。
3.  使用Redis Java \(Jedis\)客户端连接Redis实例。
    1.  获取Redis Java \(Jedis\)客户端源码，具体方法可参考[https://github.com/xetorthio/jedis](https://github.com/xetorthio/jedis)。
    2.  编写如下操作代码。

        Jedis 客户端访问DCS Redis服务，有以下两种方法：

        -   Jedis单连接
        -   Jedis连接池连接

        具体实例如下：

        1.  jedis单连接示例。

            ```
            // 密码模式创建连接
             String host = "192.168.0.150"; 
             int port = 6379; 
             String pwd = "passwd"; 
              
             Jedis client = new Jedis(host, port); 
             client.auth(pwd);
             client.connect(); // 执行set指令
             String result = client.set("key-string", "Hello, Redis!"); 
             System.out.println( String.format("set指令执行结果:%s", result) ); // 执行get指令
             String value = client.get("key-string"); 
             System.out.println( String.format("get指令执行结果:%s", value) );
            
            // 免密模式创建连接
             String host = "192.168.0.150"; 
             int port = 6379; 
              
             Jedis client = new Jedis(host, port); 
             client.connect(); // 执行set指令
             String result = client.set("key-string", "Hello, Redis!"); 
             System.out.println( String.format("set指令执行结果:%s", result) ); // 执行get指令
             String value = client.get("key-string"); 
             System.out.println( String.format("get指令执行结果:%s", value) );
            ```

            其中，**host**为Redis实例的IP地址/域名，**port**为Redis实例的端口。IP地址/域名和端口获取见步骤[1](#li695671074019)，请按实际情况修改后执行。**pwd**为创建Redis实例时自定义的密码，请按实际情况修改后执行。

        2.  jedis连接池示例。

            ```
            // 密码模式生成连接池配置信息
             String ip = "192.168.0.150"; 
             int port = 6379; 
             String pwd = "passwd"; 
             GenericObjectPoolConfig config = new GenericObjectPoolConfig(); 
             config.setTestOnBorrow(false); 
             config.setTestOnReturn(false); 
             config.setMaxTotal(100); 
             config.setMaxIdle(100); 
             config.setMaxWaitMillis(2000); 
             JedisPool pool = new JedisPool(config, ip, port, 100000, pwd);// 在应用初始化的时候生成连接池
             // 在业务操作时，从连接池获取连接
             Jedis client = pool.getResource(); 
             try { 
                 // 执行指令
                 String result = client.set("key-string", "Hello, Redis!"); 
                 System.out.println( String.format("set指令执行结果:%s", result) ); 
                 String value = client.get("key-string"); 
                 System.out.println( String.format("get指令执行结果:%s", value) ); 
             } catch (Exception e) { 
                 // TODO: handle exception
             } finally { 
                 // 业务操作完成，将连接返回给连接池
                 if (null != client) { 
                     pool.returnResource(client); 
                 } 
             } // end of try block
             // 应用关闭时，释放连接池资源
             pool.destroy();
            
            // 免密模式生成连接池配置信息
             String ip = "192.168.0.150"; 
             int port = 6379; 
             GenericObjectPoolConfig config = new GenericObjectPoolConfig(); 
             config.setTestOnBorrow(false); 
             config.setTestOnReturn(false); 
             config.setMaxTotal(100); 
             config.setMaxIdle(100); 
             config.setMaxWaitMillis(2000); 
             JedisPool pool = new JedisPool(config, ip, port, 100000);// 在应用初始化的时候生成连接池
             // 在业务操作时，从连接池获取连接
             Jedis client = pool.getResource(); 
             try { 
                 // 执行指令
                 String result = client.set("key-string", "Hello, Redis!"); 
                 System.out.println( String.format("set指令执行结果:%s", result) ); 
                 String value = client.get("key-string"); 
                 System.out.println( String.format("get指令执行结果:%s", value) ); 
             } catch (Exception e) { 
                 // TODO: handle exception
             } finally { 
                 // 业务操作完成，将连接返回给连接池
                 if (null != client) { 
                     pool.returnResource(client); 
                 } 
             } // end of try block
             // 应用关闭时，释放连接池资源
             pool.destroy();
            ```

            其中，**ip**为Redis实例的IP地址/域名，**port**为Redis实例的端口。IP地址/域名和端口获取见步骤[1](#li695671074019)，请按实际情况修改后执行。**pwd**为创建Redis实例时自定义的密码，请按实际情况修改后执行。


    3.  参考Redis Java \(Jedis\) 客户端源码中的readme文件编译代码并运行Redis Java \(Jedis\) 客户端连接Redis实例。


## 相关产品及文档<a name="section152613113129"></a>

<a name="zh-cn_topic_0046844820_table1073594361220"></a>
<table><thead align="left"><tr id="zh-cn_topic_0046844820_row197372430123"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0046844820_p4737243111216"><a name="zh-cn_topic_0046844820_p4737243111216"></a><a name="zh-cn_topic_0046844820_p4737243111216"></a>相关产品</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0046844820_p18737144301214"><a name="zh-cn_topic_0046844820_p18737144301214"></a><a name="zh-cn_topic_0046844820_p18737144301214"></a>相关文档</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0046844820_row17371443131210"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0046844820_p13372054101419"><a name="zh-cn_topic_0046844820_p13372054101419"></a><a name="zh-cn_topic_0046844820_p13372054101419"></a><a href="https://www.huaweicloud.com/product/dcs.html?infodocbz" target="_blank" rel="noopener noreferrer">分布式缓存 Redis</a></p>
<p id="zh-cn_topic_0046844820_p19548105714519"><a name="zh-cn_topic_0046844820_p19548105714519"></a><a name="zh-cn_topic_0046844820_p19548105714519"></a><a href="https://www.huaweicloud.com/product/dcsmem.html?infodocbz" target="_blank" rel="noopener noreferrer">分布式缓存 Memcached</a></p>
<p id="zh-cn_topic_0046844820_p8862161219564"><a name="zh-cn_topic_0046844820_p8862161219564"></a><a name="zh-cn_topic_0046844820_p8862161219564"></a><a href="https://www.huaweicloud.com/product/ecs.html?infodocbz" target="_blank" rel="noopener noreferrer">弹性云服务器 ECS</a></p>
<p id="zh-cn_topic_0046844820_p841193941416"><a name="zh-cn_topic_0046844820_p841193941416"></a><a name="zh-cn_topic_0046844820_p841193941416"></a><a href="http://www.huaweicloud.com/product/vpc.html?infodocbz" target="_blank" rel="noopener noreferrer">虚拟私有云 VPC</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0046844820_p1381695711471"><a name="zh-cn_topic_0046844820_p1381695711471"></a><a name="zh-cn_topic_0046844820_p1381695711471"></a><a href="https://support.huaweicloud.com/usermanual-dcs/dcs-zh-ug-180315001.html?infodocbz" target="_blank" rel="noopener noreferrer">购买Redis实例</a></p>
<p id="zh-cn_topic_0046844820_p682916370595"><a name="zh-cn_topic_0046844820_p682916370595"></a><a name="zh-cn_topic_0046844820_p682916370595"></a><a href="https://support.huaweicloud.com/usermanual-dcs/zh-cn_topic_0082114847.html?infodocbz" target="_blank" rel="noopener noreferrer">连接Redis实例</a></p>
<p id="zh-cn_topic_0046844820_p16726748155912"><a name="zh-cn_topic_0046844820_p16726748155912"></a><a name="zh-cn_topic_0046844820_p16726748155912"></a><a href="https://support.huaweicloud.com/usermanual-dcs/zh-cn_topic_0061845451.html?infodocbz" target="_blank" rel="noopener noreferrer">缓存实例扩容</a></p>
<p id="zh-cn_topic_0046844820_p12250886517"><a name="zh-cn_topic_0046844820_p12250886517"></a><a name="zh-cn_topic_0046844820_p12250886517"></a><a href="https://support.huaweicloud.com/usermanual-dcs/zh-cn_topic_0079545637.html?infodocbz" target="_blank" rel="noopener noreferrer">缓存实例备份恢复</a></p>
<p id="zh-cn_topic_0046844820_p143616360517"><a name="zh-cn_topic_0046844820_p143616360517"></a><a name="zh-cn_topic_0046844820_p143616360517"></a><a href="https://support.huaweicloud.com/migration-dcs/zh-cn_topic_0078784423.html?infodocbz" target="_blank" rel="noopener noreferrer">缓存实例数据迁移</a></p>
</td>
</tr>
</tbody>
</table>

