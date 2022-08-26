<template>
    <div>
        <button @click="click_me">click me</button>

        <p>name: {{User.name}}</p>
        <p>age: {{User.age}}</p>
        <p>premium: {{User.is_premium}}</p>
        <p>id: {{User.id}}</p>
        
        <!-- <p>this is smallUser</p> -->
        
        

    </div>
</template>

<script>
    export default {
        methods: {
            click_me() {
                // console.warn(`see me`);   the `passing from child to parent` will be passed through using user_1 in parent
                this.$emit('user_clicked', `passing from child to parent`)
                
            }
        },
       
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