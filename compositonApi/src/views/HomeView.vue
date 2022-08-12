<template>
  <main>
    <viewShow :count="count"/>
    <viewControler @parentIncrement="increment($event)" />
  </main>
</template>
<script >
import {ref} from "vue";
import viewShow from "../components/viewShow.vue";
import viewControler from "../components/viewControler.vue";
  export default {
    components:{
      viewShow,
      viewControler
    },
    setup (){
      let count=ref(1000);
      const increment=(num)=>{
        count.value+=num;
      }
      return{
        count,
        increment
      }

    }
  }
</script>
<style scoped>
  .difStyle{
    font-size: 18px;
    color: lightgreen;
  }
</style>