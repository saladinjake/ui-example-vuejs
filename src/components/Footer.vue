<template>
<div  style="background:orange">



<v-container fluid >
      <v-row align="center" justify="center" class="mt-10 mb-10" >
        <v-col cols="12">
          <v-row align="center" justify="space-around">
           <v-col cols="12" class="text-center">
              <h1 class="font-weight-light display-2 white--text"> Try leapsail.com for your comfort</h1>
              <h1 class="font-weight-light white--text">
               coman buy our market| debit card go dey needed.
              </h1>
            </v-col> 
          </v-row>
        </v-col>
    </v-row>


      <v-row align="center" justify="space-around">
           <v-col cols="12" class="text-center">
           
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
      <br/><br/>
</v-container>
<div class="pg-footer">
    <footer class="footer">
     
      <div class="footer-content">
        <div class="footer-content-column">
          <div class="footer-logo">
            <a class="footer-logo-link" href="#">
              <span class="hidden-link-text">LOGO</span>
              <h1>LeapSail</h1>
               <br/><br/>
              <p> All right reserverd &copy leapsail.com</p>
            </a>
          </div>
          <div class="footer-menu">
            <h2 class="footer-menu-name">Address</h2>
            <ul id="menu-get-started" class="footer-menu-list">
              
              <li class="menu-item menu-item-type-post_type menu-item-object-product">
                <a href="#">23 Ezekiel Street off Toyin Street . Ikeja</a>
              </li>
              
            </ul>
          </div>
        </div>
        <div class="footer-content-column">
          <div class="footer-menu">
            <h2 class="footer-menu-name"> Product</h2>
            <ul id="menu-company" class="footer-menu-list">
              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">Product</a>
              </li>
              <li class="menu-item menu-item-type-taxonomy menu-item-object-category">
                <a href="#">Pricing</a>
              </li>
              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">Partners</a>
              </li>
              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">Affiliate</a>
              </li>
              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">Students</a>
              </li>

              

            </ul>
          </div>
          <div class="footer-menu">
            
          </div>
        </div>
        <div class="footer-content-column">
          <div class="footer-menu">

          <h2 class="footer-menu-name"> Teams</h2>
            <ul id="menu-legal" class="footer-menu-list">
              <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-privacy-policy menu-item-170434">
                <a href="#">About</a>
              </li>
              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">Contactus</a>
              </li>
              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">Careers</a>
              </li>

              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">Find a Partner</a>
              </li>

              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">In The News</a>
              </li>

            </ul>
            
          </div>
        </div>
        <div class="footer-content-column">
          <div class="footer-call-to-action">
            <h2 class="footer-menu-name"> Resources</h2>
            <ul id="menu-quick-links" class="footer-menu-list">
              <li class="menu-item menu-item-type-custom menu-item-object-custom">
                <a target="_blank" rel="noopener noreferrer" href="#">Knowledge base</a>
              </li>
              <li class="menu-item menu-item-type-custom menu-item-object-custom">
                <a target="_blank" rel="noopener noreferrer" href="#">Guides</a>
              </li>
              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">Daily webinars</a>
              </li>
              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">Community</a>
              </li>
              <li class="menu-item menu-item-type-post_type_archive menu-item-object-customer">
                <a href="#">Customers stores</a></li>
              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">Video Tutorials</a>
              </li>

              <li class="menu-item menu-item-type-post_type menu-item-object-page">
                <a href="#">Blogs</a>
              </li>

            </ul>
          </div>
          <div class="footer-call-to-action">
           
          </div>
        </div>
        
      </div>
     
    </footer>
  </div>
  
  <v-divider></v-divider>

  <v-footer  padless>
    <v-card flat tile class="secondary  text-center">
     

      <v-card-text class="white--text pt-0">
        <a class="padded-link">Status</a> 
        <a class="padded-link">Security</a>
        <a class="padded-link">Terms of Sevice</a>
        <a class="padded-link">Privacy Policy</a>
        <a class="padded-link">Accessibility Statement</a>
          <a class="padded-link">English</a>
        <v-btn
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-4 "
          :href="icon.link"
          target="_blank"
          icon
        >
          <v-icon size="24px">{{ icon.text }}</v-icon>
        </v-btn>
      </v-card-text>

    

    
    </v-card>
  </v-footer>

  </div>
</template>

<style scoped>
.v-card {
  width: 100%;
}





.padded-link{
  margin:10px;
  padding:10px;
  width:300px;
  color:#000;
}





* {
  margin: 0;
  padding: 0;
}
a {
  color: #fff;
  text-decoration: none;
}
.pg-footer {
  font-family: 'Roboto', sans-serif;
}


.footer {
     background:#e5e5e5;
    color: #000;
}


.footer-content {
    margin-left: auto;
    margin-right: auto;
    max-width: 1230px;
    padding: 40px 15px 450px;
    position: relative;
}

.footer-content-column {
    box-sizing: border-box;
    float: left;
    padding-left: 15px;
    padding-right: 15px;
    width: 100%;
    color: #000;
}

.footer-content-column ul li a {
  color: #000;
  text-decoration: none;
}

.footer-logo-link {
    display: inline-block;
    color:orange;
}
.footer-menu {
    margin-top: 30px;
}

.footer-menu-name {
    color: #000;
    font-size: 15px;
    font-weight: 900;
    letter-spacing: .1em;
    line-height: 18px;
    margin-bottom: 0;
    margin-top: 0;
    text-transform: uppercase;
}
.footer-menu-list {
    list-style: none;
    margin-bottom: 0;
    margin-top: 10px;
    padding-left: 0;
}
.footer-menu-list li {
    margin-top: 5px;
}

.footer-call-to-action-description {
    color: #000;
    margin-top: 10px;
    margin-bottom: 20px;
}
.footer-call-to-action-button:hover {
    background-color: #000;
    
}
.button:last-of-type {
    margin-right: 0;
}
.footer-call-to-action-button {
    background-color: #027b9a;
    border-radius: 21px;
   
    display: inline-block;
    font-size: 11px;
    font-weight: 900;
    letter-spacing: .1em;
    line-height: 18px;
    padding: 12px 30px;
    margin: 0 10px 10px 0;
    text-decoration: none;
    text-transform: uppercase;
    transition: background-color .2s;
    cursor: pointer;
    position: relative;
}
.footer-call-to-action {
    margin-top: 30px;
}
.footer-call-to-action-title {
   
    font-size: 14px;
    font-weight: 900;
    letter-spacing: .1em;
    line-height: 18px;
    margin-bottom: 0;
    margin-top: 0;
    text-transform: uppercase;
}
.footer-call-to-action-link-wrapper {
    margin-bottom: 0;
    margin-top: 10px;
    color: #fff;
    text-decoration: none;
}
.footer-call-to-action-link-wrapper a {
    color: #fff;
    text-decoration: none;
}





.footer-social-links {
    bottom: 0;
    height: 54px;
    position: absolute;
    right: 0;
    width: 236px;
}




.footer-social-link.linkedin {
    height: 26px;
    left: 3px;
    top: 11px;
    width: 26px;
}

.footer-social-link {
    display: block;
    padding: 10px;
    position: absolute;
}

.hidden-link-text {
    position: absolute;
    clip: rect(1px 1px 1px 1px);
    clip: rect(1px,1px,1px,1px);
    -webkit-clip-path: inset(0px 0px 99.9% 99.9%);
    clip-path: inset(0px 0px 99.9% 99.9%);
    overflow: hidden;
    height: 1px;
    width: 1px;
    padding: 0;
    border: 0;
    top: 50%;
}

.footer-social-icon-svg {
    display: block;
}

.footer-social-icon-path {
    fill: #fffff2;
    transition: fill .2s;
}

.footer-social-link.twitter {
    height: 28px;
    left: 62px;
    top: 3px;
    width: 28px;
}

.footer-social-link.youtube {
    height: 24px;
    left: 123px;
    top: 12px;
    width: 24px;
}

.footer-social-link.github {
    height: 34px;
    left: 172px;
    top: 7px;
    width: 34px;
}

.footer-copyright {
    background-color: #027b9a;
    color: #fff;
    padding: 15px 30px;
  text-align: center;
}

.footer-copyright-wrapper {
    margin-left: auto;
    margin-right: auto;
    max-width: 1200px;
}

.footer-copyright-text {
  color: #fff;
    font-size: 13px;
    font-weight: 400;
    line-height: 18px;
    margin-bottom: 0;
    margin-top: 0;
}

.footer-copyright-link {
    color: #fff;
    text-decoration: none;
}







/* Media Query For different screens */
@media (min-width:320px) and (max-width:479px)  { /* smartphones, portrait iPhone, portrait 480x320 phones (Android) */
  .footer-content {
    margin-left: auto;
    margin-right: auto;
    max-width: 1230px;
    padding: 40px 15px 1050px;
    position: relative;
  }
}
@media (min-width:480px) and (max-width:599px)  { /* smartphones, Android phones, landscape iPhone */
  .footer-content {
    margin-left: auto;
    margin-right: auto;
    max-width: 1230px;
    padding: 40px 15px 1050px;
    position: relative;
  }
}
@media (min-width:600px) and (max-width: 800px)  { /* portrait tablets, portrait iPad, e-readers (Nook/Kindle), landscape 800x480 phones (Android) */
  .footer-content {
    margin-left: auto;
    margin-right: auto;
    max-width: 1230px;
    padding: 40px 15px 1050px;
    position: relative;
  }
}
@media (min-width:801px)  { /* tablet, landscape iPad, lo-res laptops ands desktops */

}
@media (min-width:1025px) { /* big landscape tablets, laptops, and desktops */

}
@media (min-width:1281px) { /* hi-res laptops and desktops */

}




@media (min-width: 760px) {
  .footer-content {
      margin-left: auto;
      margin-right: auto;
      max-width: 1230px;
      padding: 40px 15px 450px;
      position: relative;
  }

  .footer-wave-svg {
      height: 50px;
  }

  .footer-content-column {
      width: 24.99%;
  }
}
@media (min-width: 568px) {
  /* .footer-content-column {
      width: 49.99%;
  } */
}

</style>

<script>
export default {
  data: () => ({
    icons: [
      {
        text: "mdi-facebook",
        link: "",
      },
      {
        text: "mdi-twitter",
        link: "",
      },
      {
        text: "mdi-linkedin",
        link: "",
      },
      {
        text: "mdi-instagram",
        link: "https://instagram.com/joabson_arley/",
      },
    ],
  }),
};
</script>
