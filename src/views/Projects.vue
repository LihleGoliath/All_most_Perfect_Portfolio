<template>
<section id="Projects">
  <div  class="Projects">
    <div v-for="(project,index) in projects" :key="index"  class="Projects-img" :class="{active:active === index}">
      <img :src="project.imgURL" alt="">
      <h1>{{project.title}}</h1>
      <a :href="project.github"><button>Github</button></a>  <a :href="project.live"><button>Live</button> </a>
      <P>Techstack: {{project.techStack}}</P>
    </div>
    <div class="Projects-text">
    <div  v-for="(project,index) in projects" :key="index"  class="project-card" >
    <div class="project-img">
     <img :src="project.imgURL" alt=""/>
    </div>
      <h3>{{project.title}}</h3>
    <button @click="On(index)">Full View</button>
      
    </div>
      </div>
  </div>

</section>
</template>
<script>

export default{
  data(){
    return{
      projects:[
    {
    title:"Font Gallery",
    imgURL:"https://i.postimg.cc/SQdTV9s1/font-gallery.png",
    github:"link",
    live:"link",
    techStack:"Html,CSS"
    },
    {
     title:"Calculator",
     imgURL:"https://i.postimg.cc/G3XKv17Z/Screenshot-2022-04-22-101154.png",
     github:"link",
     live:"link",
    techStack:"Html,CSS"
    },
    {
      title:"Restaurantly",
      imgURL:"https://i.postimg.cc/LXK9y7yS/Screenshot-2022-05-31-115944.png",
      github:"link",
      live:"link",
    techStack:"Html,CSS,Bootstrap"
    },
    {
      title:"BMI Calculator",
      imgURL:"https://i.postimg.cc/ZRRwwgZ2/BMI-calculator.png",
      github:"link",
      live:"link",
    techStack:"Html,CSS,JavaScript"
    },
    {
      title:"Temp Calculator",
      imgURL:"https://i.postimg.cc/mD80DC2f/TEMP-calculator.png",
      github:"link",
      live:"link",
    techStack:"Html,CSS,Javascript"
    },
    {
      title:"Properties",
      imgURL:"https://i.postimg.cc/ht4M4j3T/Properties.png",
      github:"link",
      live:"link",
    techStack:"Html,CSS,Javascript"
    },
    {
      title:"Group_App",
      imgURL:"https://i.postimg.cc/7LQRrDBw/Group-App.png",
      github:"link",
      live:"link",
    techStack:"Vue.js"
    },
    {
      title:"Pokemon Fetch API",
      imgURL:"https://i.postimg.cc/yxYX1pLB/Pokemon-Fetch-API.png",
      github:"link",
      live:"link",
    techStack:"Html,CSS,JavaScript"
    },
    {
      title:"Christ's Hand",
      imgURL:"https://i.postimg.cc/G2s4LYyM/Christ-s-hand.png",
      github:"link",
      live:"link",
    techStack:"Html,CSS"
    }
    ],
    active:0 
    };
  },

    methods: {
      On(index){
        this.active = index
      }
    },
}
</script>

<style lang="scss">
section#Projects{
background-color:#000 ;
height:95%;
width: 100vw;
@media (max-width:1200px) {
  height:fit-content;
  
}


.Projects{
  width: 100%;
  height: 100%;
  padding: 20px;
  padding-left: 0;
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
  .Projects-img{
    display: none;
  }
   .Projects-img.active{
    display: block;
    width: 50vw;
    height: 100%;
    object-fit: cover;
    color: #fff;
    padding-top:20px ;
        @media(max-width: 1200px) {
      width: 100vw;
      height: 100vw;
      object-position: center;
      object-fit: contain;
      padding: 10px;
      padding-bottom:6vh ;
    }
    img{
      width: 100%;
      height: 90%;
      
    }
    button{
      padding: 4px;
      border-radius: 10px;
      background: #000;
      color: #fff;
    }
   }
   .Projects-text{
    position: relative;
    width: 50vw;
    height: 100%;
    max-height: 95vw;
    color: white;
    font-weight: 200;
    overflow-y: scroll;
    padding: 15px;
    padding-top: 8vw;
    display: flex;
    flex-wrap:wrap ;
        @media (max-width:1200px) {
      width: 100vw;
      height: fit-content;
      overflow-y: hidden;
      overflow-x: hidden;
      max-height: fit-content;
      
    }
    
    &::before{
      position:absolute;
      content:"Projects";
      font-size:6vw;
      left: 2px;
      top: 10px;
      opacity: 0.7;
    }
    .project-card{
      border:3px solid #fff;
      padding: 10px;
      margin:7px;
      width: fit-content;
      background-color: gainsboro;
      color: #000;
      border-radius: 20px;

      
      .project-img{
        width:250px;
        height: 200Px;
        border: 5px solid #fff;
        background-color: #000;
        img{
          width: 100%;
          max-width: fit-content;
          height: 100%;
          max-height:fit-content ;
        }
      }
      button{
        padding: 2px;
        background: #000;
        color: #fff;
        border-radius: 10px;
        
        &:hover{
          background: #fff;
          color: #000;
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
         @media(max-width:1200) {
          ::-webkit-scrollbar{
         width:0;
       }
    }
</style>
