<template>
<div class="tags">
<div v-for="link in tagsItems" :key="link">
    <p class="btn btnPrimary" v-on:click="$emit('handlerTag', link)">{{link}}</p>
 
    </div>  
</div>
</template>





<script>
export default{
    name:'TagList',
    props:{
        tagsItems:{
            type:Array,
            default:[]
        }
    },
    methods:{
        
    }

}
</script>
<style scoped>
.tags{
    display:flex;
    margin: 40px;
    align-items: center;
   
}
.link__tag{
    margin-right: 10px;
}
</style>