# spring5

## Spring概念

- #### 基本概述

  1. Spring框架是一个轻量级的开源的JavaEE框架。

  2. Spring可以解决企业应用开发的复杂性。

  3. Sping有两个核心部分：IOC和Aop

     - IOC：控制反转，把创建对象的过程交给Spring进行管理。
     - AOP：面向切面，在不修改源代码的进行功能的增强。

     

  4. Spring特点：

     - 方便解耦，简化开发。
     - Aop编程支持。
     - 方便程序测试。
     - 方便和其他框架进行整合。
     - 方便事务操作。
     - 降低java API开发难度。

- Spring下载地址：https://repo.spring.io/release/org/springframework/spring/


## IOC概念

### IOC容器

1. #### IOC（概念和原理）：

   - 什么是IOC？

     - 控制反转，把对象的创建和对象之间的调用过程，交给Spring进行管理
     - 使用IOC的目的：为了降低耦合度

   - IOC底层原理

     - xml解析、工厂模式、反射

   - IOC（接口）

     - IOC思想基于IOC容器完成，IOC容器底层就是对象工厂

     - Spring提供了IOC容器实现两种方式：（两个接口）

       - BeanFactory:IOC容器基本实现，是Spring内部的使用接口，不提供开发人员进行使用

         ©加载配置文件时候不会创建对象，在获取对象（使用）采取创建对象

       - ApplicationContext: BeanFactory接口的子接口，提供更多强大的功能，一般有开发人员进行使用

         ©加载配置文件的时候就会把在配置文件对象进行创建

     - ApplicationContext接口有实现类：

       ​		*FileSystemXmlApplicaitonContext*

       ​	   *ClassPathXmlApplicationConte*

2. IOC操作Bean管理

   - 什么是Bean管理

     Bean管理指的是两个操作，Spring创建对象，Spring注入属性

   - Bean管理操作有两种方式

     基于XML配置文件方式

     ```
     一、基于XML方式创建对象
     
     <!-- 配置User对象创建 -->
     <bean id="user" class= "com.springtest.spring5.User"></bean>
     
     说明：
     	1、在spring配置文件中，使用bean标签，标签里面添加对应属性，就可以实现对象创建
     	2、在bean标签有很多属性，介绍常用的属性
     		* id 属性：唯一标识
     		* class 属性： 类全路径（包类路径）
     	3、创建对象默认执行无参构造方法完成对象的创建
     
     二、基于XML方式注入属性
     	1、DI：依赖注入，就是注入属性
     		第一种：原始的创建对象之后，调用set属性方法
     		   ... class类头部
     		   
     		   public static Book
     		   {
     		   		// 创建属性
     		   		private String name;
     		   		private String bauther;
     		   		
     		   		// 创建属性对应的set方法
     		   		public void setName(String name)
     		   		{
     		   			this.name = name;
     		   		}
     		   		
     		   		public void setBauther(Strign bauther)
     		   		{
     		   			this.bauther = bauther;
     		   		}
     		   		
     		   		public static void main(String[] args)
     		   		{
     		   			Book book = new Book();
     		   			book.setName("abd");
     		   			book.setBauther("PDD");
     		   		}
     		   
     		   }
     		   
     		   ... class类尾部
     		第二种：在spring配置文件配置对象创建，配置属性注入
     			... xml头
     			
     			<!-- 配置User对象创建 -->
     			<bean id="user" class= "com.springtest.spring5.User">
     				<!-- 
     				使用property 完成属性注入
                     name: 类中属性的名称，
                     value： 需要向属性中注入的值
                     -->
     				<property name="name" value="元始天尊"></property>
     				<property name="bauther" value="鲲鹏"></property>
     			</bean>
     				
     			... xml尾
     		
     		
     ```

     

     基于注解方式实现

     

   - 

   #### 2020-12-08

   ```
   最近父母开始婚了，虽然父母说有他们不用我操心什么（钱），但是我觉得我还没有准备好，我觉的现在的自己太差劲了，我想要把更好的自己给她。虽然说结婚后和现在的生活没有多大的变化，但是我还是希望自己能更加成熟一些，起码在经济上能够支撑起两个家庭。给自己一年时间，在努力拼一把！
   
   
   2020
   	今年由于疫情的缘故，在家足足呆了一个月，已经有好几年没有在家待过这么久了。
   	这一年，读了几本书。♡
   	和女朋友租了更大的房子，虽然还不是很满意。
   	前所未有的想要赚钱，对金钱的渴望达到了前所未有的高度（可能是穷的太久了）。
   	
   最近老有一种感觉，就是突然觉得可以一下子就看到自己5-6年后的样子。挺恐惧的，但是有不甘心，我想要更好的生活。
   
   再给自己一年的时间去成长，努力一年，看看会有什么不一样？
   
   
   焦虑，在自己30岁时，会活出什么样子？期待♞
   
   ```

   #### 

   - xt*的额的得得
     - 1. 

   


## AOP

## JDBC













------------------------------------------------------------------------------------------

2020-12-07     07:20-8:00  40min  spring5-04   

2020-12-07 	21:30-23:00 1.5h 	Spring5-08   坚持学习第三天

2020-12-08	22:00-23:06  1.0h   Spring5-16     主动学习第四天

2020-12-09 	07:10-07:41	30min	Spring6-19    主动学习第五天清晨

