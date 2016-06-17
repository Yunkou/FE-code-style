# Vue-Style-Guide

### 1 Vue属性书写顺序

```javascript
export default {
  mixins,
  data,
  props,
  store，
  computed，
  route,
  created，
  ready，    // => 生命周期顺序不赘述
  methods,
  event,
  watch,
  components
}
```



### 2 组件

#### 2.1 命名

组件以驼峰命名

```html
<template>
  <my-components></my-components>
</template>
<script>
  import myComponents from './myComponents.vue'
    
  export default {
  components: {
  	  myComponents
    }
  }
</script>

```

#### 2.2 组件引用

```javascript
  import myComponentsA from './myComponentsA.vue'  
  import myComponentsB from './myComponentsB.vue'
  import myComponentsC from './myComponentsC.vue'
  import myComponentsD from './myComponentsD.vue'
  export default {
    components: {
  	  myComponentsA,
      myComponentsB,
      myComponentsC,
      myComponentsD,
    }
  }
```

### 3 事件

```html
<!-- bad -->
<a v-on:click="pass()">pass</a>

<!-- good -->
<a @click="pass">pass</a>
  
```
