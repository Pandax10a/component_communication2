<template>
    <div>
        <button>click me</button>
        <p>name: {{User.name}}</p>
        <p>age: {{User.age}}</p>
        <p>premium: {{User.is_premium}}</p>
        <p>id: {{User.id}}</p>
        
        <!-- <p>this is smallUser</p> -->
        
        

    </div>
</template>

<script>
    export default {
       
        props: {
            User: {          
                name: String,
                age: Number,
                is_premium: Boolean,
                msg: String,
                id: String
        },
         
            },
        
        name: 'small-user-profile'
    }
</script>

<style scoped>

</style>