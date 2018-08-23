# Mock 数据

Mock 数据文件存放在工程根目录下的 `mock` 目录，该目录主要存放网站本地开发时网页ajax异步请求接口返回的数据。

Mock 服务只在 dev 环境下运行，服务运行在 `http://localhost:3002` 上，可以通过传递环境变量 `DACE_MOCK_PORT` 来修改端口号，可以通过传递环境变量 `DACE_MOCK_RULES_CONFIG` 来修改转发规则配置文件的位置。

数据文件有两类：

- json：返回 `json` 数据，不可编程。
- js：返回一个模块，可以是数据模块，也可以是函数模块。

```js
module.exports = (req, res, next) => [
  {
    "id": 1,
    "title": "React vs vue"
  },
  {
    "id": 2,
    "title": "Javascript - the best language"
  },
  {
    "id": 3,
    "title": "Java"
  }
]
```

## 参数
当数据文件返回为函数模块时，该函数可以会接收3个参数：

### request
HTTP request请求，通过该参数可以拿到请求提交过来的参数、cookie等。

### response
HTTP response相应，可以控制该参数来实现返回json数据、修改cookie、发送错误码、重定向等功能。

### next
跳转到下一个中间件。

## 返回值
`json` 字符串、函数或者直接操作 `response` 对象。

## 示例
[mock-data](https://github.com/dacejs/dace/tree/master/examples/mock-data)
