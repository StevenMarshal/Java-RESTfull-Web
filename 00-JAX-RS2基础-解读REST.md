REST（Representational State Transfer），意思是“表术性状态转移”。来源于Thomas Fielding博士在2000年就读加州大学欧文分校期间发表的一篇学术论文《Architectural  Styles and the Design of Network-based Software Architectures》。    

REST之父在该论文中提出了REST的6个特点：  

* 客户端—服务器
* 无状态的
* 可缓存的
* 统一接口
* 分层系统
* 按需编码

## 1.1 解读REST

### 1.1.1 REST是一种架构风格。
  
在这种架构风格中，对象被视为一种资源，通常使用概念清晰的名字命名。  
表述性状态指资源数据在某个瞬间的状态快照。  
表述格式有：XML、JSON、Atom等。  

REST的资源是可寻址的，通过HTTP 1.1协议（RFC 2616）定义的通用动词方法：GET、PUT、DELETE、POST。  
使用URI协议（RFC3305）来唯一标识某个资源公布出来的接口。  

请求一个资源的过程可以理解为访问一个具有指定性和描述性的URI，通过HTT协议，将资源的表述从服务器“转移”到客户端或者相反方向。  

REST不是一种技术（technology），也不是一个标准（standard）/协议（protocol），而是一种使用既有标准：HTTP + URI + XML（XML已经成为数据格式的借指，而不仅代表XML本身）来实现其要求的架构风格。  
因此，与之对应的不是SOAP协议，而是像RPC这样的架构风格。

### 1.1.2 基本实现形式

HTTP + URI + XML是REST的基本实现形式，但不是唯一的实现形式。  
REST开始是通过HTTP协议（RFC2616）、URI协议（RFC3305）来描述其特征，并没有对如何使用一种编程语言来实现进行相关的描述和规定，甚至包括使用哪些传输类型或者数据格式也没有进行详细说明，通常的实现则至少包含XML格式。  

具体而言，HTTP协议和URI用于统一接口和定位资源，文本、二进制流、XML和JSON等格式用来作为资源的表述。  
使用HTTP + URI + XML实现REST的好处是让开发者持有这些已知的技术来开发REST，则关注点更容易在REST的核心概念和业务逻辑上。  

REST是一种架构风格。学习和使用REST的关键是掌握这种思想，而不是具体的实现形式。
