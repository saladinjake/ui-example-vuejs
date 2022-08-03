<template>
  <section id="about">
    <v-container fluid>
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
  </section>
</template>

<style scoped>
#about {
  
  background:#e5e5e5;
}
</style>
