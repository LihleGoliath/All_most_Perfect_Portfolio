<template >
    <header id=" nav" :class="{ 'scrolled-nav': scrollPosition }">
    <nav>
    <div class="logo"><h1>L</h1></div>
    
   <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <router-link to="/" class="nav-link active link" aria-current="page">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/about" class="link">About</router-link>
        </li>
        <li class="nav-item">
         <router-link to="/resume" class="link">Resume</router-link>
        </li>
           <li class="nav-item">
         <router-link to="/project" class="link">projects</router-link>
        </li>
           <li class="nav-item">
         <router-link to="/testimonials" class="link">Testimonials</router-link>
        </li>
           <li class="nav-item">
         <router-link to="/contact" class="link">Contact</router-link>
        </li>
      </ul>
     <div class="button">
         <i @click="ToggleNav" class="fa-solid fa-bars" :class="{'button-active' : mobileNav}"></i>
     </div>
     <transition name="mobile-nav">
     <ul v-show="mobileNav" class="navbar-nav me-auto mb-2 mb-lg-0 dropdown-nav">
        <li class="nav-item">
          <router-link to="/" class="nav-link active link" aria-current="page">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/about" class="link">About</router-link>
        </li>
        <li class="nav-item">
         <router-link to="/resume" class="link">Resume</router-link>
        </li>
           <li class="nav-item">
         <router-link to="/projects" class="">projects</router-link>
        </li>
           <li class="nav-item">
         <router-link to="/testimonials" ><div class="link">Testimonials</div> </router-link>
        </li>
           <li class="nav-item">
         <router-link to="/contact" >Contact</router-link>
        </li>
      </ul>
     </transition>
    </nav>
    </header>
</template>
<script>
export default {
    
}
</script>
<style lang="scss" scoped>

header{
    position: fixed;
    background-color:#231F20;
    z-index:100;
    width: 100vw;
    transition: 0.5s ease all;
    color:gainsboro;

    nav{
        display: flex;
        justify-content:space-between ;
        padding:10px 0;
        transition: 0.5s ease all;
        width: 90vw;
        margin: auto;
        
         .logo{
          width: fit-content;
          cursor: pointer;
         }
        ul,.link{
          list-style: none;
          font-weight: 200;
          color: #fff;
          text-decoration: none;
          display: flex;
          cursor: pointer;
        }

        li{
         text-transform:uppercase;
         padding: 10px;
        }

        .link{
          font-size: 10px;
        }
    }

}
  
</style>