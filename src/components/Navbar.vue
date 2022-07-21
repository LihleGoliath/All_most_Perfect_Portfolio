<template >
    <header id=" nav" >
    <nav>
    <div class="logo"><h1>L</h1></div>
    
   <ul  v-show="!mobile" class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <router-link to="/" class="link"  :class="{active}">Home</router-link>
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
     <div class="btn">
      <button v-show="mobile" @click="ToggleNav" :class="{'active' : mobileNav}">
      <span class="num1"></span>
      <span class="num2"></span>
      <span class="num3"></span>
      </button>
         <!-- <i v-show="mobile" @click="ToggleNav" class="fa-solid fa-bars" :class="{'button-active' : mobileNav}"></i> -->
     </div>
     <transition name="mobile-nav" class=" dropdown">
        
       <ul v-show="mobileNav" >
        <li class="nav-item">
          <router-link to="/" class="link" >Home</router-link>
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
     </transition>
    </nav>
    </header>
</template>
<script>
export default {
  data(){
    return{
      
      mobile:true,
      mobileNav:false,
      windowWidth:null

    }
  },
  created(){
    window.addEventListener('resize',this.ScreenChecker);
    this.ScreenChecker()
  },
  methods:{
    ToggleNav(){
      this.mobileNav = !this.mobileNav
    },
 
     ScreenChecker(){
      this.windowWidth = window.innerWidth
      if(this.windowWidth <= 750){
        this.mobile = true;
        return;
      }else{
        this.mobile = false;
        this.mobileNav  = false;
        return;
      }
    }
  }
  
    
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

          &:hover{
            background-color: rgba(55, 55, 199, 0.94);
            border: 1px solid #fff;
          }
        }
        .active{
          border-bottom: 2px solid rgba(55, 55, 199, 0.94);
          color:rgba(55, 55, 199, 0.94);
        }
        .btn{
          
          button{
            background:none;
           color: #fff;
           border: none;

                  span{
                    display: block;
              width: 20px;
              height: 3px;
              background-color: #fff;
              margin: 3px;
              border-radius:2px ;
              
              .num3.active{
                display: none;
              }
                
            }
          }
        }

        .dropdown{
          background-color: #231F20;
         position: fixed;
         justify-content: center;
         flex-direction: column;
         left: 0;
         height: 100%;
         width: 100%;
         max-width: fit-content;
         transition: 0,8s ease all;

        }
        .mobile-nav-enter-active,
        .mobile-nav-leave-active{
          transition: 1s ease all;
        }
        .mobile-nav-enter-from,
        .mobile-nav-leave-to{
          transform:translateX(-250px) ;
        }
        .mobile-nav-enter-to{
          transform: translateX(0);
        }
    }

}
  
  button.active{                      
                  .num1{
                   transform: rotate(-45deg);
                      margin-bottom:-2px ;
                  }
                  .num2{
                    transform: rotate(45deg);
                    margin-top:-3px ;
                  }
                   .num3{
                     display: none;
                   }
               
                }
          
        
   </style>      