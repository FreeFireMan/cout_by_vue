<template>
  <div id="app">
<!--    <img alt="Vue logo" src="./assets/logo.png">-->
    <HelloWorld :msg="count" />
    <Buttons
            @add="handlerAdd"
            @reset="handlerReset"
            @set-off="handlerSetOff"
            @input-msg="handlerMsg"
    />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Buttons from './components/Buttons.vue'

export default {
  name: 'App',
    data: function () {
        return{
            count: 0
        }
    },
    methods:{
        handlerAdd: function (e) {
            console.log('handlerAdd',e);
            this.count += e;
        },
        handlerReset: function () {
            console.log('handlerReset');
            this.count = 0;
        },
        handlerSetOff: function (e) {
            console.log('handlerSetOff',e);
            if (this.count - e >= 0)
            {
                this.count -= e;
            }
        },
        handlerMsg: function (msg) {
            if(typeof(+msg) === 'number') {
                this.count += +msg
            }
        }
    },
  components: {
    HelloWorld,
      Buttons
  }
}
</script>

<style>
/*#app {*/
/*  font-family: Avenir, Helvetica, Arial, sans-serif;*/
/*  -webkit-font-smoothing: antialiased;*/
/*  -moz-osx-font-smoothing: grayscale;*/
/*  text-align: center;*/
/*  color: #2c3e50;*/
/*  margin-top: 60px;*/
/*}*/
</style>
