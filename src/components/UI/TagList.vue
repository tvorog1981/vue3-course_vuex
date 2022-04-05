<template>
<div class="tags">
<div v-for="(link, index) in tagsItems" :key="index">
    <router-link class="link__tag" :to="link">{{link}}</router-link>
 
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