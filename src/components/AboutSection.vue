<template>
  <section id="about" class="slides">

       <v-container fluid class="slide" id="slide1">
      <v-row align="center" justify="center">

              

              <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="7">
               <v-img src="@/assets/img/money.jpg" class="d-block " max-width="350px" />
            </v-col>


            <v-col cols="12" md="5" class="d-none d-md-flex">
               

               <v-card-text>
               <h3 class=" display-2 mb-2">Investment</h3>
               <br/><br/>
                 Reap  enticing investment reward! Be confident in your investment because of the security  we provide you<br/>
                 <br/><br/>
                 <a>Learn more</a>
               </v-card-text>
               
            </v-col>
          </v-row>



          <v-row align="center" justify="center">
            <v-col cols="12" md="5">
             

               <v-card-text>
               <h3 class=" display-2 mb-2">Pay small small</h3>
               <br/><br/>
                 No matter how solid your plans are<br/> sometimes you dont have all the money<br/>
                 <br/><br/>
                 <a>Learn more</a>
               </v-card-text>
            </v-col>


            <v-col cols="12" md="7" class="d-none d-md-flex">
                 <v-img src="@/assets/img/atm.jpg" class="d-block ml-auto mr-auto" max-width="350px" />

               
               
            </v-col>
          </v-row>
        </v-col>

        </v-row>

      </v-container>



      <v-container fluid class="slide" id="slide2" >
      <v-row align="center" justify="center">

              

              <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="7">
               <v-img src="@/assets/img/webinar.jpg" class="d-block " max-width="350px" />
            </v-col>


            <v-col cols="12" md="5" class="d-none d-md-flex">
               

               <v-card-text>
               <h3 class=" display-2 mb-2">Webinars</h3>
               <br/><br/>
                 There are somay immigration question begging to be answered. Som many people are confused about how to process their immigration... <br/>
                 <br/><br/>
                 <a>Learn more</a>
               </v-card-text>
               
            </v-col>
          </v-row>



          <v-row align="center" justify="center">
            <v-col cols="12" md="5">
             

               <v-card-text>
               <h3 class=" display-2 mb-2">Education</h3>
               <br/><br/>
                To be honest we are not interested in the course you want to study. This is your decision.<br/> But we can guide you on how to make the best decision.<br/>
                 <br/><br/>
                 <a>Learn more</a>
               </v-card-text>
            </v-col>


            <v-col cols="12" md="7" class="d-none d-md-flex">
                 <v-img src="@/assets/img/education.jpg" class="d-block ml-auto mr-auto" max-width="350px" />

               
               
            </v-col>
          </v-row>
        </v-col>

        </v-row>

      </v-container>





      <span
         class="prev"
         @click="move(-1)"
        >
         <i class="fa fa-chevron-left" aria-hidden="true"></i>
       </span>
        <span
          class="next"
          @click="move(1)"
        >
          <i class="fa fa-chevron-right" aria-hidden="true"></i>
        </span>















  </section>
</template>




<script>

export default {
 // el: '#appl',
  

  data: () => ({
    active: 1,
    slides:2,
  }),
  methods: {
    move(amount) {
      let newActive
      
      const newIndex = this.active + amount
      if (newIndex > this.slides) newActive = 1
      if (newIndex === 0) newActive = this.slides
      this.active = newActive || newIndex;
     

      if(this.active <=1){
        const slide = document.querySelector("#slide"+ (this.active+ 1));
        slide.style.display="none"
        const slideNew = document.querySelector("#slide"+ (this.active));
        slideNew.style.height="block" 

      }else if(this.active > 1){

         
         const slide = document.querySelector("#slide"+ (this.active -1));
        slide.style.display="none"
        const slideNew = document.querySelector("#slide"+ (this.active));
        
        slideNew.style.display="block"

      }else{

         const slide = document.querySelector("#slide"+ (this.active+ 1));
        slide.style.display="none"
        const slideNew = document.querySelector("#slide"+ (this.active));
        slideNew.style.height="block" 

      }
      

     

    
    },
     jump(index) {
      this.active = index
    },
    
  },

  mounted(){
     const slides = document.querySelectorAll(".slide");
     slides.forEach( (slide,index) =>{
       if(index!==0){
         
         slide.style.display="none"
       }
       
     })
  }
}
</script>

<style scoped>
#about {
  
  background:#e5e5e5;
}


</style>




<style scoped>
.prev,
.next {
  position: absolute;
  top: 50%;
  width: 50px;
  height: 50px;
  border: 2px solid #221e21;
  color: #221e21;
  border-radius: 50%;
  margin-top: -25px;
  margin-left: 25px;
  cursor: pointer;
  line-height: 48px;
  text-align: center;
  text-indent: -2px;
  transition: all 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
.prev:hover,
.next:hover {
  background: #221e21;
  color: #fff;
  transform: scale(1.2);
}
.prev:active,
.next:active {
  transform: translate(0, 3px) scale(1.2);
}

.next {
  right: 20px;
  margin-left: auto;
  margin-right: 65px;
  text-indent: 2px;
}

.slides {
  
}
@media (min-width: 600px) {

}
@media (min-width: 900px) {
  .slides {
    
  }
}
.slides .animated {
  transition: all 400ms;
  position: absolute;
  transform: translate(-50%, -50%);
}
.slides .slide-in {
  opacity: 0;
  transform: translate(-40%, -50%);
}
.slides .slide-in-active {
  transition-delay: 150ms;
}
.slides .slide-out {
  opacity: 1;
}
.slides .slide-out-active {
  opacity: 0;
  transform: translate(-60%, -50%);
}

.buttons {
  position: absolute;
  top: 10px;
  left: 10px;
}

button {
  padding: 10px;
  outline: none;
  border: none;
  -webkit-appearance: none;
  background: #221e21;
  color: #fff;
  font-weight: bold;
  font-size: 18px;
  cursor: pointer;
}
button:disabled {
  opacity: 0.2;
  cursor: no-drop;
}
</style>
