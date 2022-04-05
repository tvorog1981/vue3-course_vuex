<template>
<div>
  
    <form @submit.prevent="onSubmit" class="note-form">
        <textarea type="text" required v-model="value"  placeholder="Type ur note"/>
     <TheTag :tagsItems="tagsList" />
        <button type="submit" class="btn btnPrimary btn-size">Add new note</button>
       
    </form>
       
</div>
 
</template>

<script>
import TagsList from '../UI/TagList.vue'
export default{

 data(){
     return{
         value:'',
         tagsList:['home', 'work','travel']
     }
 },
 methods:{
     onSubmit(){
         this.$emit('onSubmit', this.value)
         this.value = ""
        
     }
 },
 components:{
     TheTag:TagsList
 }


}
</script>
<style scoped>
.note-form{
    display: flex;
    flex-direction: column;
    width: 600px;
    align-content: center;
}
.btn-size{
    width: 450px;
    margin: 0 auto;
}
</style>