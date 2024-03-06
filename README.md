<p align="center">
    <a href="http://www.form-create.com">
        <img width="200" src="http://form-create.com/logo.png">
    </a>
</p>

# form-create-designer v3 for ant-design-vue

**这个是 Vue3 版本**

[![MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/xaboy/form-create-designer)
[![github](https://img.shields.io/badge/Author-xaboy-blue.svg)](https://github.com/kissice)

**form-create-designer 是基于 [@form-create/ant-design-vue](https://github.com/xaboy/form-create) vue3版本实现的表单设计器组件。可以通过拖拽的方式快速创建表单，提高开发者对表单的开发效率，节省开发者的时间。**


![demo1](http://form-create.com/img/designer-review.png)
**NodeJs:**

```shell
npm install antv-form-designer
```

请自行导入`Ant-Design-Vue`并挂载

```js
import formCreate from '@form-create/ant-design-vue'
import AceDesigner from 'antv-form-designer'

app.use(formCreate)
app.use(AceDesigner)
```

## 使用

```html
<ace-designer ref="designer"/>
```

## 设置多语言
通过 locale 配置项设置语言

```vue
<template>
  <ace-designer :locale="locale"></ace-designer>
</template>

<script>
import En from "@form-create/designer/locale/en.js";
export default {
  data(){
    return {
        locale: En,
    }
  }
}
</script>
```

## 组件`props`

- **menu**`MenuList` 重新配置拖拽的组件

- **height**`int|string` 设计器组件高度, 默认`100%`

- **locale**`object` 设置多语言

- **config**`Config` 设置多语言

- **mask** `boolean` 设置拖拽表单中的组件是否可以操作

## 组件方法

- 获取当前生成表单的生成规则

    ```ts
    type getRule = () => Rule[]
    ```
  **示例: `this.$refs.designer.getRule()`**

- 获取当前表单的全局配置

    ```ts
    type getOption = () => Object
    ```

- 设置当前生成表单的规则

    ```ts
    type setRule = (rules: Rule[]) => void;
    ```

- 设置当前表单的全局配置

    ```ts
    type setOption = (option: Object) => void;
    ```

- 增加一组拖拽组件

    ```ts
    type addMenu = (menu: Menu) => void;
    ```
- 删除一组拖拽组件

    ```ts
    type removeMenu = (name: string) => void;
    ```

- 批量覆盖插入拖拽组件

    ```ts
    type setMenuItem = (name: string, items: MenuItem[]) => void;
    ```

- 插入一个拖拽组件到分组

    ```ts
    type appendMenuItem = (name:string, item: MenuItem) => void;
    ```

- 删除一个拖拽组件

    ```ts
    type removeMenuItem = (item: string | MenuItem) => void;
    ```

- 新增一个拖拽组件的生成规则

    ```ts
    type addComponent = (item: DragRule) => void;
    ```
> **提示! 内置的三个组件分组`name`分别为: `main`,`aide`,`layout`**

## 联系

##### email : 709896100@qq.com

## License

[MIT](http://opensource.org/licenses/MIT)

Copyright (c) 2024-present aceice
