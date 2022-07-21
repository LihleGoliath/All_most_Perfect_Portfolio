<template>
<section id="about">
  <div class="about">
    <div class="about-img">
      <img :src="img" alt="">
    </div>
    <div class="about-text">
 <div class="row">    
    <div class="col">
        <h3> I'm  Lihle GOLIATH</h3>
        <P class="lead">My inspiration for  being a developer is from the evolution of the world. That's heading online</P>
        <p class="lead">A positive and enthusiastic person can be said about myself . Having a great appreciation for networking and relationships
            .These are proven to be advantageous in the ways of success. Focused  and driven towards life , know how to work in a team and also very independent at times  </p>
            <p class="lead"> I'm going to start with my personality : a leader type ,strategist and problem solver. Good at interacting with people and have a strong character.My passion towards the tech was based on how curious I was how the world is changing for better so I have to better myself.  </p>
             <div class="row">
                 <div class="col-md-6"> 
                     <ul>
                         <li>Birthday:22 May 2003   
                         </li>
                         <li>Age:19years</li>
                         <li>Residence:Gugulethu,Cape Town</li>
                         <li>Province: Western Cape,SA</li>
                     </ul>
                 </div>
                 <div class="col-md-6">
                    <ul>
                        <li>E-mail:lihlegoliath2@gmail.com 
                        </li>
                        <li>Phone:072 366 7902</li>
                        <li>Willing To Relocate:Yes</li>
                       <li> Gender:Male</li>
                    </ul>
                 </div>
             </div>
            <a href="../assets/Lihle Goliath_CV.pdf" download>
                 <button type="button" class="btn">Download CV</button>
             </a>
    </div>
  
</div>
<div class="skills">
     
            <p  class="pb-4">Technical Skills </p>
            <div class="row  ">
                <div class="col-md-4 text-center">
                    <div class="block">
                        <i class="fa-brands fa-html5 fs-1"></i>
                        <span>Html</span>
                    </div>
                </div>
                <div class="col-md-4  text-center">
                    <div class="block">
                        <i class="fa-brands fa-css3 fs-1 "></i>
                        <span>CSS</span>
                    </div>
                </div>
                <div class="col-md-4  text-center">
                    <div class="block">
                        <i class="fa-brands fa-bootstrap fs-1"></i>
                        <span>Bootstrap</span>
                    </div>
                </div>
                   <div class="col-md-4  text-center">
                    <div class="block">
                        <i class="bi bi-filetype-sql"></i>
                        <span>MySQL</span>
                    </div>
                </div>
                   <div class="col-md-4  text-center">
                    <div class="block">
                        <i class="fa-brands fa-js"></i>
                        <span>JavaScript</span>
                    </div>
                </div>
                   <div class="col-md-4  text-center">
                    <div class="block">
                        <i class="fa-brands fa-vuejs"></i>
                        <span>Vue.js</span>
                    </div>
                </div>
            </div>
            <p>Soft Skills</p>
            <div class="row">
                <div class="col-md-4  text-center">
                    <div class="block">
                        <i class="fa-solid fa-comment fs-1"></i>
                        <span>Communication</span>
                    </div>
                </div>
                <div class="col-md-4  text-center">
                    <div class="block">
                        <i class="fa-solid fa-lightbulb fs-1"></i>
                        <span>Thinker</span>
                    </div>
                </div>
                <div class="col-md-4  text-center ">
                    <div class="block">
                        <i class="fa-solid fa-people-group fs-1"></i>
                        <span>Teamwork</span>
                    </div>
                </div>
            </div>
        </div>
</div>
  </div>
</section>
</template>
<script>
export default{
  data(){
    return{
      img:'https://i.postimg.cc/P5g6sQm3/Copy-of-Lihle-2-min.jpg'
    }
  }
}
</script>

<style lang="scss">
section#about{
background-color:#000 ;
height:95%;
width: 100vw;
padding-top:20px;
@media (max-width:1200px) {
  height:fit-content;
  
}


.about{
  width: 100%;
  height: 100%;
  padding: 10px 20px;
  margin: auto;
  display: flex;
  flex-direction: row-reverse;
  justify-content: space-evenly;
  @media(max-width: 1200px){
    flex-direction: column;
    width: fit-content;
    max-width: 100vw;
    overflow-y: scroll;
    overflow-x: hidden;
    
  }
   .about-img{
    width: 50vw;
    height: 100%;
    object-fit: cover;
    @media(max-width: 1200px) {
      width: 100vw;
      height: fit-content;
      object-position: center;
      object-fit: contain;
      padding: 10px;
    }
    img{
      width: 100%;
      height: 100%;
      flex-grow: -1;
      border-radius:50% ;
    }
   }
   .about-text{
    position: relative;
     width: 50vw;
    height: 100%;
    max-height: 95vw;
    color: white;
    font-weight: 200;
    overflow-y: scroll;
    padding: 15px;
    padding-top: 6vw;
    @media (max-width:1200px) {
      width: 100vw;
      height: fit-content;
      overflow-y: hidden;
      overflow-x: hidden;
      max-height: fit-content;
      
    }
    
    &::before{
      position: absolute;
          content: "About Me";
          font-size:5vw;
          opacity:0.7;
          visibility: visible;
          top:2%;
          left: 0;
          color: #fff;
    }

     .row{
      width: fit-content;
      height: fit-content;
      display: flex;
      flex-wrap: wrap;
      gap:20px;
      padding: 20px;
      text-align: start; 
      @media(max-width: 1200px){
        display: block;
        
      }

      h3{
        margin: 10px;
        font-weight: 500;
        font-size: 2vw;
        text-align: center;
        text-decoration: underline;
        @media(max-width:1200px){
          font-size: 20px;
        }
      }
      .lead{
        margin: 10px;
        margin-bottom: 20px;
      }
       .row{
        margin: 5px;
        display: flex;
        gap: 20px;
        
        .col-md-6{
         


         ul{
          list-style: circle;
          display: flex;
          flex-direction: column;
           margin-left: 10px;
          li{
            margin: 2px;
          }
         }
        }
       }
       .btn{
        margin: auto;
        padding: 7px;
        background-color: #000;
        color: #fff;
        font-size:1rem;
        font-weight: 600;
        border-radius: 20px;
        border: 1px solid #fff;
        
        &:hover{
          background-color: #fff;
          color: #000;
          transition: 0.5s ease all;
        }
       }
     }
     .skills{
      position: relative;
      width: 100%;
      

      &::before{
        position: absolute;
        content:'Skills';
        font-size: 5vw;
        opacity: 0.7;
        left: 0;
      }
       
       p{
        padding-top: 70px;
        text-decoration: underline;
       }
       .row{
        display: flex;
        flex-wrap: wrap;
        
        .text-center{
          border: 1px solid #fff;
          padding:20px;
          display:flex;
          gap:10px;

          &:hover{
            background-color: #fff;
            color: #000;
            transition: 0.5s ease all;
          }

          .block{
            display: flex;
            gap:5px;
          }
        }
       }
     }
   }
}

}
 ::-webkit-scrollbar{
      width: 1rem;
    
     
    }
    ::-webkit-scrollbar-track{
    background:rgb(53, 53, 54);
     
      }
      ::-webkit-scrollbar-thumb{
        background: gainsboro;
        height: 10px;
       }
     @media only screen and(max-width:1200px) {
       ::-webkit-scrollbar{
      width:0;
    }
     }
</style>
