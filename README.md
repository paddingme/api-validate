# api-validate


在前后端分离项目中，前后端定义好 API 之后，后端同学总是不按照定义好的文档写 API 接口。

想做的就是是后端写好 API 接口之后 输入其 服务器的 地址， 服务器会要 API 文档对其该服务器下 所有接口 进行 验证格式。


1. 输入 API 文档地址拿到 API 定义 JSON 文件

  我们的 API 文档地址一般 为 http://192.168.0.219/lzx/doc/xsczda
  API 文档是由 APIDOC 通过定义 api.js 生成 静态网站，其中会 api.js 会转化为 api_data.json, 我们只要到 API 文档网站所在的目录下 读取到 api_data.json 即可拿到该文档。

  简而言之就是拿到  http://192.168.0.219/lzx/doc/xsczda/api_data.json

  - [ ] 读取 api_data.json

  - [ ] 拿到API 路径前缀 或者输入 如：/xspj/api/

  - [ ] 输入 Token, 或者用 userid 生成 token


2.  输入后端服务器 地址 例如 http://localhost/  进行匹配。

    API 路由匹配： host(http://localhost/) + API 前缀（/xspj/api/） + API 文档中的路由 （/who）

    如果没有路由，则遍历 api_data.json 中的 所有路由。


3. 向后端服务器发送 API 请求，拿回 json 数据 验证

4. 验证 API 请求

   - [ ] 1. 每个请求都必须验证成功或者失败 [尤其是对于 PUT、DELETE、POST 请求]
   - [ ] 2. TOKEN 没有或者错误 应该返回 401
   - [ ] 3. GET 模拟参数 成功
   - [ ] 4. POST 模拟参数 （X-WWW-UNURLENCODED） 成功/失败
   - [ ] 5. PUT 模拟参数  成功/失败
   - [ ] 6. DELETE 模拟参数 成功/失败
   - [ ] 7. 首先是检查 状态码 是否正确
   - [ ] 8. 严格检查返回的 json 数据格式
   - [ ] 9. 打印报错信息（先指描述哪条 API 错误，再具体到 API 路径哪个错误）






