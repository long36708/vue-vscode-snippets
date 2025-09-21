# Vue VSCode 代码片段

![vue-snippet-hero](https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/vue-snippet-hero.gif)

## 描述

这些代码片段旨在以最无缝的方式提升您的工作流程。

这个仓库特别为实际使用场景而构建。它不记录API定义，而是从实际使用的角度关注开发者的使用体验。包含了我个人厌倦重复输入的内容，以及有助于快速搭建的样板代码。

_支持的版本：Vue 2 和 Vue 3_

![SnippetDemo](https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/SnippetDemo.gif)

## 安装

_方法一_

- 点击扩展按钮（编辑器中最下方的方块图标），搜索 "Vue VSCode Snippets"，选择由 sdras 提供的扩展

_方法二_

- 访问 [VSCode 扩展市场](https://marketplace.visualstudio.com/items?itemName=sdras.vue-vscode-snippets)

```javascript
ext install Vue VSCode Snippets
```

您可以启用Tab键补全（推荐），通过打开 `Code > Preferences > Settings`（在Mac上）并在您的个人设置中添加 `"editor.tabCompletion": "onlySnippets"`

## 代码片段

### Vue 组件基础

这些代码片段旨在为您的单文件组件（SFC）提供基础脚手架。

| 代码片段          | 用途                                     |
| ----------------- | ---------------------------------------- |
| `vbase-3-ss`      | 使用 script setup 的 SFC 基础模板        |
| `vbase-3-ss-ts`   | 使用 script setup 和 TypeScript 的 SFC 基础模板 |
| `vbase`           | 使用 SCSS 的 SFC 基础模板                |
| `vbase-3`         | 使用 Composition API 和 SCSS 的 SFC 模板 |
| `vbase-3-setup`   | 使用 setup Composition API 和 SCSS 的 SFC 模板 |
| `vbase-3-reactive`| 使用 Composition API、Reactive 和 SCSS 的 SFC 模板 |
| `vbase-css`       | 使用 CSS 的 SFC 基础模板                 |
| `vbase-pcss`      | 使用 PostCSS 的 SFC 基础模板             |
| `vbase-styl`      | 使用 Stylus 的 SFC 基础模板              |
| `vbase-ts`        | 使用 TypeScript 的 SFC 基础模板          |
| `vbase-ts-class`  | 使用 TypeScript 类格式的 SFC 基础模板   |
| `vbase-3-ts`      | 使用 Composition API 和 TypeScript 的 SFC 模板 |
| `vbase-3-ts-setup`| 使用 setup Composition API 和 TypeScript 的 SFC 模板 |
| `vbase-ns`        | 无样式的 SFC 模板                       |
| `vbase-sass`      | 使用 SASS 的 SFC 基础模板               |
| `vbase-less`      | 使用 LESS 的 SFC 基础模板               |

### 模板相关

| 代码片段           | 用途                             |
| ----------------- | -------------------------------- |
| `vfor`            | v-for 指令                      |
| `vmodel`          | 语义化的 v-model 指令           |
| `vmodel-num`      | 语义化的 v-model 数字指令       |
| `von`             | v-on 点击处理函数（带参数）     |
| `vslot-named`     | 具名插槽                         |
| `vel-props`       | 带 props 的组件元素             |
| `vsrc`            | 图片 src 绑定                   |
| `vstyle`          | 内联样式绑定                    |
| `vstyle-obj`      | 使用对象的 inline style 绑定    |
| `vclass`          | 类绑定                          |
| `vclass-obj`      | 使用对象的类绑定                |
| `vclass-obj-mult` | 多条件类绑定                    |
| `vanim`           | 带 JS 钩子的 Transition 组件   |
| `vnuxtl`          | Nuxt 路由链接                  |
| `vroutename`      | router-link 命名路由           |
| `vroutenameparam` | router-link 带参数的命名路由   |
| `vroutepath`      | router-link 路径路由链接       |
| `vemit-child`     | 从子组件发出事件               |
| `vemit-parent`    | 向父组件发出事件               |

### 脚本相关

| 代码片段           | 用途                                                              |
| ----------------- | ----------------------------------------------------------------- |
| `vdata`           | 组件数据函数                                                      |
| `vmethod`         | Vue 方法                                                          |
| `vcomputed`       | Vue 计算属性                                                      |
| `vwatcher`        | Vue 监听器（带新旧值参数）                                       |
| `vbeforecreate`   | beforeCreate 生命周期方法                                         |
| `vcreated`        | created 生命周期方法                                              |
| `vbeforemount`    | beforeMount 生命周期方法                                          |
| `vmounted`        | mounted 生命周期方法                                              |
| `vbeforeupdate`   | beforeUpdate 生命周期方法                                         |
| `vupdated`        | updated 生命周期方法                                              |
| `vbeforedestroy`  | beforeDestroy 生命周期方法                                        |
| `vdestroyed`      | destroyed 生命周期方法                                            |
| `vprops`          | 带类型和默认值的 props                                           |
| `vimport`         | 导入一个组件到另一个组件中                                        |
| `vimport-dynamic` | 导入一个应该由 webpack 懒加载的组件                               |
| `vcomponents`     | 在 export 语句中导入一个组件到另一个组件中                         |
| `vimport-export`  | 导入一个组件并在 export 语句中使用它                              |
| `vmapstate`       | 从 Vuex 导入 mapState 到 Vue 组件                                |
| `vmapgetters`     | 从 Vuex 导入 mapGetters 到 Vue 组件                              |
| `vmapmutations`   | 从 Vuex 导入 mapMutations 到 Vue 组件                            |
| `vmapactions`     | 从 Vuex 导入 mapActions 到 Vue 组件                               |
| `vfilter`         | Vue 过滤器                                                        |
| `vmixin`          | 创建 Vue Mixin                                                   |
| `vmixin-use`      | 引入 mixin 到组件中使用                                          |
| `vc-direct`       | 创建自定义指令                                                   |
| `vimport-lib`     | 导入库                                                           |
| `vimport-gsap`    | 导入 GreenSock                                                   |
| `vanimhook-js`    | 在方法中使用 Transition 组件的 JS 钩子                           |
| `vcommit`         | 在方法中提交到 Vuex store（mutation）                            |
| `vdispatch`       | 在方法中分发到 Vuex store（action）                             |
| `vtest`           | 简单的单元测试组件                                               |

### Vue Composition API

| 代码片段             | 用途                                               |
| ------------------- | -------------------------------------------------- |
| `v3reactive`        | Vue Composition API - reactive                    |
| `v3reactive-setup`  | Vue Composition API - reactive 带 setup 样板代码  |
| `v3computed`        | Vue Composition API - computed                    |
| `v3watch`           | Vue Composition API - 监听单个源                  |
| `v3watch-array`     | Vue Composition API - 数组形式的 watch           |
| `v3watcheffect`     | Vue Composition API - watchEffect                 |
| `v3ref`             | Vue Ref                                           |
| `v3onmounted`       | 生命周期钩子 - onMounted                          |
| `v3onbeforemount`   | 生命周期钩子 - onBeforeMount                      |
| `v3onbeforeupdate`  | 生命周期钩子 - onBeforeUpdate                     |
| `v3onupdated`       | 生命周期钩子 - onUpdated                          |
| `v3onerrorcaptured` | 生命周期钩子 - onErrorCaptured                    |
| `v3onunmounted`     | 生命周期钩子 - (destroyed) onUnmounted            |
| `v3onbeforeunmount` | 生命周期钩子 - (beforeDestroy) onBeforeUnmount    |
| `v3useinoptions`    | 在 Options API 中使用 Composition API             |

### Vuex

| 代码片段         | 用途                        |
| --------------- | --------------------------- |
| `vstore`        | Vuex store.js 基础模板      |
| `vgetter`       | Vuex Getter                 |
| `vmutation`     | Vuex Mutation               |
| `vaction`       | Vuex Action                 |
| `vmodule`       | Vuex Module                 |
| `vstore-import` | 导入 vuex store 到 main.js  |
| `vstore2`       | 更新的 Vuex store 基础模板  |

### Vue Router

| 代码片段              | 用途                                       |
| -------------------- | ------------------------------------------ |
| `vrouter`            | Vue Router 基础模板                        |
| `vscrollbehavior`    | Vue Router scrollBehavior                  |
| `vbeforeeach`        | Vue Router 全局守卫 beforeEach             |
| `vbeforeresolve`     | Vue Router 全局守卫 beforeResolve          |
| `vaftereach`         | Vue Router 全局守卫 afterEach              |
| `vbeforeenter`       | Vue Router 路由独享守卫 beforeEnter        |
| `vbeforerouteenter`  | Vue Router 组件内守卫 beforeRouteEnter    |
| `vbeforerouteupdate` | Vue Router 组件内守卫 beforeRouteUpdate   |
| `vbeforerouteleave`  | Vue Router 组件内守卫 beforeRouteLeave    |

### Vue 配置

| 代码片段   | 用途                                                              |
| --------- | ------------------------------------------------------------------ |
| `vplugin` | 导入插件到 main.js 或 plugins 文件                                |
| `vconfig` | vue.config.js 文件，示例：将 sass 文件导入到每个组件               |

### Nuxt 配置

| 代码片段 | 用途                                                 |
| ------- | ---------------------------------------------------- |
| `nfont` | 在 nuxt-config 中包含字体的链接                      |
| `ncss`  | 链接到 CSS 资源，如 normalize                        |

### Nuxt 页面

| 代码片段           | 用途                          |
| ----------------- | ----------------------------- |
| `nasyncdata`      | Nuxt asyncData                |
| `nasyncdataaxios` | 使用 Axios 模块的 Nuxt asyncData |
| `nfetch`          | Nuxt Fetch                    |
| `nfetchaxios`     | 使用 Axios 模块的 Nuxt Fetch  |
| `nhead`           | Nuxt Head                     |
| `nparam`          | Nuxt 路由参数                 |

### 额外功能（纯文本）

| 代码片段     | 用途                 |
| ----------- | -------------------- |
| `gitignore` | .gitignore 文件预设 |

## 贡献

这是一个向任何人开放的开源项目。欢迎贡献 [GitHub](https://github.com/sdras/vue-vscode-snippets)

如果您要贡献代码片段，请确保在 README 的表格中添加相应的文档，没有此添加的拉取请求将无法被接受。谢谢！

## 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 作者

Sarah Drasner ([@sarah_edo](https://twitter.com/sarah_edo))

## 支持

如果您在使用过程中遇到问题或有任何建议，请通过以下方式联系：

- 在 [GitHub Issues](https://github.com/sdras/vue-vscode-snippets/issues) 中提交问题
- 通过 Twitter [@sarah_edo](https://twitter.com/sarah_edo) 联系作者

## 版本信息

当前版本：3.2.0

最后更新：2025-09-21