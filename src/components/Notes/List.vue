<template>
<div class="item" v-for="(item ,index) in items" :key="index">{{item}} <p style="cursor:pointer;" @click="$emit('removeItem',index)">&#10005;</p></div>

</template>





<script>
export default{
    name: 'List',
    props:{
        items:{
            type: Array,
            default:[]
        }
    }
}
</script>
<style scoped>
  .item{
      display:flex;
      justify-content: space-around;
      border: 1px solid black;
      border-radius: 5px;
      padding: 40px;
      margin-bottom: 5px;
            
  }
</style>