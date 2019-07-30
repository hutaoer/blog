# chrome_get_request_bug
* 场景，点击下载excel文件的时候，如果get请求参数值带有逗号分隔，则会下载失败。
* 错误提示：`ERR_RESPONSE_HEADERS_MULTIPLE_CONTENT_DISPOSITION`.
* 使用谷歌浏览器下载文件名中带有`英文半角逗号`的文件时，请求已发送，但响应时发生浏览器崩溃现象，页面提示 ERR_RESPONSE_HEADERS_MULTIPLE_CONTENT_DISPOSITION ，其他浏览器无此现象，查到是`chrome` 浏览器的bug