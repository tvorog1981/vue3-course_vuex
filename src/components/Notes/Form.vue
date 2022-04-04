<template>
    <form @submit.prevent="onSubmit" class="note-form">
        <textarea type="text" required v-model="value"  placeholder="Type ur note"/>
        <button type="submit" class="btn btnPrimary btn-size">Add new note</button>
       
    </form>
</template>

<script>

export default{

 data(){
     return{
         value:''
     }
 },
 methods:{
     onSubmit(){
         this.$emit('onSubmit', this.value)
         this.value = ""
        
     }
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