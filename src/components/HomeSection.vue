<template>
  <section id="hero">
    <v-parallax   height="700">
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col cols="12" md="6" xl="8">
              <h1 class="display-2 font-weight-bold mb-4 black-text">We are revolutionizing your concept of comfort</h1>
              <h1 class="font-weight-light black-text">
                created with a can do and achievers mindset. A self on-bording application with features that open you at a new day
              </h1>
              <v-btn
                rounded
                outlined
                large
                dark
                @click="$vuetify.goTo('#features')"
                class="mt-5 orange"
              >
                Get started
                
              </v-btn>
              <div class="video d-flex align-center py-4" >
                                

              <v-btn
                rounded
                outlined
                large
                dark
                @click="$vuetify.goTo('#features')"
                class="mt-5 black"
              >
              <v-icon class="ml-2">mdi-arrow-down</v-icon>
                App store
                
              </v-btn>


              <v-btn
                rounded
                outlined
                large
                dark
                @click="$vuetify.goTo('#features')"
                class="mt-5 black"
                style="margin-left:10px"
              >
              <v-icon class="ml-2">mdi-arrow-down</v-icon>
                Google Play
                
              </v-btn>

              </div>
            </v-col>
            <v-col  cols="12" md="6" xl="4" class="hidden-sm-and-down"> 
                <div class="box box1">
                  <img src="@/assets/img/icon2.png" />
                </div>

                   <div class="box box2">
                     <img src="@/assets/img/icon2.png" />
                   </div>
                    <div class="box box3">
                      <img src="@/assets/img/icon2.png" />
                    </div>

                    <div class="box box4">
                      <img src="@/assets/img/icon2.png" />
                    </div>

                    <div class="box box5">
                      <img src="@/assets/img/icon2.png" />
                    </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      
    </v-parallax>
    <v-container fluid id="features" class="mt-2">
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row align="center" justify="space-around">
           <v-col cols="12" class="text-center">
              <h1 class="font-weight-light display-2"> Work in ways that works for you</h1>
              <h1 class="font-weight-light">
               what would you like to manage with leapsail.com?
              </h1>
            </v-col> 
            <v-col
              cols="12"
              sm="2"
             
              v-for="(feature, i) in features"
              :key="i"
            >
             
                <div
                  class="badge" 
                >
                 <v-img
                   
                    max-width="100px"
                    v-bind:class="getRandomColor()" style="width: 100px; height: 50px;" v-bind:style="{  'padding':'10px', 'border-radius':'50%','margin-right':'5px', height:'30px', width:'30px' }"
                     class="img"
                  ><i ></i></v-img>
                  <h1 class="font-weight-regular d-block">{{ feature.title }}</h1>
                  
                </div>
              
            </v-col>

          </v-row>



         <v-row align="center" justify="space-around">
         

            <v-col
              cols="12"
              sm="2"
             
              v-for="(feature, i) in featuresTwo"
              :key="i"
            >
             
                <div
                  class="badge" 
                >
                   <v-img
                    
                    max-width="100px"
                    v-bind:class="getRandomColor()" style="width: 100px; height: 50px;" v-bind:style="{  'padding':'10px', 'border-radius':'50%','margin-right':'5px', height:'30px', width:'30px' }"
                     class="img"
                  ><i ></i></v-img>
                  <h1 class="font-weight-regular d-block">{{ feature.title }}</h1>
                  
                </div>
              
            </v-col>
         </v-row>



         <v-row align="center" justify="space-around">
         

            <v-col
              cols="12"
              sm="2"
             
              v-for="(feature, i) in featuresThree"
              :key="i"
            >
             
                <div
                  class="badge"
                >
                 <v-img
                    
                    max-width="100px"
                    v-bind:class="getRandomColor()" style="width: 200px; height: 100px;" v-bind:style="{  'padding':'10px', 'border-radius':'50%','margin-right':'5px', height:'30px', width:'30px' }"
                     class="img"
                  ><i ></i></v-img>
                  <h1 class="font-weight-regular d-block">{{ feature.title }}</h1>
                  
                </div>
              
            </v-col>
         </v-row> 





         <v-row align="center" justify="space-around"   >
         

            <v-col
              cols="12"
              sm="2"

             
              v-for="(feature, i) in featuresFour"
              :key="i"
            >
             
                <div
                  class="badge">
                  

                   <v-img
                    
                    max-width="100px"
                    v-bind:class="getRandomColor()" style="width: 200px; height: 100px;" v-bind:style="{  'padding':'10px', 'border-radius':'50%','margin-right':'5px', height:'30px', width:'30px' }"
                    class="img"
                  ><i ></i></v-img>


                  <h1 class="font-weight-regular ">{{ feature.title }}</h1>
                  
                </div>
              
            </v-col>


         </v-row> 


        <v-row align="center" justify="space-around">
           <v-col cols="12" class="text-center" style="margin-left:10px; margin-right:10px">
           
         <v-btn
                rounded
                outlined
                large
                dark
                @click="$vuetify.goTo('#features')"
                class="mt-5"
                style="background:orange"
              >
                Get started
                <v-icon class="ml-2">mdi-arrow-down</v-icon>
              </v-btn>

          </v-col>
      </v-row>

 

        </v-col>
      </v-row>
    </v-container>
    
   
  </section>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
      
      features: [
        {
          img: require("@/assets/img/icon2.png"),
          title: "Tour",
          
        },
        {
          img: require("@/assets/img/icon1.png"),
          title: "Webinner",
          
        },
        {
          img: require("@/assets/img/icon3.png"),
          title: "Educational",
          
        },

         {
          img: require("@/assets/img/icon3.png"),
          title: "Finance",
          
        },

         {
          img: require("@/assets/img/icon3.png"),
          title: "Investment",
          
        },
      ],


      featuresTwo: [
        {
          img: require("@/assets/img/icon2.png"),
          title: "Real estate",
          
        },
        {
          img: require("@/assets/img/icon1.png"),
          title: "Ticketing",
          
        },
        {
          img: require("@/assets/img/icon3.png"),
          title: "Visa",
          
        },

         {
          img: require("@/assets/img/icon3.png"),
          title: "Hotel",
          
        },

        
      ],


      featuresThree: [
        {
          img: require("@/assets/img/icon2.png"),
          title: "Reservations",
          
        },
        {
          img: require("@/assets/img/icon1.png"),
          title: "Events",
          
        },
        {
          img: require("@/assets/img/icon3.png"),
          title: "Entertainments",
          
        },

        {
          img: require("@/assets/img/icon3.png"),
          title: "Charity",
          
        },

        
      ],




      featuresFour: [
        {
          img: require("@/assets/img/icon2.png"),
          title: "Hub",
          
        },
        {
          img: require("@/assets/img/icon1.png"),
          title: "Immigration",
          
        },
        

        
      ],
    };
  },
  watch: {
    
  },
  methods: {
    getRandomColor: function(){
         const classes = ['badge--line','badge--info','badge--warning','badge--danger'];

         let array = [].concat(classes);
         let currentIndex = array.length, temporaryValue, randomIndex;

        // While there remain elements to shuffle...
        while (0 !== currentIndex) {

          // Pick a remaining element...
          randomIndex = Math.floor(Math.random() * currentIndex);
          currentIndex -= 1;

          // And swap it with the current element.
          temporaryValue = array[currentIndex];
          array[currentIndex] = array[randomIndex];
          array[randomIndex] = temporaryValue;
        }

        return array[0];

       
     },
  }
};
</script>

<style lang="scss">
.circle {
  stroke: white;
  stroke-dasharray: 650;
  stroke-dashoffset: 650;
  -webkit-transition: all 0.5s ease-in-out;
  opacity: 0.3;
}

</style>

<style>

 .box {
            height: 200px;
            width: 200px;
            border-right: 5px solid;
            background-color: white;
            float:left;
           
        }
 .box{
   transform: rotate(46deg);
   padding-bottom:15px;
}

.box img{
   transform: rotate(16deg);
   width:100%;
   padding-bottom:15px;

}
.box1, .box2, .box3, .box4, .box5{
  position:absolute;
}

.box1{
  right:220px;
  top:90px
}

.box2{
  right:80px;
  top:290px
}

.box3{
  right:380px;
  top:255px
}


.box4{
  right:370px;
  top:480px;
  width:100px;
  height:100px;
}

.box5{
  right:130px;
  top:450px;
  width:100px;
  height:100px;
}

.btn-play {
  transition: 0.2s;
}

.black-text{
  color:#000;
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}

#hero {
  z-index: 0;
}
.svg-border-waves img {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  margin-bottom: -2px;
  z-index: -1;
}

.card {
  min-height: 300px;
  padding: 10px;
  transition: 0.5s ease-out;
}




.badge {
  box-sizing: border-box;
  display:inline-block;
  background-color: #f5f5f5;
  color: #000;
  border-radius: 3rem;
  text-align: center;
  font-size: 13px;
 
  padding: 0px;
  line-height: inherit;
  min-width:210px;
  margin:10px;
 
}

.badge .img {
  float:left;
  margin-right:20px;
}

.black{
  background:#000;
}
.orange{
  background:orange;
}


.badge h1 {
  float:right;
  margin-right:10px;
  padding:5px;
}

.badge--line {
  background-color: transparent;
  color: #95a5a6;
  box-shadow: 0 0 0 1px #95a5a6;
}

.badge--info {
  background-color: #3498db;
}

.badge--warning {
  background-color: #f1c40f;
}

.badge--danger {
  background-color: #e74c3c;
}

.badge--success {
  background-color: #2ecc71;
}

.badge--small {
  font-size: 1.2rem;
  padding: 0.1rem 0.65rem 0.2rem;
}

.badge--smaller {
  font-size: 0.7rem;
  padding: 0.05rem 0.4rem 0.15rem;
}

</style>

<style>
section {
  position: relative;

  background-image: url("~@/assets/img/bg.jpg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}















</style>
