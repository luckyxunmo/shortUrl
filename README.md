# shortUrl

短链生成器，将一个长链接转换为短链接  
首先我们使用hash 算法将长链接转换为固定长度，代码使用了 murmur3  
然后在网址 URL 中，常用的合法字符有 0～9、a～z、A～Z 62个字符,为了将短地址变的更短一些，，将10进制的哈希值转换为62进制  
eg:   
网址 https://github.com/luckyxunmo/shortUrl/" 经过hash 运算后为 1815391910，然后使用62进制表示为 1YRcmG  
所以对应的断链为 https://{domain}/1YRcmG  
