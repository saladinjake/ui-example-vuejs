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
              
              <v-row style="margin-left:140px">
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/icon1.svg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    step 1
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/icon2.svg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    step 2
                  </p>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <v-img
                    src="@/assets/img/icon3.svg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <p class="text-justify">
                    step3
                  </p>
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

  height: 500px;
}

#download .container,
#download .row {
  height: 100%;
}
</style>