<template>
  <div class="child">
    <input type="text" name="fname" v-model="objTest.name">
    <input type="text" name="pname" v-model="normalTest">
    <button @click="change">改变</button>
  </div>
</template>

<script>
export default {
  props: ['objTest','normalTest'],
  data() {
    return {
      fname: 'fpc'
    }
  },
  methods: {
    change(){
      this.$emit('update:normalTest',this.normalTest)
    }
  },
}
</script>

<style lang="css">
  .child{
    height: 100px;
    border: 1px solid red;
  }
</style>