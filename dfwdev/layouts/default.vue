<template>
  <v-app dark>
    <v-navigation-drawer
      temporary
      v-model="drawer"
      :clipped="clipped"
      fixed
      app
      color="brown darken-4"
      class="drawer"
    >
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
           <router-link to="/"> 
            <img
            src="../assets/img/logo.png"
            height="35"
          />
          </router-link>
          </v-list-item-title>
          <v-list-item-subtitle>Web Application Development</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>
      <v-container class="social-links">
      <a href="https://github.com/DFW-Dev" target="_blank">
      <v-btn icon>
        <v-icon small>fab fa-github</v-icon>
      </v-btn>
      </a>

      <a href="https://linkedin.com/company/dfwdev" target="_blank">
      <v-btn icon>
        <v-icon small>fab fa-linkedin</v-icon>
      </v-btn>
      </a>

      <a href="https://facebook.com/DFWDev" target="_blank">
      <v-btn icon>
        <v-icon small>fab fa-facebook</v-icon>
      </v-btn>
      </a>

      <a href="https://twitter.com/devdfw" target="_blank">
      <v-btn icon>
        <v-icon small>fab fa-twitter</v-icon>
      </v-btn>
      </a>
      </v-container>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      :color="navBelowFold ? 'rgb(13, 71, 161)' : 'transparent'"
      elevate-on-scroll
      ref="nav"
      scroll-threshold="200"
      v-scroll="handleScroll"
      class="mb-0 app-bar-custom"
    >
      <v-container fluid>
      <v-row class='pl-5 pr-5'>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="hidden-md-and-up"/>
      
      <v-toolbar-title class="mt-2">
      <router-link to="/">  
      <img  class="logo"
            src="../assets/img/logo.png"
            
          />
      </router-link>    
      </v-toolbar-title>
      <v-toolbar-items class="ml-10 hidden-sm-and-down">
        <v-btn color="white" text to="/" exact>Home</v-btn>
        <v-btn color="white" text to="/services" exact>Services</v-btn>
        <v-btn color="white" text to="/contact" exact>Contact</v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
      <div class="social-links hidden-sm-and-down">
      <a href="https://github.com/DFW-Dev" target="_blank">
      <v-btn icon>
        <v-icon color="white" medium>fab fa-github</v-icon>
      </v-btn>
      </a>
      <a href="https://linkedin.com/company/dfwdev" target="_blank">
      <v-btn icon>
        <v-icon color="white" medium>fab fa-linkedin</v-icon>
      </v-btn>
      </a>
      <a href="https://facebook.com/DFWDev" target="_blank">
      <v-btn icon>
        <v-icon color="white" medium>fab fa-facebook</v-icon>
      </v-btn>
      </a>
      <a href="https://www.instagram.com/dfwdev/" target="_blank">
      <v-btn icon>
        <v-icon color="white" small>fab fa-instagram</v-icon>
      </v-btn>
      </a>
      <a href="https://twitter.com/devdfw" target="_blank">
      <v-btn icon>
        <v-icon color="white" medium>fab fa-twitter</v-icon>
      </v-btn>
      </a>
      <!--
      <v-btn color="white" text to="/login" exact>Login</v-btn>
      //-->
      </div>
      </v-row>
      </v-container>
    </v-app-bar>
    <v-main class="pt-0">
      <div >
        <nuxt />
      </div>
    </v-main>
    <v-footer
    :fixed="fixed"
    padless
  >
    <v-sheet class="pa-15 bottom-contact" width="100%" color="blue darken-4 footer-contact">
          <v-container>
          <h3 class="display-1">Have a Project You Need Done?</h3>
          <b class="display-1">Lets Talk</b><br/>
          <v-btn class="mt-2 bottom-contact-btn" color="light-blue lighten-1" 
          to="/contact"
          >
          Get in Touch
          </v-btn>    
          </v-container>  
          </v-sheet> 
    <v-card
      class="flex footer"
      flat
      tile
    >

      <v-card-title>
      <div class="social-links">
      <a href="https://github.com/DFW-Dev" target="_blank">
      <v-btn icon>
        <v-icon color="white" small>fab fa-github</v-icon>
      </v-btn>
      </a>
      <a href="https://linkedin.com/company/dfwdev" target="_blank">
      <v-btn icon>
        <v-icon color="white" small>fab fa-linkedin</v-icon>
      </v-btn>
      </a>
      <a href="https://facebook.com/DFWDev" target="_blank">
      <v-btn icon>
        <v-icon color="white" small>fab fa-facebook</v-icon>
      </v-btn>
      </a>
      <a href="https://www.instagram.com/dfwdev/" target="_blank">
      <v-btn icon>
        <v-icon color="white" small>fab fa-instagram</v-icon>
      </v-btn>
      </a>
      <a href="https://twitter.com/devdfw" target="_blank">
      <v-btn icon>
        <v-icon color="white" small>fab fa-twitter</v-icon>
      </v-btn>
      </a>
      </div>
      <v-spacer></v-spacer>
      
      <v-btn icon class="tx-icon-wrap">
        <img 
            src="../assets/img/txIcon.svg"
            height="25"
          />          
      </v-btn>
      <b class="subtitle-1">Made in Dallas, TX USA</b>  
      </v-card-title>

      <v-card-text class="py-2 white--text text-center">
       &copy; {{ new Date().getFullYear() }} — <strong>DFW Dev All Rights Reserved</strong>
      </v-card-text>
    </v-card>
  </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      navBelowFold: false,
      drawer: false,
      clipped: false,
      fixed: false,
      items: [
        { icon: "fa-home", title: "Home", to: "/" },
        { icon: "fa-concierge-bell", title: "Services", to: "/services" },
        { icon: "fa-address-card", title: "Contact", to: "/contact" }, 
      ],
      title: 'Experienced Web and Software Developers in DFW Texas'
    }
  },
  methods: {
    handleScroll: function(event) {
      if (window.pageYOffset > 150) {
        this.navBelowFold = true
      } else {
        this.navBelowFold = false
      }
    }
  }
}
</script>
<style>
.v-toolbar__content {
    animation: fadeIn ease 2s;
    -webkit-animation: fadeIn ease 2s;
    -moz-animation: fadeIn ease 2s;
    -o-animation: fadeIn ease 2s;
    -ms-animation: fadeIn ease 2s;
}
.app-bar-custom a{
  text-decoration: none;
}
.no-padding{
padding: 0px!important;
}
.logo{
  max-width: 100%;
  height: 35px;
}
.fa-bars{
  color: #fff!important;
}
.v-icon{
  color: #fff!important;
}
.v-list-item__content{
  color: #fff!important;
}
.v-list-item__subtitle{
  color : #fff!important;
}
.v-navigation-drawer{
  color: #fff!important;
  background-image: url("../assets/img/black-twill.png");
  background-color: #37474F!important;
  background-repeat: repeat;
}
.v-navigation-drawer a{
  color: #fff!important;
}
.bottom-contact{
  color: #fff!important;
}
.bottom-contact b{
  color: #76FF03;
}
.bottom-contact-btn{
  color: #fff!important;
}
.bottom-contact-btn:hover{
  color: #E1F5FE!important;
}
.footer{
  color: #fff;
  background-color: #01579B!important;
  background-repeat: repeat;
}
.footer b{
  font-weight: normal;
  color: #fff;
}
.social-links a{
  text-decoration: none;
}
.tx-icon-wrap{
  cursor: default;
}
</style>