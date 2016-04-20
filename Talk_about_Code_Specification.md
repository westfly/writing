## 聊聊代码规范 ##

不论在哪一家公司，不论是哪一种语言，Coder们总会或显式或隐式地逐渐形成一种编码约定，这其实就是编码规范。今天，我们在这里简单的聊聊代码规范。由于平时工作中涉及的编程语言主要以Java为主，所以下面讨论的主要是Java的代码规范，不过有些思想对其他的语言规范也同样有所借鉴。

#### 1. 为什么需要代码规范 ####

在谈论具体的代码规范内容之前，我们先思考一个问题：为什么需要代码规范？或者说代码规范主要是用以解决什么问题？
在我的理解中，一份代码规范主要解决以下几个问题：

##### 交流沟通效率问题 #####

从个人的代码规范而言，一致的代码风格，对于你隔一段时间回过头来看自己以前写的代码，能够很大程度上减少自己重新梳理的成本。

扩大一点范围，从个人所在的团队而言，一份代码规范，能够减少团队同事在互相backup时，接手遗留项目时，新同事熟悉团队Code Base时的理解成本。一旦能够快速有效理解代码的话，就实质上已经降低了沟通成本。

再扩大一点范围，从个人所在的整个公司而言，代码规范能够有助于跨团队合作时熟悉彼此接口交互，能够极大减少移交/接手其他团队Code Base时的理解和沟通成本。而这个理解和沟通成本往往是影响项目迭代的首要因素。

再再扩大范围，从某个编程语言的范畴而言，代码规范能够很好的降低某个编程语言开发者之间的交流沟通成本。而开发者的技术水平的提高，往往都离不开社区、个人彼此之间的交流沟通。特别是你参与到一个开源项目或者你发布一个开源项目时，制定一份合理的代码规范，往往是项目发展壮大过程中必不可少的一个重要步骤。

##### 犯错误概率问题 #####
首先，交流沟通本身就存在一个理解偏差的问题，而代码规范在一定程度上就明确了某些场景下的一些模糊问题的定义，从而能够减少由于沟通理解偏差导致的犯错概率。其次，一份好的代码规范都是在具体某个编程语言最佳实践的基础之上制定的，并且随着时间不断迭代改进。这些最佳实践本身大都是前人的失败错误经验总结，当然能够很大程度上降低编码犯错的概率。

#### 2. 一份代码规范主要包含那几个部分内容 ####

计算机编程能够解决的问题，肯定在现实生活中已经有既定的解决方案。计算机编程实际上可以看作是一个通过编程来对现实生活问题解决方案进行再创造的过程。在这个过程中，不同的编程劳动必定存在一些共性和差异的地方，这反映到不同的代码规范中，也必定会有一些共性的规范和差异。

一份好的代码规范包含但不仅限于下面几个部分内容：

**(1) 代码结构规范**

在Java编程语言中，Maven的代码组织结构，已经成为既定的一种代码结构规范。

    src
    |-- main
        |-- java
        |-- resources
        |-- webapp
        |-- scripts
        |-- assembly
    |-- test 
        |-- java
        |-- resources
    LICENSE.txt
    README.txt

**(2) 格式化规范**

常见的格式化规范主要包含以下几种：

- 规定'()','[]','{}'的格式化;
- 规定代码块的缩进；
- 列长度限制；
- 空格及转义字符的要求；
- 类的声明、构造、初始化格式；
- 变量、数组等声明、初始化格式；
- 语句的格式；
- 类、变量等修饰符的声明格式；
- 注释、字面量的格式；

针对具体的语言，可能还会有一些特有的格式化规范，例如Java语言代码规范往往还会包含下面几种：

- import的格式化；
- 对象属性、类属性、对象初始化块、类初始化块等组织顺序要求；
- package的格式化；

**(3) 命名规范**

以Java语言编程规范为例，主要包含以下几种命名规范：

- 包命名；
- 类命名；
- 方法命名；
- 常量命名；
- 对象属性命名；
- 参数命名；
- 局部变量命名；
- 类型变量命名；
- 配置文件命名；

一个Java语言中普适的命名原则：Camel case（驼峰式）。上述不同的标识命名规则大都以此基础上，再做细微调整。例如：对象属性命名，通常以首字母小写开头，后续每个单词的首字母大写，如xmlHttpRequest。更详细的Java命名规范可以参考《Clean Code》[中文名：代码整洁之道]。


**(4) 最佳实践**

同样以Java语言为例，一些被普遍接受的最佳实践：

- 总是标注@Override；
- 总是catch Exception；
- 总是通过类来引用其静态属性；
- 不使用Finalizer；
- 在Override类的equals方法的同时，要Override hashCode方法
- 不使用对象的初始化块；

更多的Java最佳实践可以参考《Effective Java》。

在这个基础之上，公司或者团队往往会总结并沉淀下来一些内部的最佳实践。例如：

- 如何实现安全的单例初始化；
- 如何合理地使用线程池；
- 如何合理地使用List、Map、Set等Java Collection；
- 如何正确地使用HttpClient、Netty等开源类库；

而上面这每一个最佳实践扩展开来，往往都需要一到多篇文章来讲解。后续有机会针对这块单独再聊聊，在此不表。

**(5) 文档规范**



#### 3. 如何制定和践行代码规范 ####


#### 4. 可参考的文档 ####
