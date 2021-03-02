# 文件分片上传服务端

## 功能：  
### FileController：  
1.文件分片上传：分片文件上传到服务器并存储在临时目录中，同时缓存已上传分片索引。  
2.合并分片文件：所有分片文件都上传后，服务器合并临时分片文件为原始大文件，并存储到正式的存储目录，同时删除临时文件和相关缓存。  
3.已上传分片信息查询：可以查询已上传的分片索引，用于识别未上传分片  
4.文件上传鉴权：提供上传鉴权接口 

### TempFileTask：  
1.定时对上传完毕的分片文件执行合并操作  
2.定时对超出存储时间的临时文件执行清理操作  

https://www.cnblogs.com/Marydon20170307/p/13847588.html  
https://www.cnblogs.com/codhome/p/13621169.html  
https://blog.csdn.net/weixin_30872337/article/details/97418485  
http://www.blogjava.net/devin/archive/2010/07/20/326618.html?opt=admin  
