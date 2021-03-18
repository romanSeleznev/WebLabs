<template>
    <div>
        <h1>Your data</h1>
        <p>FirstName: {{Person.FirstName}}</p>
        <p>LastName: {{Person.LastName}}</p>
        <p>Mail: {{Person.Mail}}</p>
        <p>Password: {{Person.Password}}</p>
    </div>
</template>

<script>
export default {
    name: 'Step3',
    props:['Person'],
    data: function(){
        
    }
}
</script>

<style scoped>
</style>