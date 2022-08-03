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
              <v-img src="@/assets/img/growth.jpg" class="d-block ml-auto mr-auto" max-width="350px" />
            </v-col>
            <v-col cols="12" sm="8" class=" text-left" >
              <h1 style="margin-left:140px" class="font-weight-light display-2 mb-2">3 steps to get started</h1>
              
              <v-row class="" style="margin-left:140px">
                <v-col cols="12" class="d-flex align-center">
                <p class="mr-10">01</p>
                  <div class="bordered-left more-margin">
                   
                  <h4 class="text-justify more-margin">
                    Create an account
                  </h4>
                  <p class="more-margin">Sign up for an account with your name, best email address and your phone number</p>
                </div>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                   <p class="mr-10">02</p>
                   <div class="bordered-left">
                  <h4 class="text-justify more-margin">
                    Book a slot
                  </h4>

                  <p class="more-margin">you can speak with us or visit our office on appointment</p>
                  </div>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <p class="mr-10">03</p>
                  <div class="bordered-left">
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