<template>
  <aside class="dev">
    <Transitions></Transitions>
    <Transitions1></Transitions1>
  </aside>
</template>
<script>
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

      _click1(){
        this.visible = !this.visible;
      }
    },
    components: {Transitions,Transitions1}
  };
</script>
<style rel="stylesheet/scss" lang="scss">
  .dev {
    text-align: center;
  }

  .button {
    width: 90%;
    height: 50px;
    line-height: 50px;
    background: #af6430;
    text-align: center;
    border-radius: 5px;
    border: 1px solid #fff;
    margin: 10px auto;
    font-size: 18px;
    color: #fff;
  }


</style>

