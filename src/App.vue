<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
import Vue from 'vue'
export default {
  name: 'App',
  mounted(){
    this.$axios({
      // Headers:{
      //   'Content-Type':"application/json;charset=utf-8",
      // },
      method:'get',
      url:'/api/users'
    }).then((response) => {
      console.log(response.data)
    }).catch((response)=>{
      console.log(response.data);
    })
  }
}
</script>