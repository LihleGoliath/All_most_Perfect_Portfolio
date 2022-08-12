<template>
 <section id="landing">
  
 
 <div class="img">
    <div class="logo">
        <h1>L</h1>
        <P>Lihle Goliath Aspiring Full Stack Developer</P>
        <router-link to="/about"><button @click="MoveToAbout" class="btn">More...</button></router-link>
    </div>
 </div>


 </section>
</template>
<script>
export default {
    
    
}
</script>
<style lang="scss">
   section#landing{
    position: relative;
     width: 100vw;
     height: fit-content;
     padding: 6vh;

     background-color: #000;
     display: flex;
        justify-content: center;
        align-items: center;

     .img{
        background:url('../assets/circle-g92d8d4cc6_1920.jpg');
        background-position:center;
        background-size: cover;
        width: 80vw;
        height: 80vh;
        display: flex;
        justify-content: center;
        align-items: center;
            
         }
         .logo{
            display: flex;
            flex-direction:column;
            color: gainsboro;
        

            h1{
                font-size:10vw;
                width: 100%;
                max-width:fit-content;
                margin: auto;
                height: 100%;
                max-height: fit-content;
             
            }
            p{
              color:#fff;
             
              font-size: 3vw;
              font-weight: 200;
              margin-bottom: 10px;
            &:hover{
               background-color:royalblue;
            }
            }
            
            .btn{
                margin: auto;
                width: fit-content;
                padding: 5px;
                background: none;
                color: #fff;
                border:2px solid #fff;
                border-radius: 10px;
                cursor: pointer;
            }
         }
     }

   
</style>