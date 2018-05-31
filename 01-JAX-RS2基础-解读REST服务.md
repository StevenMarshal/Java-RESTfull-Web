## 1.2 解读REST服务

RESTful对应的中文是REST式的。  
RESTful Web Service的准确翻译为REST式的Web服务（REST服务）。  
RESTful的应用或者Web服务式最常见的两种REST式的项目部署、存在的方式。  

### 1.2.1 REST式的Web服务

RESTful Web Service是一种遵守REST式风格的Web服务。  
REST服务是一种ROA（Resource – Oriented Architecture，面向资源的架构）应用。其主要特点是方法信息存在于HTTP协议的方法中（比如GET、PUT），作用域存在于URI中。例如，一个获取设备资源列表的GET请求中，方法信息是GET，作用域信息是URI中包含的对设备资源的过滤、分页和排序等条件。

### 1.2.2 对比RPC风格

相比Web服务领域广为流行的RPC（Remote Procedure Call Protocol，远程过程调用协议）风格。


|  对比项  |	REST  |  	RPC（Remote Procedure Call Protocol，远程过程调用协议）|
|--------|--------|-----------------------------------------------------------|  
|  风格    |	轻量和快速  |   ————   |	
|  方法信息  |  	采用标准HTTP方法。  |	都是HTTP协议的POST方法，方法信息包含于SOAP协议包或HTTP协议包中，方法名称不具有通用性。  |  
|作用域角度|采用URI显示定义作用域。|包含于协议包中，不能直观呈现。|
|————| 面向资源状态的 |	RPC风格的开发关注于服务器—客户端之间的方法调用，而不关注基于哪个网络层协议，即RPC是面向方法调用过程的。|
|风格代表| ———— |		XML-RPC，大Web服务|

#### 1.2.2.1 XML-RPC

XML-RPC是一种使用XML格式封装方法调用，并使用HTTP协议作为传送机制的RPC风格的实现。  
XML-RPC的请求方法都是HTTP协议的POST方法，请求和响应的数据格式均为XML。  
数据内容上的不同：  

* REST式的XML信息的主体是对一个资源状态的表述，无须包含方法信息。
* XML-RPC的请求数据结构额外包含方法调用信息和参数信息。

响应信息内容上的不同：

* REST式通常会包含响应实体信息，以及HTTP状态码和可选的异常信息。
* XML-RPC的返回信息仅仅是对方方法调用的响应信息。

#### 1.2.2.2 大Web服务

大Web服务（Big Web Service）是Leonard Richardson和Sam Ruby在其所著的《RESTful Web Services》一书中，对基于SOAP + WSDL + UDDI + WS标准栈等技术实现RPC风格的大型Web服务的统称。  

相比较REST式的Web服务：

* 大Web服务功能强大、设计更复杂。
* 同样是跨平台、跨语言的，对复杂的数据类型的支持也非常好。
* 由于大Web服务是基于RPC风格的重量设计，所以方法和作用域无法通过直观进行断定，需要定义在消息中，方法名也不是统一和通用的。

对比RPC风格的Web服务：

* REST式的Web服务形式更简单、设计更轻量、实现更快捷。
* 无须引入SOAP消息传输层，无须注册服务，没有客户端的stub概念等。
REST式的Web服务没有像大Web服务那样提供诸如安全策略等全面的标准规范。

两者各有优势，没有相互替代关系。