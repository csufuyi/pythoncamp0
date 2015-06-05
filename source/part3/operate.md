## 运营问题总结


- 小小书童豆瓣授权失败
2015.06.04 16：00-24：00 
sae日志：No JSON object could be decoded

```
[2015/06/04 19:33:46] - raise ValueError("No JSON object could be decoded") yq34
[2015/06/04 19:33:46] - File "/usr/local/sae/python/lib/python2.7/json/decoder.py", line 384, in raw_decode yq34
[2015/06/04 19:33:46] - obj, end = self.raw_decode(s, idx=_w(s, 0).end()) yq34
[2015/06/04 19:33:46] - File "/usr/local/sae/python/lib/python2.7/json/decoder.py", line 366, in decode yq34
[2015/06/04 19:33:46] - return _default_decoder.decode(s) yq34
[2015/06/04 19:33:46] - File "/usr/local/sae/python/lib/python2.7/json/init.py", line 338, in loads yq34
[2015/06/04 19:33:46] - return json.loads(self.text, **kwargs) yq34
[2015/06/04 19:33:46] - File "/data1/www/htdocs/708/freesz/1/site-packages/requests/models.py", line 741, in json yq34
[2015/06/04 19:33:46] - return self.resp.json() yq34
[2015/06/04 19:33:46] - File "/data1/www/htdocs/708/freesz/1/site-packages/pyoauth2/libs/response.py", line 42, in parsed yq34
[2015/06/04 19:33:46] - opts.update(self.response.parsed) yq34
[2015/06/04 19:33:46] - File "/data1/www/htdocs/708/freesz/1/site-packages/pyoauth2/client.py", line 39, in get_token yq34
```

联系豆瓣工程师:  
目前看来可能是sae上有人在滥用豆瓣账号的接口， 220.181.136.229 这个出口ip被封了，你们就被误杀了。
https://sae.sina.com.cn/doc/php/fetchurl.html

豆瓣将我们的每小时次数提升到最高2K, oh yeah!

- saecloud 晚饭时段容易出现svn错误无法deploy代码

- sae kvdb 出现过无法访问，可以去sae论坛寻求帮助
 


