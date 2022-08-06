<template>
  <div>
   <div class="mask">
  </div>
    <v-navigation-drawer
      v-model="drawer"
      app
      temporary
      
    >
      <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <img src="@/assets/img/logo.jpg" alt="Logo" />
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title class="title">LeapSail</v-list-item-title>
            
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider />

      <v-list dense>
        <v-list-item
          v-for="([icon, text, link], i) in items"
          :key="i"
          link
          @click="$vuetify.goTo(link)"
        >
          <v-list-item-icon class="justify-center">
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="subtitile-1">{{
              text
            }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      :color="color"
      
      
      class="px-15 "
      :class="{ expand: flat }"
    >
      <v-toolbar-title class="" style="color:orange; font-size:40px;font-family:comic-sans">
        Leapsail
      </v-toolbar-title>


      <v-btn text >
          <span class="mr-2 nav-text shareBtn" id="shareBtn">
          Why Leapsail
          <div class="triangle">
              
          </div>

          </span>
          <div class="shareContainer">
      <i id="f" class="icons" data-feather="facebook"></i>
      <i id="t" class="icons" data-feather="twitter"></i>
      <i id="g" class="icons" data-feather="github"></i>
      <i id="m" class="icons" data-feather="mail"></i>
      <i id="d" class="icons" data-feather="download"></i>
  </div>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#features')">
          <span class="mr-2 nav-text">Products</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#download')">
          <span class="mr-2 nav-text">Pricing</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#pricing')">
          <span class="mr-2 nav-text">
          Learn
          <div class="triangle">
              
          </div>
          </span>
        </v-btn>


      <v-spacer /><v-spacer />
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
        class="mr-4"
        v-if="isXs"
      />
      <div v-else>
        
         <v-btn text @click="$vuetify.goTo('#pricing')">
          <span class="mr-2 nav-text">Contact
          <div class="triangle"></div></span>
        </v-btn>

         <v-btn text @click="$vuetify.goTo('#pricing')">
          <span class="mr-2 nav-text">Support<div class="triangle"></div> </span>
        </v-btn>

        <v-btn text @click="$vuetify.goTo('#pricing')">
          <span class="mr-2 nav-text">Login</span>
        </v-btn>

        <v-btn rounded outlined text @click="$vuetify.goTo('#contact')" class="orange">
          <span class="mr-2 nav-text" style="color:#fff">Create Account  <div class="arrow-right">
              
          </div></span>
        </v-btn>
      </div>
    </v-app-bar>
  </div>
</template>

<style scoped>


.triangle {
    width: 0; 
    height: 0; 
    border-left: 5px solid transparent;
    border-right: 5px solid transparent;
    border-top: 5px solid black;
    float:right;
    margin-top:2px;
}

.arrow-right {
  width: 0; 
  height: 0; 
  border-top: 5px solid transparent;
  border-bottom: 5px solid transparent;
  margin-top:2px;
  float:right;
  margin-left:5px;
  color:#ffff;
  border-left: 5px solid white;
}

.mask{
  position : absolute;
  top : 0;
  left : 0;
  width : 100%;
  height : 100%;
  background : #0e0e0e;
  transition-timing-function: cubic-bezier(0.42,0.63,0.63,0.42);
  transition: display 1s;
  opacity : 0.8;
  z-index : -1;
  display : none;
}
.mask.show{
  display : block;
}


.v-toolbar {
  transition: 0.6s;
}

.orange{
  background: orange;
  color:#fff;
  font-size:12px;
}

.nav-text{font-size:12px;}

.expand {
  height: 80px !important;
  padding-top: 10px;
  background-color:#fff;
}
.background-nav{
  background:#fff;
}
</style>

<script>
export default {
  data: () => ({
    drawer: null,
    isXs: false,
    items: [
      ["mdi-home-outline", "Why leapsail", "#hero"],
      ["mdi-information-outline", "Products", "#features"],
      ["mdi-download-box-outline", "Pricing", "#download"],
      ["mdi-currency-usd", "Learn", "#pricing"],
      ["mdi-email-outline", "Contact", "#contact"],
      ["mdi-email-outline", "Support", "#contact"],
      ["mdi-email-outline", "Login", "#contact"],
    ],
  }),
  props: {
    color: String,
    flat: Boolean,
  },
  methods: {
    onResize() {
      this.isXs = window.innerWidth < 850;
    },
  },

  watch: {
    isXs(value) {
      if (!value) {
        if (this.drawer) {
          this.drawer = false;
        }
      }
    },
  },
  mounted() {
    this.onResize();
    window.addEventListener("resize", this.onResize, { passive: true });


  let shareButton = document.querySelector('#shareBtn');
  let mask = document.querySelector('.mask');
  let shareContainer = document.querySelector('.shareContainer');
  let icons = document.querySelectorAll('.icons');
  shareButton.addEventListener('click',function(e){
        shareButton.setAttribute("data-feather","more-vertical")
        shareContainer.classList.add('show');
        mask.classList.add('show');
        shareButton.classList.add('show');
        for(let i = 0; i < icons.length;i++)
          icons[i].classList.add('show')
  });

  window.addEventListener('keyup',function(e){
    if(e.keyCode == 27){
      shareButton.setAttribute("data-feather","more-horizontal")
        shareContainer.classList.remove('show');
        mask.classList.remove('show');
        shareButton.classList.remove('show');
        for(let i = 0; i < icons.length;i++)
          icons[i].classList.remove('show')
    }
  })
  window.addEventListener('click',function(e){
    if(e.target != shareButton){
      shareButton.setAttribute("data-feather","more-horizontal")
        shareContainer.classList.remove('show');
        mask.classList.remove('show');
        shareButton.classList.remove('show');
        for(let i = 0; i < icons.length;i++)
          icons[i].classList.remove('show')
    }
  })
  },
};
</script>
