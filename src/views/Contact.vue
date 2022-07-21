<template>
<section id="contact">
  <div class="contact">
    <div class="contact-img">
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3308.4144564060257!2d18.56205635050133!3d-33.98188668052994!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1dcc44e0d2ed21b5%3A0xc7b68a9ffbf85ad0!2s77%20Ny11%2C%20Guguletu%2C%20Cape%20Town%2C%207750!5e0!3m2!1sen!2sza!4v1658228863745!5m2!1sen!2sza" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>    </div>
    <div class="contact-text">
        <div class="get-in-touch">
            <h1>Let's Get in Touch</h1>        
        <div class="container">
            <i class="bi bi-geo-alt"></i>
            <div class="text-dark">
                <h3>Location:</h3>
                <p>Gugulethu,Cape Town  Western Cape</p>
            </div>
         </div>
        <div class="container">
            <i class="bi bi-envelope"></i>
            <div class="text-dark">
                <h3>Email:</h3>
                <p>lihlegoliath2@gmail.com</p>
            </div>
        </div>
        <div class="container">
            <i class="bi bi-phone"></i>
            <div class="text-dark">
                <h3>Phone:</h3>
                <p>+27 72 366 7902</p>
            </div>
        </div>
    </div>
    <div class="form">
    <h1>Message Me</h1>
        <form action="https://formspree.io/f/mrgjrpwl"
        method="POST"
         class="text-center"  target="_blank" >
            <div class="row">
                <div class="col-md-6">
                  <input type="text" name="Name" class="form-control" placeholder="Your Name" aria-label="First name" required>
                </div>
                <div class="col-md-6">
                  <input type="email" name="Email" class="form-control" placeholder="Your Email" aria-label="Last name" required>
                </div>
            </div>
                <div class="subject">
                  <input type="text" name="subject" class="form-control" placeholder="subject" aria-label="Subject" required>
               </div>                     
              <div class="textarea">
                <textarea name="Message" class="form-control" id="TextArea" rows="3" placeholder="Message" required></textarea>
              </div>
       <button type="submit" class="btn">Send Message</button>
        </form>
    </div>
      
      </div>
  </div>

</section>
</template>
<script>
export default{
  data(){
    return{
      img:'http://get.imglarger.com:8889/results/2unRO0l9_4x.jpg'
    }
  }
}
</script>

<style lang="scss">
section#contact{
background-color:#000 ;
height:95%;
width: 100vw;
@media (max-width:1200px) {
  height:fit-content;
  
}

.contact{
  width: 100%;
  height: 100%;
  padding: 20px;
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
   .contact-img{
    width: 50vw;
    height: 100%;
      object-fit: cover;
    @media(max-width: 1200px) {
      width: 100vw;
      height: 50vh;
      object-position: center;
      object-fit: contain;
      padding: 10px;
    }
    iframe{
      width: 100%;
      height: 100%;
    
    }
   }
   .contact-text{
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
    content: 'Contact Me';
    font-size: 6vw;
    left:2px;
    top:3px;
    opacity: 0.7;
   }

  

   .get-in-touch{
    margin: 10px;
     margin-top: 20px;
    padding: 10px;
    padding-bottom: 20px;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-items: center;
    gap:20px;
     border:2px solid #fff;
    border-radius:20px;
    
    
     h1{
   text-decoration: underline;
   }

    .container{
        border: 1px solid white;
        background-color: gainsboro;
        color: #000;
        border-radius: 10px;
        width: fit-content;
        max-width:250px;
        padding: 5px;
        text-align: center;
        &:hover{
            background-color: #000;
            color: #fff;
            transition: 0.5s ease all;
        }
    }
   }
    
    .form{
        margin-top: 30px;
        border: 1px solid #fff;
        color:#000;
        background-color: gainsboro;
        border-radius: 22px;
        padding: 10px;

        h1{
            text-decoration: underline;
        }
      
      form{
          display: flex;
          flex-direction: column;
          gap:20px;
          text-align: center;
          
        .row{
            display:flex;
            flex-direction: column;
            flex-wrap:wrap;
            gap: 20px;
            

          .col-md-6{
            input{
             background: none;
             color: #000;
             width: 80%;
             padding: 9px;
             border:none;
             border-bottom:2px solid #000;
             display: flex;
             flex-grow: 1;
             margin: auto;            
            }
          }
        }
          .subject{
            input{
             background: none;
             color: #000;
             width: 80%;
             padding: 9px;
             border:none;
             border-bottom:2px solid #000;
             display: flex;
             flex-grow: 1;
             margin: auto; 
            }
          }
          .textarea{

            textarea{
            background: none;
             color: #000;
             width: 80%;
             padding: 9px;
             border:none;
             border-bottom:2px solid #000;
             display: flex;
             flex-grow: 1;
             margin: auto; 
            }
          }
          .btn{
            background-color: #000;
             color: #fff;
             width: fit-content;
             margin:auto;
             padding: 10px; 
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
