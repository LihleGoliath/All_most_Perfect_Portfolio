<template>
<section id="resume">
  <div class="resume">
    <div class="resume-img">
      <img :src="img" alt="">
    </div>
    <div class="resume-text">
  
      <div class="container"> 
        <div class="contain">
            <p>This resume includes Work Experience{ No Work Experience} and Educational Journey </p>
        </div>
            <div v-for="resume in resumes" :key="resume.date" class="schools">
                <div class="Grade11 Grade12 Coding-Course">
                   <h1>{{resume.date}}</h1> 
                  <div class="container">                        
                            <P><strong>{{resume.title}}</strong> {{resume.text}}</P>                      
                            <p class="school"> {{resume.location}}</p>
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
      img:'https://i.postimg.cc/zGBsVgSN/IMG-20211019-WA0014-auto-x2.jpg',
      resumes:[
    {
        date:"2020",
        title:"Grade11 in Bloemfontein :",
        text:"I was a capable high school student that was average in doing the following subject: Mathematics ,English ,Afrikaans, Life Orientation, Geography, Physical Science, Life Science",
        location:"School was Head Start High School",
        imgURL:"https://i.postimg.cc/3rqrykTV/Screenshot-2022-05-31-120530.png"
    },
    {
        date:"2021",
        title:"Grade 12 certification  in  Cape Town :",
        text:"Another factors at play forced me to change schools and place of residence . At this new school  I had to also change my subjects and  they are as follow :Maths Lit ,  English, Afrikaans, Life Orientation, Religious Studies, Tourism, History",
         location:"School was City Mission Educational Services in Bridgetown,Cape Town",
        imgURL:"https://i.postimg.cc/0yV9sjcV/CMES.jpg"
    },
    {
        date:"2022",
        title:"Coding course :",
        text:" I'm still in the process of completing the course  but the skills that I have taken are fully drilled in the mind ",
         location:"The academy is Life Choices academy in Lansdowne,Cape Town",
        imgURL:"https://i.postimg.cc/CLJ3Ztk1/download.png"
    }
    ]
    }
  }
}
</script>

<style lang="scss">
section#resume{
background-color:#000 ;
height:95%;
width: 100vw;
@media (max-width:1200px) {
  height:fit-content;
  
}

.resume{
  width: 100%;
  height: 100%;
  padding: 20px;
  padding-left:0 ;
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

   .resume-img{
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
    }
   }
   .resume-text{
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
      max-height: fit-content;
      
    }
   
   &::before{
    position: absolute;
    content: 'Resume';
    font-size: 6vw;
    left: 2px;
    top:10px;
    opacity: 0.7;
   }

   .container{
    margin-top: 20px;

    .contain{
        border: 1px solid #fff;
        margin: 10px;
        padding: 20px;
        font-size: 1rem;
    }
    .schools{
        width: 80%;
        margin: auto;
        margin-top:30px;
        padding: 20px;
        background-color:#fff;
        border-radius: 20px;
       
      .Grade11{
        border:1px solid #fff;
        background-color: #000;
        padding: 10px;
        .container{
            background-color: gainsboro;
            color: #000;
            padding: 5px;
            border-radius:10px ;
        }
      }
      .Grade12{
        border:1px solid #fff;
        background-color: #000;
        padding: 10px;
        .container{
            background-color: gainsboro;
            color: #000;
            padding: 5px;
            border-radius:10px ;
        }
      }
      .Coding-Course{
        border:1px solid #fff;
        background-color: #000;
        padding: 10px;
        .container{
            background-color: gainsboro;
            color: #000;
            padding: 5px;
            border-radius:10px ;
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
        border-radius:20px ;
      }
          @media only screen and(max-width:1200px) {
       ::-webkit-scrollbar{
      width:0;
    }
     } 
</style>
