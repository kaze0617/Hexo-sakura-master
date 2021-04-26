---
title: Java命名规范
author: KAZE
avatar: 'https://cdn.jsdelivr.net/gh/kaze0617/cdn@2.3/images/custom/avatar.jpg'
authorLink: /about/
authorAbout: No game no life!
authorDesc: 爱折腾，热爱ACG。
comments: true
date: 2021-03-23 22:46:13
categories: Java
tags:
keywords: Java命名规范
description: 好的命名能体现出代码的特征，含义或者是用途，让阅读者可以根据名称的含义快速厘清程序的脉络。
photos: https://cdn.jsdelivr.net/gh/kaze0617/image-hosting@master/20210425/java.jpg
---
每个公司都有不同的标准，目的是为了保持统一，减少沟通成本，提升团队研发效能。所以本文中是笔者结合阿里巴巴开发规范，以及工作中的见闻针对Java领域相关命名进行整理和总结，仅供参考。
## 一、Java中的命名规范
好的命名能体现出代码的特征，含义或者是用途，让阅读者可以根据名称的含义快速厘清程序的脉络。不同语言中采用的命名形式大相径庭，Java 中常用到的命名形式共有三种，既首字母大写的 UpperCamelCase ，首字母小写的
lowerCamelCase 以及全部大写的并用下划线分割单词的UPPER_CAMEL_UNSER_SCORE。

**通常约定，类一般采用大驼峰命名，方法和局部变量使用小驼峰命名，而大写下划线命名通常是常量和枚举中使用。**

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>类型</p></div></th><th style="text-align:left"><div class="table-header"><p>约束</p></div></th><th style="text-align:left"><div class="table-header"><p>例</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>项目名</p></div></td><td style="text-align:left"><div class="table-cell"><p>全部小写，多个单词用中划线分隔‘-’</p></div></td><td style="text-align:left"><div class="table-cell"><p>spring-cloud</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>包名</p></div></td><td style="text-align:left"><div class="table-cell"><p>全部小写</p></div></td><td style="text-align:left"><div class="table-cell"><p>com.alibaba.fastjson</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>类名</p></div></td><td style="text-align:left"><div class="table-cell"><p>单词首字母大写</p></div></td><td style="text-align:left"><div class="table-cell"><p>Feature, ParserConfig,DefaultFieldDeserializer</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>变量名</p></div></td><td style="text-align:left"><div class="table-cell"><p>首字母小写，多个单词组成时，除首个单词，其他单词首字母都要大写</p></div></td><td style="text-align:left"><div class="table-cell"><p>password, userName</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>常量名</p></div></td><td style="text-align:left"><div class="table-cell"><p>全部大写，多个单词，用'_'分隔</p></div></td><td style="text-align:left"><div class="table-cell"><p>CACHE_EXPIRED_TIME</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>方法</p></div></td><td style="text-align:left"><div class="table-cell"><p>同变量</p></div></td><td style="text-align:left"><div class="table-cell"><p>read(), readObject(), getById()</p></div></td></tr></tbody></table></div>

## 二、包命名
**包名**统一使用**小写**，**点分隔符**之间有且仅有一个自然语义的英文单词或者多个单词自然连接到一块（如 springframework，deepspace
不需要使用任何分割）。包名统一使用单数形式，如果类命有复数含义，则可以使用复数形式。

包名的构成可以分为以下几四部分【前缀】 【发起者名】【项目名】【模块名】。常见的前缀可以分为以下几种：

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>前缀名</p></div></th><th style="text-align:left"><div class="table-header"><p>例</p></div></th><th style="text-align:left"><div class="table-header"><p>含义</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>indi（或onem ）</p></div></td><td style="text-align:left"><div class="table-cell"><p>indi.发起者名.项目名.模块名.……</p></div></td><td style="text-align:left"><div class="table-cell"><p>个体项目，指个人发起，但非自己独自完成的项目，可公开或私有项目，copyright主要属于发起者。</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>pers</p></div></td><td style="text-align:left"><div class="table-cell"><p>pers.个人名.项目名.模块名.……</p></div></td><td style="text-align:left"><div class="table-cell"><p>个人项目，指个人发起，独自完成，可分享的项目，copyright主要属于个人</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>priv</p></div></td><td style="text-align:left"><div class="table-cell"><p>priv.个人名.项目名.模块名.……</p></div></td><td style="text-align:left"><div class="table-cell"><p>私有项目，指个人发起，独自完成，非公开的私人使用的项目，copyright属于个人。</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>team</p></div></td><td style="text-align:left"><div class="table-cell"><p>team.团队名.项目名.模块名.……</p></div></td><td style="text-align:left"><div class="table-cell"><p>团队项目，指由团队发起，并由该团队开发的项目，copyright属于该团队所有</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>顶级域名</p></div></td><td style="text-align:left"><div class="table-cell"><p>com.公司名.项目名.模块名.……</p></div></td><td style="text-align:left"><div class="table-cell"><p>公司项目，copyright由项目发起的公司所有</p></div></td></tr></tbody></table></div>

## 三、类命名
**类名使用大驼峰命名形式**，类命通常时**名词或名词短语**，接口名除了用名词和名词短语以外，还可以使用形容词或形容词短语，如 Cloneable，Callable
等，表示实现该接口的类有某种功能或能力。对于测试类则以它要测试的类开头，以 Test 结尾，如 HashMapTest。

对于一些特殊特有名词缩写也可以使用全大写命名，比如XMLHttpRequest，不过笔者认为缩写三个字母以内都大写，超过三个字母则按照要给单词算。这个没有标准如阿里巴巴中fastjson用JSONObject作为类命，而google则使用JsonObjectRequest
命名，对于这种特殊的缩写，原则是统一就好。

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>属性</p></div></th><th style="text-align:left"><div class="table-header"><p>约束</p></div></th><th style="text-align:left"><div class="table-header"><p>例</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>抽象类</p></div></td><td style="text-align:left"><div class="table-cell"><p>Abstract 或者 Base 开头</p></div></td><td style="text-align:left"><div class="table-cell"><p>BaseUserService</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>枚举类</p></div></td><td style="text-align:left"><div class="table-cell"><p>Enum 作为后缀</p></div></td><td style="text-align:left"><div class="table-cell"><p>GenderEnum</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>工具类</p></div></td><td style="text-align:left"><div class="table-cell"><p>Utils作为后缀</p></div></td><td style="text-align:left"><div class="table-cell"><p>StringUtils</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>异常类</p></div></td><td style="text-align:left"><div class="table-cell"><p>Exception结尾</p></div></td><td style="text-align:left"><div class="table-cell"><p>RuntimeException</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>接口实现类</p></div></td><td style="text-align:left"><div class="table-cell"><p>接口名+ Impl</p></div></td><td style="text-align:left"><div class="table-cell"><p>UserServiceImpl</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>领域模型相关</p></div></td><td style="text-align:left"><div class="table-cell"><p>/DO/DTO/VO/DAO</p></div></td><td style="text-align:left"><div class="table-cell"><p>正例：UserDAO 反例： UserDo， UserDao</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>设计模式相关类</p></div></td><td style="text-align:left"><div class="table-cell"><p>Builder，Factory等</p></div></td><td style="text-align:left"><div class="table-cell"><p>当使用到设计模式时，需要使用对应的设计模式作为后缀，如ThreadFactory</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>处理特定功能的</p></div></td><td style="text-align:left"><div class="table-cell"><p>Handler，Predicate, Validator</p></div></td><td style="text-align:left"><div class="table-cell"><p>表示处理器，校验器，断言，这些类工厂还有配套的方法名如handle，predicate，validate</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>测试类</p></div></td><td style="text-align:left"><div class="table-cell"><p>Test结尾</p></div></td><td style="text-align:left"><div class="table-cell"><p>UserServiceTest， 表示用来测试UserService类的</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>MVC分层</p></div></td><td style="text-align:left"><div class="table-cell"><p>Controller，Service，ServiceImpl，DAO后缀</p></div></td><td style="text-align:left"><div class="table-cell"><p>UserManageController，UserManageDAO</p></div></td></tr></tbody></table></div>

## 四、方法
方法命名采用小驼峰的形式，首字小写，往后的每个单词首字母都要大写。 和类名不同的是，方法命名一般为动词或动词短语，与参数或参数名共同组成动宾短语，即动词 + 名词。一个好的函数名一般能通过名字直接获知该函数实现什么样的功能。

### 4.1 返回真伪值的方法
注：Prefix-前缀，Suffix-后缀，Alone-单独使用

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>位置</p></div></th><th style="text-align:left"><div class="table-header"><p>单词</p></div></th><th style="text-align:left"><div class="table-header"><p>意义</p></div></th><th style="text-align:left"><div class="table-header"><p>例</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>is</p></div></td><td style="text-align:left"><div class="table-cell"><p>对象是否符合期待的状态</p></div></td><td style="text-align:left"><div class="table-cell"><p>isValid</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>can</p></div></td><td style="text-align:left"><div class="table-cell"><p>对象能否执行所期待的动作</p></div></td><td style="text-align:left"><div class="table-cell"><p>canRemove</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>should</p></div></td><td style="text-align:left"><div class="table-cell"><p>调用方执行某个命令或方法是好还是不好,应不应该，或者说推荐还是不推荐</p></div></td><td style="text-align:left"><div class="table-cell"><p>shouldMigrate</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>has</p></div></td><td style="text-align:left"><div class="table-cell"><p>对象是否持有所期待的数据和属性</p></div></td><td style="text-align:left"><div class="table-cell"><p>hasObservers</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>needs</p></div></td><td style="text-align:left"><div class="table-cell"><p>调用方是否需要执行某个命令或方法</p></div></td><td style="text-align:left"><div class="table-cell"><p>needsMigrate</p></div></td></tr></tbody></table></div>

### 4.2 用来检查的方法

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>单词</p></div></th><th style="text-align:left"><div class="table-header"><p>意义</p></div></th><th style="text-align:left"><div class="table-header"><p>例</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>ensure</p></div></td><td style="text-align:left"><div class="table-cell"><p>检查是否为期待的状态，不是则抛出异常或返回error code</p></div></td><td style="text-align:left"><div class="table-cell"><p>ensureCapacity</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>validate</p></div></td><td style="text-align:left"><div class="table-cell"><p>检查是否为正确的状态，不是则抛出异常或返回error code</p></div></td><td style="text-align:left"><div class="table-cell"><p>validateInputs</p></div></td></tr></tbody></table></div>

### 4.3 按需求才执行的方法

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>位置</p></div></th><th style="text-align:left"><div class="table-header"><p>单词</p></div></th><th style="text-align:left"><div class="table-header"><p>意义</p></div></th><th style="text-align:left"><div class="table-header"><p>例</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>Suffix</p></div></td><td style="text-align:left"><div class="table-cell"><p>IfNeeded</p></div></td><td style="text-align:left"><div class="table-cell"><p>需要的时候执行，不需要的时候什么都不做</p></div></td><td style="text-align:left"><div class="table-cell"><p>drawIfNeeded</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>might</p></div></td><td style="text-align:left"><div class="table-cell"><p>同上</p></div></td><td style="text-align:left"><div class="table-cell"><p>mightCreate</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>try</p></div></td><td style="text-align:left"><div class="table-cell"><p>尝试执行，失败时抛出异常或是返回errorcode</p></div></td><td style="text-align:left"><div class="table-cell"><p>tryCreate</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Suffix</p></div></td><td style="text-align:left"><div class="table-cell"><p>OrDefault</p></div></td><td style="text-align:left"><div class="table-cell"><p>尝试执行，失败时返回默认值</p></div></td><td style="text-align:left"><div class="table-cell"><p>getOrDefault</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Suffix</p></div></td><td style="text-align:left"><div class="table-cell"><p>OrElse</p></div></td><td style="text-align:left"><div class="table-cell"><p>尝试执行、失败时返回实际参数中指定的值</p></div></td><td style="text-align:left"><div class="table-cell"><p>getOrElse</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>force</p></div></td><td style="text-align:left"><div class="table-cell"><p>强制尝试执行。error抛出异常或是返回值</p></div></td><td style="text-align:left"><div class="table-cell"><p>forceCreate, forceStop</p></div></td></tr></tbody></table></div>

### 4.4 异步相关方法

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>位置</p></div></th><th style="text-align:left"><div class="table-header"><p>单词</p></div></th><th style="text-align:left"><div class="table-header"><p>意义</p></div></th><th style="text-align:left"><div class="table-header"><p>例</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>blocking</p></div></td><td style="text-align:left"><div class="table-cell"><p>线程阻塞方法</p></div></td><td style="text-align:left"><div class="table-cell"><p>blockingGetUser</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Suffix</p></div></td><td style="text-align:left"><div class="table-cell"><p>InBackground</p></div></td><td style="text-align:left"><div class="table-cell"><p>执行在后台的线程</p></div></td><td style="text-align:left"><div class="table-cell"><p>doInBackground</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Suffix</p></div></td><td style="text-align:left"><div class="table-cell"><p>Async</p></div></td><td style="text-align:left"><div class="table-cell"><p>异步方法</p></div></td><td style="text-align:left"><div class="table-cell"><p>sendAsync</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Suffix</p></div></td><td style="text-align:left"><div class="table-cell"><p>Sync</p></div></td><td style="text-align:left"><div class="table-cell"><p>对应已有异步方法的同步方法</p></div></td><td style="text-align:left"><div class="table-cell"><p>sendSync</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix or Alone</p></div></td><td style="text-align:left"><div class="table-cell"><p>schedule</p></div></td><td style="text-align:left"><div class="table-cell"><p>Job和Task放入队列</p></div></td><td style="text-align:left"><div class="table-cell"><p>schedule, scheduleJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix or Alone</p></div></td><td style="text-align:left"><div class="table-cell"><p>post</p></div></td><td style="text-align:left"><div class="table-cell"><p>同上</p></div></td><td style="text-align:left"><div class="table-cell"><p>postJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix or Alone</p></div></td><td style="text-align:left"><div class="table-cell"><p>execute</p></div></td><td style="text-align:left"><div class="table-cell"><p>执行异步方法（注：我一般拿这个做同步方法名）</p></div></td><td style="text-align:left"><div class="table-cell"><p>execute, executeTask</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix or Alone</p></div></td><td style="text-align:left"><div class="table-cell"><p>start</p></div></td><td style="text-align:left"><div class="table-cell"><p>同上</p></div></td><td style="text-align:left"><div class="table-cell"><p>start, startJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix or Alone</p></div></td><td style="text-align:left"><div class="table-cell"><p>cancel</p></div></td><td style="text-align:left"><div class="table-cell"><p>停止异步方法</p></div></td><td style="text-align:left"><div class="table-cell"><p>cancel, cancelJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix or Alone</p></div></td><td style="text-align:left"><div class="table-cell"><p>stop</p></div></td><td style="text-align:left"><div class="table-cell"><p>同上</p></div></td><td style="text-align:left"><div class="table-cell"><p>stop, stopJob</p></div></td></tr></tbody></table></div>

### 4.5 回调方法

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>位置</p></div></th><th style="text-align:left"><div class="table-header"><p>单词</p></div></th><th style="text-align:left"><div class="table-header"><p>意义</p></div></th><th style="text-align:left"><div class="table-header"><p>例</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>on</p></div></td><td style="text-align:left"><div class="table-cell"><p>事件发生时执行</p></div></td><td style="text-align:left"><div class="table-cell"><p>onCompleted</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>before</p></div></td><td style="text-align:left"><div class="table-cell"><p>事件发生前执行</p></div></td><td style="text-align:left"><div class="table-cell"><p>beforeUpdate</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>pre</p></div></td><td style="text-align:left"><div class="table-cell"><p>同上</p></div></td><td style="text-align:left"><div class="table-cell"><p>preUpdate</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>will</p></div></td><td style="text-align:left"><div class="table-cell"><p>同上</p></div></td><td style="text-align:left"><div class="table-cell"><p>willUpdate</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>after</p></div></td><td style="text-align:left"><div class="table-cell"><p>事件发生后执行</p></div></td><td style="text-align:left"><div class="table-cell"><p>afterUpdate</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>post</p></div></td><td style="text-align:left"><div class="table-cell"><p>同上</p></div></td><td style="text-align:left"><div class="table-cell"><p>postUpdate</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>did</p></div></td><td style="text-align:left"><div class="table-cell"><p>同上</p></div></td><td style="text-align:left"><div class="table-cell"><p>didUpdate</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>Prefix</p></div></td><td style="text-align:left"><div class="table-cell"><p>should</p></div></td><td style="text-align:left"><div class="table-cell"><p>确认事件是否可以发生时执行</p></div></td><td style="text-align:left"><div class="table-cell"><p>shouldUpdate</p></div></td></tr></tbody></table></div>

### 4.6 操作对象生命周期的方法

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>单词</p></div></th><th style="text-align:left"><div class="table-header"><p>意义</p></div></th><th style="text-align:left"><div class="table-header"><p>例</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>initialize</p></div></td><td style="text-align:left"><div class="table-cell"><p>初始化。也可作为延迟初始化使用</p></div></td><td style="text-align:left"><div class="table-cell"><p>initialize</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>pause</p></div></td><td style="text-align:left"><div class="table-cell"><p>暂停</p></div></td><td style="text-align:left"><div class="table-cell"><p>onPause ，pause</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>stop</p></div></td><td style="text-align:left"><div class="table-cell"><p>停止</p></div></td><td style="text-align:left"><div class="table-cell"><p>onStop，stop</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>abandon</p></div></td><td style="text-align:left"><div class="table-cell"><p>销毁的替代</p></div></td><td style="text-align:left"><div class="table-cell"><p>abandon</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>destroy</p></div></td><td style="text-align:left"><div class="table-cell"><p>同上</p></div></td><td style="text-align:left"><div class="table-cell"><p>destroy</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>dispose</p></div></td><td style="text-align:left"><div class="table-cell"><p>同上</p></div></td><td style="text-align:left"><div class="table-cell"><p>dispose</p></div></td></tr></tbody></table></div>

### 4.7 与集合操作相关的方法

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>单词</p></div></th><th style="text-align:left"><div class="table-header"><p>意义</p></div></th><th style="text-align:left"><div class="table-header"><p>例</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>contains</p></div></td><td style="text-align:left"><div class="table-cell"><p>是否持有与指定对象相同的对象</p></div></td><td style="text-align:left"><div class="table-cell"><p>contains</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>add</p></div></td><td style="text-align:left"><div class="table-cell"><p>添加</p></div></td><td style="text-align:left"><div class="table-cell"><p>addJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>append</p></div></td><td style="text-align:left"><div class="table-cell"><p>添加</p></div></td><td style="text-align:left"><div class="table-cell"><p>appendJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>insert</p></div></td><td style="text-align:left"><div class="table-cell"><p>插入到下标n</p></div></td><td style="text-align:left"><div class="table-cell"><p>insertJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>put</p></div></td><td style="text-align:left"><div class="table-cell"><p>添加与key对应的元素</p></div></td><td style="text-align:left"><div class="table-cell"><p>putJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>remove</p></div></td><td style="text-align:left"><div class="table-cell"><p>移除元素</p></div></td><td style="text-align:left"><div class="table-cell"><p>removeJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>enqueue</p></div></td><td style="text-align:left"><div class="table-cell"><p>添加到队列的最末位</p></div></td><td style="text-align:left"><div class="table-cell"><p>enqueueJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>dequeue</p></div></td><td style="text-align:left"><div class="table-cell"><p>从队列中头部取出并移除</p></div></td><td style="text-align:left"><div class="table-cell"><p>dequeueJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>push</p></div></td><td style="text-align:left"><div class="table-cell"><p>添加到栈头</p></div></td><td style="text-align:left"><div class="table-cell"><p>pushJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>pop</p></div></td><td style="text-align:left"><div class="table-cell"><p>从栈头取出并移除</p></div></td><td style="text-align:left"><div class="table-cell"><p>popJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>peek</p></div></td><td style="text-align:left"><div class="table-cell"><p>从栈头取出但不移除</p></div></td><td style="text-align:left"><div class="table-cell"><p>peekJob</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>find</p></div></td><td style="text-align:left"><div class="table-cell"><p>寻找符合条件的某物</p></div></td><td style="text-align:left"><div class="table-cell"><p>findById</p></div></td></tr></tbody></table></div>

### 4.8 与数据相关的方法

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>单词</p></div></th><th style="text-align:left"><div class="table-header"><p>意义</p></div></th><th style="text-align:left"><div class="table-header"><p>例</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>create</p></div></td><td style="text-align:left"><div class="table-cell"><p>新创建</p></div></td><td style="text-align:left"><div class="table-cell"><p>createAccount</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>new</p></div></td><td style="text-align:left"><div class="table-cell"><p>新创建</p></div></td><td style="text-align:left"><div class="table-cell"><p>newAccount</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>from</p></div></td><td style="text-align:left"><div class="table-cell"><p>从既有的某物新建，或是从其他的数据新建</p></div></td><td style="text-align:left"><div class="table-cell"><p>fromConfig</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>to</p></div></td><td style="text-align:left"><div class="table-cell"><p>转换</p></div></td><td style="text-align:left"><div class="table-cell"><p>toString</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>update</p></div></td><td style="text-align:left"><div class="table-cell"><p>更新既有某物</p></div></td><td style="text-align:left"><div class="table-cell"><p>updateAccount</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>load</p></div></td><td style="text-align:left"><div class="table-cell"><p>读取</p></div></td><td style="text-align:left"><div class="table-cell"><p>loadAccount</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>fetch</p></div></td><td style="text-align:left"><div class="table-cell"><p>远程读取</p></div></td><td style="text-align:left"><div class="table-cell"><p>fetchAccount</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>delete</p></div></td><td style="text-align:left"><div class="table-cell"><p>删除</p></div></td><td style="text-align:left"><div class="table-cell"><p>deleteAccount</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>remove</p></div></td><td style="text-align:left"><div class="table-cell"><p>删除</p></div></td><td style="text-align:left"><div class="table-cell"><p>removeAccount</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>save</p></div></td><td style="text-align:left"><div class="table-cell"><p>保存</p></div></td><td style="text-align:left"><div class="table-cell"><p>saveAccount</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>store</p></div></td><td style="text-align:left"><div class="table-cell"><p>保存</p></div></td><td style="text-align:left"><div class="table-cell"><p>storeAccount</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>commit</p></div></td><td style="text-align:left"><div class="table-cell"><p>保存</p></div></td><td style="text-align:left"><div class="table-cell"><p>commitChange</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>apply</p></div></td><td style="text-align:left"><div class="table-cell"><p>保存或应用</p></div></td><td style="text-align:left"><div class="table-cell"><p>applyChange</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>clear</p></div></td><td style="text-align:left"><div class="table-cell"><p>清除数据或是恢复到初始状态</p></div></td><td style="text-align:left"><div class="table-cell"><p>clearAll</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>reset</p></div></td><td style="text-align:left"><div class="table-cell"><p>清除数据或是恢复到初始状态</p></div></td><td style="text-align:left"><div class="table-cell"><p>resetAll</p></div></td></tr></tbody></table></div>

### 4.9 成对出现的动词

<div class="table-wrapper"><table><thead><tr><th style="text-align:left"><div class="table-header"><p>单词</p></div></th><th style="text-align:left"><div class="table-header"><p>意义</p></div></th></tr></thead><tbody><tr><td style="text-align:left"><div class="table-cell"><p>get获取</p></div></td><td style="text-align:left"><div class="table-cell"><p>set 设置</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>add 增加</p></div></td><td style="text-align:left"><div class="table-cell"><p>remove 删除</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>create 创建</p></div></td><td style="text-align:left"><div class="table-cell"><p>destory 移除</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>start 启动</p></div></td><td style="text-align:left"><div class="table-cell"><p>stop 停止</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>open 打开</p></div></td><td style="text-align:left"><div class="table-cell"><p>close 关闭</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>read 读取</p></div></td><td style="text-align:left"><div class="table-cell"><p>write 写入</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>load 载入</p></div></td><td style="text-align:left"><div class="table-cell"><p>save 保存</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>create 创建</p></div></td><td style="text-align:left"><div class="table-cell"><p>destroy 销毁</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>begin 开始</p></div></td><td style="text-align:left"><div class="table-cell"><p>end 结束</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>backup 备份</p></div></td><td style="text-align:left"><div class="table-cell"><p>restore 恢复</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>import 导入</p></div></td><td style="text-align:left"><div class="table-cell"><p>export 导出</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>split 分割</p></div></td><td style="text-align:left"><div class="table-cell"><p>merge 合并</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>inject 注入</p></div></td><td style="text-align:left"><div class="table-cell"><p>extract 提取</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>attach 附着</p></div></td><td style="text-align:left"><div class="table-cell"><p>detach 脱离</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>bind 绑定</p></div></td><td style="text-align:left"><div class="table-cell"><p>separate 分离</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>view 查看</p></div></td><td style="text-align:left"><div class="table-cell"><p>browse 浏览</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>edit 编辑</p></div></td><td style="text-align:left"><div class="table-cell"><p>modify 修改</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>select 选取</p></div></td><td style="text-align:left"><div class="table-cell"><p>mark 标记</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>copy 复制</p></div></td><td style="text-align:left"><div class="table-cell"><p>paste 粘贴</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>undo 撤销</p></div></td><td style="text-align:left"><div class="table-cell"><p>redo 重做</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>insert 插入</p></div></td><td style="text-align:left"><div class="table-cell"><p>delete 移除</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>add 加入</p></div></td><td style="text-align:left"><div class="table-cell"><p>append 添加</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>clean 清理</p></div></td><td style="text-align:left"><div class="table-cell"><p>clear 清除</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>index 索引</p></div></td><td style="text-align:left"><div class="table-cell"><p>sort 排序</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>find 查找</p></div></td><td style="text-align:left"><div class="table-cell"><p>search 搜索</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>increase 增加</p></div></td><td style="text-align:left"><div class="table-cell"><p>decrease 减少</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>play 播放</p></div></td><td style="text-align:left"><div class="table-cell"><p>pause 暂停</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>launch 启动</p></div></td><td style="text-align:left"><div class="table-cell"><p>run 运行</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>compile 编译</p></div></td><td style="text-align:left"><div class="table-cell"><p>execute 执行</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>debug 调试</p></div></td><td style="text-align:left"><div class="table-cell"><p>trace 跟踪</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>observe 观察</p></div></td><td style="text-align:left"><div class="table-cell"><p>listen 监听</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>build 构建</p></div></td><td style="text-align:left"><div class="table-cell"><p>publish 发布</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>input 输入</p></div></td><td style="text-align:left"><div class="table-cell"><p>output 输出</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>encode 编码</p></div></td><td style="text-align:left"><div class="table-cell"><p>decode 解码</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>encrypt 加密</p></div></td><td style="text-align:left"><div class="table-cell"><p>decrypt 解密</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>compress 压缩</p></div></td><td style="text-align:left"><div class="table-cell"><p>decompress 解压缩</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>pack 打包</p></div></td><td style="text-align:left"><div class="table-cell"><p>unpack 解包</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>parse 解析</p></div></td><td style="text-align:left"><div class="table-cell"><p>emit 生成</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>connect 连接</p></div></td><td style="text-align:left"><div class="table-cell"><p>disconnect 断开</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>send 发送</p></div></td><td style="text-align:left"><div class="table-cell"><p>receive 接收</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>download 下载</p></div></td><td style="text-align:left"><div class="table-cell"><p>upload 上传</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>refresh 刷新</p></div></td><td style="text-align:left"><div class="table-cell"><p>synchronize 同步</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>update 更新</p></div></td><td style="text-align:left"><div class="table-cell"><p>revert 复原</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>lock 锁定</p></div></td><td style="text-align:left"><div class="table-cell"><p>unlock 解锁</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>check out 签出</p></div></td><td style="text-align:left"><div class="table-cell"><p>check in 签入</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>submit 提交</p></div></td><td style="text-align:left"><div class="table-cell"><p>commit 交付</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>push 推</p></div></td><td style="text-align:left"><div class="table-cell"><p>pull 拉</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>expand 展开</p></div></td><td style="text-align:left"><div class="table-cell"><p>collapse 折叠</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>begin 起始</p></div></td><td style="text-align:left"><div class="table-cell"><p>end 结束</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>start 开始</p></div></td><td style="text-align:left"><div class="table-cell"><p>finish 完成</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>enter 进入</p></div></td><td style="text-align:left"><div class="table-cell"><p>exit 退出</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>abort 放弃</p></div></td><td style="text-align:left"><div class="table-cell"><p>quit 离开</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>obsolete 废弃</p></div></td><td style="text-align:left"><div class="table-cell"><p>depreciate 废旧</p></div></td></tr><tr><td style="text-align:left"><div class="table-cell"><p>collect 收集</p></div></td><td style="text-align:left"><div class="table-cell"><p>aggregate 聚集</p></div></td></tr></tbody></table></div>

## 五、变量&常量命名
### 5.1 变量命名
变量是指在程序运行中可以改变其值的量，包括成员变量和局部变量。变量名由多单词组成时，第一个单词的首字母小写，其后单词的首字母大写，俗称骆驼式命名法（也称驼峰命名法），如
computedValues，index、变量命名时，尽量简短且能清楚的表达变量的作用，命名体现具体的业务含义即可。

变量名不应以下划线或美元符号开头，尽管这在语法上是允许的。变量名应简短且富于描述。变量名的选用应该易于记忆，即，能够指出其用途。尽量避免单个字符的变量名，除非是一次性的临时变量。pojo中的布尔变量，都不要加is(数据库中的布尔字段全都要加
is_ 前缀)。
### 5.2 常量命名
常量命名CONSTANT_CASE，一般采用全部大写（作为方法参数时除外），单词间用下划线分割。那么什么是常量呢?

常量是在作用域内保持不变的值，一般使用final进行修饰。一般分为三种，全局常量（public static final修饰），类内常量（private static final
修饰）以及局部常量（方法内，或者参数中的常量），局部常量比较特殊，通常采用小驼峰命名即可。

```java
public class HelloWorld {

/**
* 局部常量(正例)
*/
public static final long USER_MESSAGE_CACHE_EXPIRE_TIME = 3600;

/**
* 局部常量(反例，命名不清晰）
*/
public static final long MESSAGE_CACHE_TIME = 3600;

/**
* 全局常量
*/
private static final String ERROR_MESSAGE = " error message";

/**
* 成员变量
*/
private int currentUserId;

/**
* 控制台打印 {@code message} 信息
*
* @param message 消息体，局部常量
*/
public void sayHello(final String message){
System.out.println("Hello world!");
}

}
```

常量一般都有自己的业务含义,**不要害怕长度过长而进行省略或者缩写**。如，用户消息缓存过期时间的表示，那种方式更佳清晰，交给你来评判。
## 通用命名规则
1.尽量不要使用拼音；杜绝拼音和英文混用。对于一些通用的表示或者难以用英文描述的可以采用拼音，一旦采用拼音就坚决不能和英文混用。
正例： BeiJing， HangZhou
反例： validateCanShu
2.命名过程中尽量不要出现特殊的字符，常量除外。
3.尽量不要和jdk或者框架中已存在的类重名，也不能使用java中的关键字命名。
4.妙用介词，如for(可以用同音的4代替), to(可用同音的2代替), from, with，of等。
如类名采用User4RedisDO，方法名getUserInfoFromRedis，convertJson2Map等。
## 六、代码注解
### 6.1 注解的原则
好的命名增加代码阅读性，代码的命名往往有严格的限制。而注解不同，程序员往往可以自由发挥，单并不意味着可以为所欲为之胡作非为。优雅的注解通常要满足三要素。

1.Nothing is strange
没有注解的代码对于阅读者非常不友好，哪怕代码写的在清除，阅读者至少从心理上会有抵触，更何况代码中往往有许多复杂的逻辑，所以一定要写注解，不仅要记录代码的逻辑，还有说清楚修改的逻辑。

2.Less is more
从代码维护角度来讲，代码中的注解一定是精华中的精华。合理清晰的命名能让代码易于理解，对于逻辑简单且命名规范，能够清楚表达代码功能的代码不需要注解。滥用注解会增加额外的负担，更何况大部分都是废话。
`
// 根据id获取信息【废话注解】
getMessageById(id)
`
3.Advance with the time
注解应该随着代码的变动而改变，注解表达的信息要与代码中完全一致。通常情况下修改代码后一定要修改注解。

### 6.2 注解格式
注解大体上可以分为两种，一种是javadoc注解，另一种是简单注解。javadoc注解可以生成JavaAPI为外部用户提供有效的支持javadoc注解通常在使用IDEA，或者Eclipse等开发工具时都可以自动生成，也支持自定义的注解模板，仅需要对对应的字段进行解释。参与同一项目开发的同学，尽量设置成相同的注解模板。

#### a. 包注解
包注解在工作中往往比较特殊，通过包注解可以快速知悉当前包下代码是用来实现哪些功能，强烈建议工作中加上，尤其是对于一些比较复杂的包，包注解一般在包的根目录下，名称统一为package-info.java。

```java
/**
* 落地也质量检测
* 1. 用来解决什么问题
* 对广告主投放的广告落地页进行性能检测，模拟不同的系统，如Android，IOS等; 模拟不同的网络：2G，3G，4G，wifi等
*
* 2. 如何实现
* 基于chrome浏览器，用chromedriver驱动浏览器，设置对应的网络，OS参数，获取到浏览器返回结果。
*
* 注意： 网络环境配置信息{@link cn.mycookies.landingpagecheck.meta.NetWorkSpeedEnum}目前使用是常规速度，可以根据实际情况进行调整
*
* @author author
* @time 2019/12/7 20:3 下午
*/
package cn.mycookies.landingpagecheck;
```

#### b. 类注接
javadoc注解中，每个类都必须有注解。
```java
/**
* Copyright (C), 2019-2020, Jann balabala...
*
* 类的介绍：这是一个用来做什么事情的类，有哪些功能，用到的技术.....
*
* @author 类创建者姓名 保持对齐
* @date 创建日期 保持对齐
* @version 版本号 保持对齐
*/
```
#### c. 属性注解
在每个属性前面必须加上属性注释，通常有一下两种形式，至于怎么选择，你高兴就好，不过一个项目中要保持统一。
```java
/** 提示信息 */
private String userName;
/**
* 密码
*/
private String password;
```
#### d. 方法注释
在每个方法前面必须加上方法注释，对于方法中的每个参数，以及返回值都要有说明。
```java
/**
* 方法的详细说明，能干嘛，怎么实现的，注意事项...
*
* @param xxx 参数1的使用说明， 能否为null
* @return 返回结果的说明， 不同情况下会返回怎样的结果
* @throws 异常类型 注明从此类方法中抛出异常的说明
*/
```
#### e. 构造方法注释
在每个构造方法前面必须加上注释，注释模板如下：
```java
/**
* 构造方法的详细说明
*
* @param xxx 参数1的使用说明， 能否为null
* @throws 异常类型 注明从此类方法中抛出异常的说明
*/
```
而简单注解往往是需要工程师字节定义，在使用注解时应该注意一下几点：

1.枚举类的各个属性值都要使用注解，枚举可以理解为是常量，通常不会发生改变，通常会被在多个地方引用，对枚举的修改和添加属性通常会带来很大的影响。
2.保持排版整洁，不要使用行尾注释；双斜杠和星号之后要用1个空格分隔。
```java
int id = 1;// 反例：不要使用行尾注释
//反例：换行符与注释之间没有缩进
int age = 18;
// 正例：姓名
String name;
/**
* 1. 多行注释
*
* 2. 对于不同的逻辑说明，可以用空行分隔
*/
```
## 声明
本文转载自：https://www.cnblogs.com/liqiangchn/p/12000361.html
<style>
    .table-wrapper th {
        padding: 12px 16px;
        border: 1px solid #E1E6F0;
        background-color: #F5F7FA;
        color: #677489;
        text-align: left;
        font-weight: normal;
        word-break: keep-all;
    }

    .table-wrapper {
        width: 100%;
        /*表格宽度*/
        max-width: 65em;
        /*表格最大宽度，避免表格过宽*/
        margin: 15px auto;
        /*外边距*/
        border-collapse: collapse;
        /*使用单一线条的边框*/
        empty-cells: show;
        /*单元格无内容依旧绘制边框*/
    }

    .table-wrapper th,
    .table-wrapper td {
        height: 35px;
        /*统一每一行的默认高度*/
        border: 1px solid #E1E6F0;
        /*内部边框样式*/
        padding: 12px 16px;
        /*内边距*/
    }

    .table-wrapper td {
        font-weight: bold
    }
    .table-wrapper table{
        width: inherit;
    }
    .table-wrapper p{
        margin: 0px;
    }
</style>