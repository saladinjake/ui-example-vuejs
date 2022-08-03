<template>
  <v-app>
    <navigation :color="color" :flat="flat" />
    <v-main class="pt-0">
      <hero />
      
    </v-main>
    
    
  </v-app>
</template>

<style scoped>
.v-main {
 background:#eaeaea;
}
</style>

<script>
import navigation from "./components/Navigation";
import hero from "./components/HeroSection";


export default {
  name: "App",

  components: {
    navigation,
    hero,
    
  },

  data: () => ({
    fab: null,
    color: "",
    flat: null,
  }),

  created() {
    const top = window.pageYOffset || 0;
    if (top <= 60) {
      this.color = "transparent";
      this.flat = true;
    }
  },

  watch: {
    fab(value) {
      if (value) {
        this.color = "#fff";
        //this.color = "secondary";
        this.flat = false;
      } else {
        this.color = "#fff";
        this.flat = true;
      }
    },
  },

  methods: {
    onScroll(e) {
      if (typeof window === "undefined") return;
      const top = window.pageYOffset || e.target.scrollTop || 0;
      this.fab = top > 60;
    },
    toTop() {
      this.$vuetify.goTo(0);
    },
  },
};
</script>
