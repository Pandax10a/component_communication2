<template>
  <div id="app">
   <!-- <small-user-profile v-for="(user, index) in users" :key="index" :user=> -->
<small-user-profile v-for="(users_obj, index) in users" :key="index"
:user="users_obj"></small-user-profile>

   <h3>this is appvue</h3>

   <!-- finally worked to make it show up -->
   <h3>{{users[0][`name`]}}</h3>
   

   
  </div>
</template>

<script>

import SmallUserProfile from '@/components/SmallUserProfile.vue';

export default {
  components: { 
    SmallUserProfile
    } 
    ,
    data() {
      return {
        users: [{
          name: `alpha`,
          age: `4`,
          is_premium: true,
          id: `00` +7
        },
        {
          name: `gamma`,
          age: `11`,
          is_premium: false,
          id: `00` +8
        },
        {
          name: `alpha`,
          age: `18`,
          is_premium: false,
          id: `00` +9
        },
      ]
    }
    },
  name: 'App',
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
