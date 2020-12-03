# IDEA技巧

## Maven配置

1. 在安装Maven之前首先需要安装JDK并配置环境变量。

2. 安装Maven

3. 配置环境变量

   ```
   MAVEN_HOME
   maven的安装路径
   例如：D:\Work\Maven\apache-maven-3.6.2
   ```

   ```
   path
   %MAVEN_HOME%/bin
   ```

   

4. 配置阿里云镜像和本地仓库

   在maven安装目录中的settings.xml文件中修改

   例如：D:WorkMavenapache-maven-3.6.2confserrings.xml

   - 配置阿里云镜像方式：☟

     配置在mirros标签内，可以直接搜索

     ```
     <mirror>
     	<id>nexus-aliyun</id>
      	<mirror0f>central</mirror0f>
     	<name>Nexus aliyun</ name>
     <url>http://maven.aliyun.com/nexus/content/groups/public</url>
     </mirror>
     ```

   -    配置本地仓库方式：☟

     ```
     <localRepository>本地仓库的路径</localRepository>
     
     例如：
     <localRepository> E:\LocalRepository</localRepository>
     ```

     

5. 在IDEA中配置自己的mavne

   IDEA中菜单路径：

   File--->Settings-->Build,Execution,Deployment-->Build Tools --> Maven （也可以直接在Settings中搜索Maven直接到达）中

   修改：

   ```
   Maven home directoty(maven核心路径): 
   ​			例如：D:\Work\Maven\apache-maven-3.6.2
   User settings file(maven的配置文件路径):
   ​			例如：D:\Work\Maven\apache-maven-3.6.2\conf\settings.xml
   Local repository(配置本地maven仓库):
   ​			例如：E:\LocalRepository
   
   备注：
   	1、如果后两项不修改，先勾选Override选项
   	2、修改配置之后记得点击OK生效
   ```

6. 设置maven自动导入

   IDEA中菜单路径：

   File--->Settings-->Build,Execution,Deployment-->Build Tools --> Maven -->Importing中

   修改：

   ```
   只需勾选    Import Maven projects automatically 选项框即可
   
   备注：
   	1、修改配置之后记得点击OK生效
   ```

   ## IDEA中配置GIT