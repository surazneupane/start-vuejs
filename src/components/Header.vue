<template>
    <header>
        <h1> {{ title }} </h1>
        <Button @btn-click ="$emit('toggle-add-task')" :text="isFormShown ? 'Close':'Add Task'" :color ="isFormShown ? 'red':'green'"/>
        <!-- <Button text="Update Task" color = "blue"/> -->
        <!-- <Button text="Delete Task" color = "red"/> -->
  
    </header>
</template>

<script>
import Button from './Button'

export default{
    name: 'Header',
    props: {
        title:String,
        isFormShown:Boolean,
    }, 
    components:{
        Button,
    },
}
</script>

// Scoped only for this component

<style scoped>

header{
    display:  flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}


</style>