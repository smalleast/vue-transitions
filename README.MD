#vue-transitions
> transitions for vue.


## usage:
+ install:
```bash
npm install smalleast/vue-transitions --save


```



+template
```
<template>
  <aside class="dev">
    <Transitions></Transitions>
    <Transitions1></Transitions1>
  </aside>
</template>
```
+script
```
import Transitions from '../components/transitions.vue'
  import Transitions1 from '../components/transitions-1.vue'
  export default {
    data() {
      return {
        visible: false
      };
    },
    props: {},
    created(){
    },
    methods: {

    },
    components: {Transitions,Transitions1}
  };
```

## resource:
+ http://www.cnblogs.com/Kummy/p/4966937.html
+ https://github.com/steven5538/vue-button
+ https://yarnpkg.com/en/docs/install
