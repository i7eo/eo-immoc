#### vue3 概览

1. slot api
```html
<div v-slot:one="{ msg }">
  {{ msg }}
</div>
```

v-slot 默认插槽
v-slot:one 名称为one的具名插槽
v-slot:one="{ msg }" 值为msg的作用域插槽
v-slot => #

作用域插槽使用时注意：
删除了 this.$scopedSlots 全部使用 this.$slot 获取值

2. 全局api规范

`this.$nextTick(() => {})`

=>

`import { nextTick, h } from 'vue'`

`nextTick(() => {})`

好处是为了 tree-shaking

3. teleport api
之前写组件必须挂在 #app 中，但是modal这种就没必要挂在这个下面，挂在这个下面有时样式会被影响，所以可以使用 teleport

`<teleport to="#endofbody">111</teleport>`

4. composition api

5. v-model 指令
