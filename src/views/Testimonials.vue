<template>
<section id="Testimonials">
  <div v-for="(test,index) in testimonials" :key="index" class="Testimonials" :class="{active : active === index}">
    <div class="Testimonials-img">
      <img :src="test.imgURL" alt="">
    </div>
    <div class="Testimonials-text">
      <div class="text">
        <h1>{{test.Name}}</h1>
        <div class="contain">
          {{test.testimonial}}
        </div>
        <p>{{test.occupation}}</p>
  <button @click="Pervious" class="btn Pervious"><i class="fa-solid fa-arrow-left"></i></button>
   <button @click="Next" class="btn"><i class="fa-solid fa-arrow-right"></i></button>
      </div>
      </div>
  </div>
</section>
</template>
<script>
export default{
  data(){
    return{
        img:'http://get.imglarger.com:8889/results/2unRO0l9_4x.jpg',
       
       testimonials:[
        {
            Name:"Jason",
            testimonial:"Lihle never fails to put a smile on your face. He is very welcoming and caring, which are traits that he also applies to his work. He always carries himself in a humble and friendly manner and is a pillar of support among his peers.",
            occupation:"Lecturer",
            imgURL:"https://i.postimg.cc/XvKL09s3/Jason-Wandrag.jpg"
        },
        {
            Name:"Siyolise",
            testimonial:"Goliath is not afraid to make an impression. He is outspoken and pleasently socail with his colleagues. He takes every opportunity to learn and showcase his passion with both hands",
            occupation:"Co-student",
            imgURL:`https://i.postimg.cc/xdTz1r0R/Copy-of-Siyolise-3-min.jpg`
        },
        {
            Name:"Joshua",
            testimonial:"Lihle is a stand-out guy with a great personality. He always sees the good in people and has displayed strong leadership qualities over the short period of time I got to know him.",
            occupation:"Co-student",
            imgURL:`https://i.postimg.cc/PJmxMKXJ/Joshua-4-min.jpg`
        },
        {
            Name:"Cameron",
            testimonial:"Lihle Goliath is a very competent individual, he strives higher than what he is capable of doing. His passion for his work preference is outstanding and he is a headstrong and smart working person",
            occupation:"Co-student",
            imgURL:`https://i.postimg.cc/ryCMQDGD/Cameron-3-min.jpg`
        },
        {
            Name:"Mika",
            testimonial:"Lihle is a very inquisitive person that's eager to learn. He is not shy to ask for clarity and enjoys talking about the different views others have. He would make an excellent addition wherever he goes.",
            occupation:"Co-student",
            imgURL:`https://i.postimg.cc/rwd6Xs4C/Mika-2-min.jpg`
        },
        {
            Name:"Fatima",
            testimonial:"Lihle is an individual with a kind spirit, he portrays himself as unapologetically authentic and is especially talented at what he does. His natural ability to connect with people is to be admired.",
            occupation:"Co-student",
            imgURL:`https://i.postimg.cc/3JdfW6w3/Fatima-2-min.jpg`
        }
    ],
    active:0
    }
  },
  methods: {
    Next(){
      console.log("hello")
     this.active === this.testimonials.length - 1 ? (this.active = 0 ) : ( this.active = this.active + 1)
    },
    Pervious(){
      console.log("hello")
     this.active === this.testimonials.length - 1 ? (this.active = 0 ) : ( this.active = this.active - 1)
    }
  },
}
</script>

<style lang="scss" scoped>

section#Testimonials{
background-color:#000 ;
height:95%;
width: 100vw;
display: flex;
transition: 0.5s ease all;
  @media(max-width: 1200px){
    flex-direction: column;
    width: fit-content;
    max-width: 100vw;
    height: 100%;
    max-height: fit-content;
    overflow-y: scroll;
    overflow-x: hidden;
  }

.Testimonials{
  display: none;
}
.active{
  
  width: 100%;
  height: 100%;
  padding: 20px;
  padding-left:0;
  margin: auto;
  transition: 0.5s ease all;
  display: flex;
  flex-direction: row-reverse;
  justify-content: space-evenly;
  @media(max-width: 1200px){
    flex-direction: column;
    width: fit-content;
    max-width: 100vw;
    height: fit-content;

    overflow-y: scroll;
    overflow-x: hidden;
    
  }

 

   .Testimonials-img{
    width: 50vw;
    height: 100%;
    display: flex;
    justify-content: center;
    align-content: center;
    transition: 0.5s ease all;
    object-fit: cover;
    @media(max-width: 1200px) {
      width: 100vw;
      height: 80vh;
      object-position: center;
      object-fit: contain;
      padding: 10px;
    }
    img{
      width: 100%;
      height: 100%;
    }
   }
   .Testimonials-text{
    position: relative;
    width: 50vw;
    height: 100%;
    max-height: 95vw;
    color: white;
    font-weight: 200;
    overflow-y: scroll;
    padding: 15px;
    padding-top: 8vw;
    transition: 0.5s ease all;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
   
      @media (max-width:1200px) {
      width: 100vw;
      height: 100%;
      overflow-y: hidden;
      overflow-x: hidden;
      max-height: 100%;
      
    }
     &::before{
    content: "Testmonials";
    position: absolute;
    font-size:6vw;
    left:2px;
    top:10px;
    opacity: 0.7;
  }
      .text{
      border: 1px solid #fff;
      width: fit-content;
      max-width: 100%;
      height: fit-content;
      // max-height:100%;
      padding: 15px;
      border-radius: 20px;
      @media(max-width: 1200){
        margin-top:px;
      }
      .contain{
        margin: 2px;
        margin-bottom: 0;
        padding: 5px;
        background-color: #fff;
        color: #000;
        font-weight: 200;
        border-radius: 10px;
    
      }
      p{
        background: #fff;
        color:#000;
        margin: auto;
        width:fit-content;
        border-bottom-left-radius: 6px;
        border-bottom-right-radius: 6px;
        font-size:1rem;
        font-weight: bold;
        padding: 2px;

      }
      .btn{
        margin-top:10px;
        padding: 2px;
        padding-top:0 ;
        padding-bottom:0;
        font-size:larger;
      }
      .Pervious{
        margin-right:5px;
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
      button{
        height: fit-content;
      }
          @media only screen and(max-width:1200px) {
       ::-webkit-scrollbar{
      width:0;
    }
     }
</style>
