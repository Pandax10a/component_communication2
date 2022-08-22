<template>
  <div id="app">
   <small-user-profile></small-user-profile>
  </div>
</template>

<script>

import SmallUserProfile from '@/components/SmallUserProfile.vue';

export default {
  components: { 
    SmallUserProfile 
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
