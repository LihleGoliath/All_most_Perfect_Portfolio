<template >
 <section id="footer">
    <div class="footer-content">
<div class="logo">
    <H1>L</H1>
   </div>
   <div class="copy-right">
    <p>Copy Right Of 2022</p>
   </div>
   <div class="icon-links">
    <a href="https://www.linkedin.com/in/lihle-goliath-355921244/" target="_black"><i class="fa-brands fa-linkedin"></i></a>
    <a href="https://github.com/LihleGoliath" target="_black"><i class="fa-brands fa-github"></i></a>
    <a href="https://codepen.io/lihlegoliath" target="_black"><i class="fa-brands fa-codepen"></i></a>
    <a href="https://app.netlify.com/teams/lihlegoliath/overview" target="_black"><i class="fa-solid fa-diamond"></i></a>
   </div>
    </div>
   
 </section>
</template>
<script>
export default {
    
}
</script>
<style lang="scss">
section#footer{
    background-color: #231F20;
    width: 100vw;
    text-align: center;
   transition: 0.5s ease all;
      
      .footer-content{
        width: 90vw;
        margin: auto;
        display: flex;
        justify-content: space-evenly;
        flex-wrap: wrap;
        color: gainsboro;
        text-decoration: none;
            transition: 0.5s ease all;


         div{
            padding: 10px;
         }
        
        .logo{
            cursor: pointer;
        }

         .copy-right{
            font-weight: 200;
            color: #fff;
         }

         .icon-links{
           display: flex;
           gap:10px;
           color: #fff;
          a{
            color: #fff;
           i{
            cursor: pointer;
            &:hover{
               color:royalblue;
            }
           }
          }
         }
      }
}
    
</style>