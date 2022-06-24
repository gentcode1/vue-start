<script>
import Home from "./components/Home.vue"
export default {
 name: "App",
 components:{
   Home
 }}
</script>

 
<template id='App'>
<Home />
</template>
  

<style>
@import './assets/base.css';

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

button{
  font-weight: bold;
}
</style>
