<template>
  <div id="app">
   <!-- <small-user-profile v-for="(user, index) in users" :key="index" :user=> -->
<small-user-profile v-for="(users_obj, index) in users" 
:key="index"
:user="users_obj"
@user_clicked="show_user" 
></small-user-profile>
<!-- <individual-post  -->
    <!-- v-for="(post, index) in posts" -->
    <!-- :key="index" -->
    <!-- :post="post" -->
    <!-- @user_clicked="show_post">testing -->

<!-- </individual-post> -->

   <h3>this is appvue</h3>

   <!-- finally worked to make it show up -->
   <h3>{{users[0][`name`]}}</h3>
   

   
  </div>
</template>

<script>

import SmallUserProfile from '@/components/SmallUserProfile.vue';

export default {
  // this is working now, if argument is set just use
  methods: {
    show_user(user_1) {
      // to access the variable declared below here, need the $data.  user_1 is passing the string
      // from the this.$emit after the event and comma.  which was a string of text
      this.$data.users[0].name = user_1
    }
  },
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
