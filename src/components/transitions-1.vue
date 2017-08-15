<template>
  <div class="app">
    <button @click="showball" class="btn">show</button>
    <transition name="move" type="animation">
      <div class="ball" v-show="show">
        <div class="inner"></div>
      </div>
    </transition>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    data () {
      return {
        show: false
      };
    },
    methods: {
      showball () {
            this.show = !this.show;
      }
    }
  };
</script>

<style lang="scss" rel="stylesheet/scss">
  @keyframes shape-change {
    0%, 100% {
      //border-radius: 50%;
      background: red;
    }
    50% {
      //border-radius: 0;
      background: blue;
    }
  }

  @keyframes moveball-in {
    0% {
      transform: translate3d(300px, -10px, 0);
    }
    10% {
      transform: translate3d(270px, -20px, 0);
    }
    20% {
      transform: translate3d(240px, -30px, 0);
    }
    30% {
      transform: translate3d(210px, -40px, 0);
    }
    40% {
      transform: translate3d(180px, -50px, 0);
    }
    50% {
      transform: translate3d(150px, -50px, 0);
    }
    60% {
      transform: translate3d(120px, -50px, 0);
    }
    70% {
      transform: translate3d(90px, -40px, 0);
    }
    80% {
      transform: translate3d(60px, -30px, 0);
    }
    90% {
      transform: translate3d(30px, -20px, 0);
    }
    100% {
      transform: translate3d(0, -10px, 0);
    }
  }

  @keyframes moveball-out {
    0% {
      transform: translate3d(0, -10px, 0);
    }
    10% {
      transform: translate3d(30px, -20px, 0);
    }
    20% {
      transform: translate3d(60px, -30px, 0);
    }
    30% {
      transform: translate3d(90px, -40px, 0);
    }
    40% {
      transform: translate3d(120px, -50px, 0);
    }
    50% {
      transform: translate3d(150px, -50px, 0);
    }
    60% {
      transform: translate3d(180px, -50px, 0);
    }
    70% {
      transform: translate3d(210px, -40px, 0);
    }
    80% {
      transform: translate3d(240px, -30px, 0);
    }
    90% {
      transform: translate3d(270px, -20px, 0);
    }
    100% {
      transform: translate3d(300px, -10px, 0);
    }
  }

  .app {
    .btn {
      width: 40px;
      height: 30px;
      margin-top: 40px;
      border: none;
      outline: none;
      background: red;
      color: #fff;
    }
    .ball {
      position: absolute;
      bottom: 20px;
      left: 20px;
      width: 50px;
      height: 50px;
      transition: all 1s cubic-bezier(.25, .1, .25, .1);
      &.move-enter-active {
        opacity: 1;
        animation: moveball-in 0.3s;
        .inner {
          animation: shape-change 1s;
        }
      }
      &.move-leave-active {
        opacity: 0.8;
          animation: moveball-out 0.3s;
        .inner {
          animation: shape-change 1s;
        }
      }
      .inner {
        display: inline-block;
        width: 30px;
        height: 30px;
        border-radius: 50%;
        background: red;
        transition: all 1s linear;
      }
    }
  }
</style>
