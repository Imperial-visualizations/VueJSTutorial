<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png"/>
    <user-info :nameChangeCallback="userNameChanged" v-model="username"/>
    <dialog-box></dialog-box>
    <footer> User {{username}} is currently logged in </footer>


  </div>
</template>

<script>
import UserInfo from "./components/UserInfo.vue"
import DialogBox from "./components/DialogBox.vue"

export default {
  name: 'App',
  components: {
    "user-info":UserInfo,
    "dialog-box":DialogBox
  },
  data(){
    return {
      username:"Ben",
      fullName:"Ben RW"
    }
  },
  methods:{

  }
}
</script>

<style>
body,html {
  padding:0;
  margin:0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
footer{
  position: absolute;
  border-top: 2px solid #2c3e50;
  background-color:#2c3e50;
  color:white;
  top:95%;
  width:100%;
  height:5%;
  margin:0;
  padding: 15px 0;
  box-sizing: border-box;
}

</style>
