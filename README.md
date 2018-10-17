# Remote-operation-of-static-resources
这个主要实现java远程访问服务器的读写文件操作，自动登录读写文件，以上代码整理来自互联网，然后自己将很多琐碎的东西整理在了一起

pom.xml要配置
   <!-- https://mvnrepository.com/artifact/ch.ethz.ganymed/ganymed-ssh2 -->
        <dependency>
            <groupId>ch.ethz.ganymed</groupId>
            <artifactId>ganymed-ssh2</artifactId>
            <version>build210</version>
        </dependency>
        <!-- https://mvnrepository.com/artifact/com.jcraft/jsch -->
        <dependency>
            <groupId>com.jcraft</groupId>
            <artifactId>jsch</artifactId>
            <version>0.1.54</version>
        </dependency>
        
       文件loginServer主要类中有个getProperties这个方法是配置服务器的地址信息的，需要先配置地址信息然后调用login去做登录的操作
       LoginServer.login(LoginServer.getProperties(Config.Alertkey1 + ".json"), false);
       
       如果这个单独的看不懂你可以看看我在项目中是怎么使用的项目中的服务器是内网服务器需要配置成你自己的服务器
       
       
