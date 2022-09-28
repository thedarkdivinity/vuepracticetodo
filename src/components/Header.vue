<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <header>
        <h1>{{title}}</h1>
        <ButtonComponent @toggle-add-task="$emit('toggle-add-task')" :text="showAddTask?'Close':'Add Task'" 
        
        :color="showAddTask?'red':'green'"/>
      
    </header>
</template>
<script>
    import ButtonComponent from './ButtonComponent.vue';

    export default{
        name:'HeaderComponent',
        props:{
            title:{
                type: String
                
            },
            showAddTask:{
                type:Boolean
            }
        },
        components:{
    ButtonComponent
}
    }
</script>
<style scoped>
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>