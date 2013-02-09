js
==

Version: v1.1.3
  1）修改Google结果页面打开目标网页的连接，减少被ZF缺德网重置的可能性 
  2）修改Google结果页面的翻页连接，也是减少被重置 
  3）下面介绍了一种修改Chrome地址栏搜索的配置方式，进一步减少可能的被重置！

v1.1 
  修改翻页连接，翻页很多时候也被重置了。 
  
v1.0
  fix urls broken redirt in google.com.hk (or google.com) result page. 
  Google搜索时候，它将url变得很复杂(它需要跟踪用户行为)，导致很容易给GWF拦截。
  而且打开一个被已知拦截的网站，可能导致Google也被reset了。 本脚本主要解决上面的问题，
  同时增加了一个修改默认搜索的小技巧，可以有效降低被拦截的可能性。


More useful operations:
  After you search some words on Google, it will show you a result page containing more than 10 result url. 
  Every url will change into a complex url when you click it. This will cause some problems when you are in China (F*ck GWF)

  This script changes the url

 http://www.google.com.hk/url?sa=t&rct=j&q=good&source=web&cd=2&ved=0CDwQFjAB&url=http%3A%2F%2Fwww.good.is%2F&ei=b1DlToC5Gq6tiQevlNW2BQ&usg=AFQjCNEGmYZ_LuxOMP3stj_6JBQRCzGUnA)
into
http://www.good.is/
, trying to make you access the webpage directly.


** Another tip for Chrome 
modify chrome's default search engine 
1) change the current default search engine, ex: from google.com.hk to google.com 
2) add a new search engine configure, set url (this is important):

http://www.google.com/search?ie={inputEncoding}&q=%s

or 
http://www.google.com.hk/search?ie={inputEncoding}&q=%s

3) set the new search engine to be the default one.
