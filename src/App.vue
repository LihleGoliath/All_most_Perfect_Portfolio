<template >
<Navbar/>

  <router-view></router-view>

  <Footer/>
</template>
<script>
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";

export default{
  components:{
    Navbar,
    Footer
  }
}
</script>
<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Lora&family=Poppins&display=swap');
#app {
  position: fixed;
  width: 100%;
  max-width: 100vw;
  height: 100%;
  max-height: 100vw;
 font-family: 'Lora', serif;
font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  overflow-x: hidden;
  overflow-y:hidden;
 @media(max-width:1200px) {
  position: static;
  width: fit-content;
  max-width: max-content;
  height: fit-content;
  max-height: max-content;

 }
 html{
  background-color: black;
 }

}
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  --animate-delay: 2s;
}

@media only screen and (max-width: 1200px) {
  ::-webkit-scrollbar{
    width: 0;
  }
}
</style>
