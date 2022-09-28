<template>
    <button @click="onClick()" :style="{background: color}" class="btn">{{text}}</button>
</template>
<script> 
export default{
    name:'ButtonComponent',
    props:{
        color:{
            type:String,
            default:'green'
        },
        text:{
            type:String
        }
    },
    methods:{
        onClick(){
            this.$emit('toggle-add-task')
        }
    }
}
</script> 