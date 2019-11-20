# 企业级后台设计

## 权限系统

## 常用的权限模型
ACL(Access Control List)(访问控制列表)
DAC(Discretionary Access Control)(自主访问控制)
MAC(Mandatory Access Control)(强制访问控制)
RBAC(Role-Based Access Control)(基于角色的访问控制)，常用且推荐。
ABAC(Attribute-Based Access Control)(基于属性的访问控制)，实现复杂，动态计算，拼接sql.

## 实践
* 表格查询抽象：https://juejin.im/post/5ca3314d6fb9a05e2726a84c，项目：https://github.com/Tianlikai/mobxSpa


## 脚手架
* 动态加载：react-loadable的作用
由于路由只是组件，我们仍然可以在路由级别轻松地进行代码拆分。
在你的应用程序中引入新的代码分割点应该是如此简单，以至于你不会再三考虑。这应该是一个改变几行代码和其他一切都应该自动化的问题。
Loadable是一个高阶组件(一个创建组件的函数)，它允许您在将任何模块呈现到应用程序之前动态加载它。

## 表单配置
* noform: https://zhuanlan.zhihu.com/p/44120143
  - 联动的控制
  - https://github.com/alibaba/nopage
  - https://alibaba.github.io/nopage/#/nopage/noform/if
* uform: https://zhuanlan.zhihu.com/p/66002856, https://zhuanlan.zhihu.com/p/62927004, https://github.com/alibaba/uform
* 依赖拖拽库：Drag and Drop for React http://react-dnd.github.io/react-dnd

### 组件间通信
* eventEmitter or redux
* 
