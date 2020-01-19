<template>
<!--  测试 .sync  -->
  <div class="app">
    {{parentNum.name}}--{{myName}}
    <div class="child-wrapper">
      <Child :objTest="parentNum" :normalTest.sync="myName"></Child>
    </div>
  </div>
</template>

<script>
import Child from './Child.vue'
export default {
  components:{
    Child
  },
  data(){
    return{
      parentNum:{
        name:'fpx'
      },
      myName:'fpc'
    }
  }
}
</script>

<style>
  .app{
    border: 1px solid red;
    width: 200px;
    height: 200px;
  }
</style>