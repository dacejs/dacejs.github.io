# dacejs.github.io

## 教程
- [入门](01.get-started.md)
- [页面之间的导航](02.navigate-between-pages.md)
- [使用共享组件](03.using-shared-components.md)
- [创建动态页面](04.create-dynamic-pages.md)
- [使用路由创建干净的URL](05.clean-urls.md)
- [为页面获取数据](06.fetching-data-for-pages.md)
- [组件样式](08.styling-components.md)
- [部署](09.depoying-a-nextjs-app.md)

## FAQ
### 如何自定义 eslint 规则
在工程根目录新建一个 `.eslintrc.js`

```js
module.exports = {
  extends: [
    'dace/.eslintrc.js'
  ].map(require.resolve)
};
```

## API
-
