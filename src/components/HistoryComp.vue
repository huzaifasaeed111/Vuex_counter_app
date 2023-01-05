<template>
   <div class="container">
     <h4>History</h4>
     <div class="flex">
          <p v-for="(number,index) in history" :key="index"
            :class="activeIndexes(value).includes(index) && 'bold'"
          >
             {{number}}
          </p>
     </div>
     <div>
        {{activeIndexes(value)}}
        <input type="number" placeholder="Search by Index" v-model="value">
     </div>
   </div>
</template>

<script>
  import {mapState,mapGetters} from "vuex"
  export default{
     name: 'HistoryComp',
     data(){
       return{
        value: 0
       }
     },
     computed:{
        ...mapState(["history"]),
        ...mapGetters(["activeIndexes"])
     }
  }
</script>

<style>
  .container{
     margin-top: 3rem;
  }
  .flex{
    display: flex;
    text-align: center;
    width: 25rem;
    margin: 0 auto;
    justify-content: center;
    flex-wrap: wrap;
  }
  .flex p{
    margin: 1rem;
  }
  .bold{
    font-weight: 1000;
  }
</style>