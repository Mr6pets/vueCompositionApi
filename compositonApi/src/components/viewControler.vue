<template>
  <button @click="increment(1)">+</button>
  <button @click="increment(-1)">-</button>
</template>

<script>
export default {
  name: "viewControler",
  setup(props,conte){
    let increment=(num)=>{
      //注册事件 调用父亲节点
      conte.emit('parentIncrement',num)
    }
    return {
      increment
    }
  }
}
</script>

<style scoped>

</style>