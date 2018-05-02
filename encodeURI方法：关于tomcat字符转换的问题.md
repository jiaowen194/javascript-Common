## 一条get请求：
   export?fileName=垫支管理导出20180502&titleMap={"cuser.nickname":"货主名称","amount":"充值金额"}

#### tomcat 报错：Invalid character found in the request target.  
大概意思是说 不认识某些传过来的请求文件 

在测试时发现使用post就可以请求成功

后得到方式  需要通过javascript 的encodeURI方法  对 整个请求字符串进行转码得到以下字符：
http://localhost:8080/yrsoft_start_systemWeb/advance/export?fileName=%E5%9E%AB%E6%94%AF%E7%AE%A1%E7%90%86%E5%AF%BC%E5%87%BA20180502&titleMap=%7B%22shipperName%22:%22%E8%B4%A7%E4%B8%BB%E5%90%8D%E7%A7%B0%22%7D
