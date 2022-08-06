<template>
  <section id="download">
    <v-container fluid>
      
      <v-row align="center" justify="center" style="margin-top:-10px;">
        <v-col cols="12" style="background:#fff">
        <h1 class=" display-2 mb-2" style="margin-left:120px">Why Leapsail?</h1>
     <p class="mb-2" style="color:#ddd; font-size:44px; margin-left:120px">Excellent customer relations?<span style="color:orange"> of course!</span></p>
     <br/><br/>
     </v-col>
   <v-col cols="10">
          <v-row align="center" justify="center">
            <v-col sm="4" class="hidden-xs-only">
              <v-img src="@/assets/img/growth.jpg" class="d-block ml-auto mr-auto"  />
            </v-col>
            <v-col cols="12" sm="8" class=" text-left" >
              <h3 style="margin-left:140px" class="font-weight-light display-2 mb-2">3 steps to get started</h3><br/>
              
              <v-row class="" style="margin-left:140px">
                <v-col cols="12" class="d-flex align-center">
                <div style="display:flex; flex-direction:column">
                   <p class="mr-10">01</p>
                   <p style="height:100px;width:1px;border:1px solid orange"></p>
                </div>
                  <div class=" more-margin" style="margin-top:-65px">
                   
                  <h4 class="text-justify more-margin">
                    Create an account
                  </h4>
                  <p class="more-margin">Sign up for an account with your name, best email address and your phone number</p>
                </div>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                   <div style="display:flex; flex-direction:column">
                   <p class="mr-10">02</p>
                   <p style="height:100px;width:1px;border:1px solid orange"></p>
                </div>
                   <div style="margin-top:-95px" >
                  <h4 class="text-justify more-margin">
                    Book a slot
                  </h4>

                  <p class="more-margin">you can speak with us or visit our office on appointment</p>
                  </div>
                </v-col>
                <v-col cols="12" class="d-flex align-center" style="margin-top:-50px">
                  <div style="display:flex; flex-direction:column">
                   <p class="mr-10">03</p>
                  
                </div>
                  <div style="margin-top:30px">
                  <h4 class="text-justify more-margin">
                    Grow with leapsail
                  </h4>
                  <p class="more-margin">Watch your investment grow, realize your dreams and begin your new life</p>
                  </div>
                </v-col>
              </v-row>
              
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
#download {

  height: 800px;
}

.more-margin{
  margin:10px;
}
.bordered-left{
  border-left:1px solid orange;
  margin-top:40px;
}

#download .container,
#download .row {
  height: 100%;
}
</style>