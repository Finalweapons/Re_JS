<h1>58同城简历信息爬取(字体加密逆向)</h1>
<p>原理:获取嵌入html源码中的font字体文件,
文件以base64编码的形势存在于网页之中<br>自行解码后即可获得完整的字体文件(woff)文件.目前的58字体加密除了编码和字体之间的映射关系在变化以外,
字形的模样也在不断的变化,所以<br>已经无法通过手动建立字形和字符的对照表来识别字体
这里我采用的是先将文字按照字体文件里面的笔画画出来,<br>然后将生成一张包含所有字的图片,交给百度的OCR识别API来获取文字内容
并通过识别到的文字内容来建立字体与编码的映射关系</p>
<p>由于我没有写登录相关的代码,所以如果要运行项目的话需要手动复制下登录后的Cookies</p>