<template>
<section id="Projects">
  <div  class="Projects">
    <div v-for="(project,index) in projects" :key="index"  class="Projects-img" :class="{active:active === index}">
      <img :src="project.imgURL" alt="">
      <h1>{{project.title}}</h1>
      <a :href="project.github" target="_black"><button>Github</button></a>  <a :href="project.live" target="_black"><button>Live</button> </a>
      <P>Tech stack: {{project.techStack}}</P>
    </div>
    <div class="Projects-text">
      <div class="filter">
        <select name="TechStack" id="TechStack"  v-model="value" @change="FilteringProjects()">
          <option value="" >All</option>
          <option value="Html,CSS">Html,CSS</option>
          <option value="Html,CSS,Bootstrap">Html,CSS,Bootstrap</option>
          <option value="Html,CSS,Javascript">Html,CSS,Javascript</option>
          <option value="Vue.js">Vue.js</option>
        </select>
      </div>
      <div class="project">

        <div  v-show="filtering" v-for="(project,index) in FilteredProjects" :key="index"  class="project-card" >
        <div class="project-img">
         <img :src="project.imgURL" alt=""/>
        </div>
          <h3>{{project.title}}</h3>
        <button @click="On(index)"><i class="fa-solid fa-eye"></i></button>
        </div>
         <div v-show="!filtering" v-for="(project,index) in projects" :key="index"  class="project-card" >
        <div class="project-img">
         <img :src="project.imgURL" alt=""/>
        </div>
          <h3>{{project.title}}</h3>
        <button @click="On(index)"><i class="fa-solid fa-eye"></i></button>
          
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
      projects:[
    {
    title:"Font Gallery",
    imgURL:"https://i.postimg.cc/SQdTV9s1/font-gallery.png",
    github:"https://github.com/LihleGoliath/gallery",
    live:"https://dynamic-gingersnap-5d2507.netlify.app/",
    techStack:"Html,CSS"
    },
    {
     title:"Calculator",
     imgURL:"https://i.postimg.cc/N0TgXF6b/Calulator.png",
     github:"https://github.com/LihleGoliath/calculator",
     live:"https://cheery-axolotl-7cf81a.netlify.app/",
    techStack:"Html,CSS"
    },
    {
      title:"Restaurantly",
      imgURL:"https://i.postimg.cc/LXK9y7yS/Screenshot-2022-05-31-115944.png",
      github:"https://github.com/LihleGoliath/restaurant_project",
      live:"https://profound-alpaca-3fa441.netlify.app/",
    techStack:"Html,CSS,Bootstrap"
    },
    {
      title:"BMI Calculator",
      imgURL:"https://i.postimg.cc/ZRRwwgZ2/BMI-calculator.png",
      github:"https://github.com/LihleGoliath/BMI_calculator",
      live:"https://classy-truffle-be8973.netlify.app/",
    techStack:"Html,CSS,JavaScript"
    },
    {
      title:"Temp Calculator",
      imgURL:"https://i.postimg.cc/mD80DC2f/TEMP-calculator.png",
      github:"https://github.com/LihleGoliath/Temperature_Calcu-ator",
      live:"https://delicate-cuchufli-37eab7.netlify.app/",
    techStack:"Html,CSS,Javascript"
    },
    {
      title:"Properties",
      imgURL:"https://i.postimg.cc/ht4M4j3T/Properties.png",
      github:"https://github.com/LihleGoliath/js-apartments",
      live:"https://animated-cascaron-de047e.netlify.app/",
    techStack:"Html,CSS,Javascript"
    },
    {
      title:"Group_App",
      imgURL:"https://i.postimg.cc/7LQRrDBw/Group-App.png",
      github:"https://github.com/siyolisemekuto/group_app",
      live:"link",
    techStack:"Vue.js"
    },
    {
      title:"Pokemon Fetch API",
      imgURL:"https://i.postimg.cc/yxYX1pLB/Pokemon-Fetch-API.png",
      github:"https://github.com/LihleGoliath/fetch",
      live:"https://gorgeous-biscotti-189d83.netlify.app/",
    techStack:"Html,CSS,JavaScript"
    },
    {
      title:"Christ's Hand",
      imgURL:"https://i.postimg.cc/G2s4LYyM/Christ-s-hand.png",
      github:"https://github.com/LihleGoliath/net-ninja-book-project/blob/main/index.html",
      live:"https://enchanting-cucurucho-37c8e6.netlify.app/",
    techStack:"Html,CSS,Bootstrap"
    }
    ],
    active:0 ,
    value:"",
    FilteredProjects:[],
    filtering:false
    };
  },

    methods: {
      On(index){
        this.active = index
      },  
      FilteringProjects(){
        
        if(this.value ===  ""){
          return this.FilteredProjects = this.projects
         
        }else{
          this.FilteredProjects = this.projects?.filter((project) => {
           return project.techStack.toLocaleLowerCase().includes(this.value.toLocaleLowerCase()) 
          });
          this.filtering=true;
          return;
        }
        }
    },

      }
    

</script>

<style lang="scss" scoped>
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
      &:hover{
        color: royalblue;
        border: 1px solid royalblue;
      }
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
    flex-direction: column;
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

    i{
      font-size: 1vw;
    }
    .project{
      display: flex;
      flex-wrap:wrap;
      width: 100%;
    }

    #TechStack{
      padding: 8px;
      padding-bottom:3px;
      margin-bottom:15px ;
      font-size: 2vh;
      border:none;
      background: none;
      color: #fff;
      border-bottom:2px solid #fff;
      text-transform: uppercase;
      text-align: center;
      option{
       color: #000;

      }
    }
</style>
