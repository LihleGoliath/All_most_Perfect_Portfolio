<template>
<section id="Testimonials">
  <div v-for="(test,index) in testimonials" :key="index" class="Testimonials" :class="{active : index}">
    <div class="Testimonials-img">
      <img :src="test.imgURL" alt="">
    </div>
    <div class="Testimonials-text">
      <h1>{{test.Name}}</h1>
      <div class="contain">
        {{test.testimonial}}
      </div>
      <p>{{test.occupation}}</p>
 <button @click="Next">Next</button>
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
            testimonial:"lorem",
            occupation:"Lecturer",
            imgURL:`https://i.postimg.cc/kXbN0d4R/T02-LW4-RMXJQ-U036-JA3-NVL5-45897a34dc43-512.jpg`
        },
        {
            Name:"Siyolise",
            testimonial:"lorem",
            occupation:"Co-student",
            imgURL:`https://i.postimg.cc/xdTz1r0R/Copy-of-Siyolise-3-min.jpg`
        },
        {
            Name:"Joshua",
            testimonial:"lorem",
            occupation:"Co-student",
            imgURL:`https://i.postimg.cc/PJmxMKXJ/Joshua-4-min.jpg`
        },
        {
            Name:"Cameron",
            testimonial:"lorem",
            occupation:"Co-student",
            imgURL:`https://i.postimg.cc/ryCMQDGD/Cameron-3-min.jpg`
        },
        {
            Name:"Mika",
            testimonial:"lorem",
            occupation:"Co-student",
            imgURL:`https://i.postimg.cc/rwd6Xs4C/Mika-2-min.jpg`
        },
        {
            Name:"Fatima",
            testimonial:"lorem",
            occupation:"Co-student",
            imgURL:`https://i.postimg.cc/3JdfW6w3/Fatima-2-min.jpg`
        }
    ],
    active:0
    }
  },
  methods: {
    Next(){
     this.active = this.active ? this.active : this.active + 1
    }
  },
}
</script>

<style lang="scss">
.Testimonials{
    display: none;
}
.Testimonials.active{
    display: block;
}
section#Testimonials{
background-color:#000 ;
height:95%;
width: 100vw;


.Testimonials{
  width: 100%;
  height: 100%;
  padding: 20px;
  margin: auto;
  display: flex;
  flex-direction: row-reverse;
  justify-content: space-evenly;
   .Testimonials-img{
    width: 50vw;
    height: 100%;
      object-fit: cover;
    img{
      width: 100%;
      height: 100%;
    }
   }
   .Testimonials-text{
    width: 50vw;
    height: 100%;
    max-height: 95vw;
    color: white;
    font-weight: 200;
    overflow-y: scroll;
    padding: 15px;
    padding-top: 6vw;
   
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
</style>
