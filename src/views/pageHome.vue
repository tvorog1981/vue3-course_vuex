<template>
  <div>
    <Form @onSubmit="Submit"></Form>
    <List :items="notes" @removeItem="handlerItem"></List>
  </div>
</template>


<script>
import Form from '@/components/Notes/Form.vue'
import List from '@/components/Notes/List.vue'
export default{
components:{
  Form:Form,
  List:List
},
methods:{
  Submit(event){
   this.notes.push(event)
  },
  handlerItem(index){
    

  this.notes.splice(index, 1)
  
 
} 
},
 data(){
    return{
      notes: ['note 1', 'note 2', 'note 3']
    }
  }

}
</script>
