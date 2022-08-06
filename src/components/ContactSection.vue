<template>
  <section class="pb-8" id="contact">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row justify="center">
            <v-col cols="12" sm="6">
              
              <v-row class="d-flex align-center">
                <div>
                <v-col cols="12" class="d-flex align-center" >
                  <div>
                  <v-img
                    src="@/assets/img/icon1.svg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <h4 class="text-justify">
                    Quick response chat
                  </h4>
                  </div>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                  <div>
                  <v-img
                    src="@/assets/img/icon2.svg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <h4 class="text-justify">
                    Live chat
                  </h4>
                  </div>
                </v-col>
                <v-col cols="12" class="d-flex align-center">
                <div>
                  <v-img
                    src="@/assets/img/icon3.svg"
                    max-width="60px"
                    class="mr-4"
                  />
                  <h4 class="text-justify">
                   Daily webinars
                  </h4>
                  </div>
                </v-col>
                </div>

                <div>
                     <v-img
                    src="@/assets/img/hero.jpg"
                    max-width="280px"
                    class="mr-4 avatar"
                  />
                </div>
              </v-row>

            </v-col>
            <v-col cols="12" sm="6" style="margin-top:30px">
              <h1 class="font-weight-light display-1">24/7 Customer Support</h1>
              <h3 class="font-weight-light mt-3">
                Our team is here to give you personalized support with
                in the hour available 24/7. Join daily live webinars , watch our tutorials, or browse through our knowledge   base
              </h3>
              
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<style scoped>
#contact {
  background-color: #f4f7f5;
}

.avatar{
  border-radius:50%;
  margin-left:10px;
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}

</style>

<script>
// import {db} from '@/main'

export default {
  
};
</script>
