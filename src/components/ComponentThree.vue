<template>
    <div>
       <ComponentFour/>
       <HistoryComp/>
    </div>
</template>

<script>
 import ComponentFour from './ComponentFour.vue';
 import HistoryComp from './HistoryComp.vue';
   export default{
    name: 'ComponentThree',
    components: {
        ComponentFour,
        HistoryComp,
    }
   }
</script>

<style>

</style>