<template>
    <div>
       <CounterComp/>
    </div>
</template>

<script>
 import CounterComp from './CounterComp.vue';
   export default{
    name: 'ComponentFour',
    components:{
      CounterComp,
    }
   }
</script>

<style>

</style>