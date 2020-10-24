<template>
  <v-app>
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
            src="../assets/img/logo.svg"
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
      elevate-on-scroll 
      class="mb-0 app-bar-custom"
    >
    <v-container>
      <v-row>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="hidden-md-and-up"/>
      
      <v-toolbar-title class="mt-2">
      <router-link to="/">  
      <img  class="logo"
            src="../assets/img/logo.svg"
            
          />
      </router-link>    
      </v-toolbar-title>
      <v-toolbar-items class="ml-10 hidden-sm-and-down">
        <v-btn color="white" text to="/" exact>Home</v-btn>
        <v-btn color="white" text to="/services" exact>Services</v-btn>
        <v-btn color="white" text to="/projects" exact>Projects</v-btn>
        <v-btn color="white" text to="/contact" exact>Contact</v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
      <div class="social-links hidden-sm-and-down">
      <a href="https://github.com/DFW-Dev" target="_blank">
      <v-btn icon>
        <v-icon medium>fab fa-github</v-icon>
      </v-btn>
      </a>
      <a href="https://linkedin.com/company/dfwdev" target="_blank">
      <v-btn icon>
        <v-icon medium>fab fa-linkedin</v-icon>
      </v-btn>
      </a>
      <a href="https://facebook.com/DFWDev" target="_blank">
      <v-btn icon>
        <v-icon medium>fab fa-facebook</v-icon>
      </v-btn>
      </a>
      <a href="https://twitter.com/devdfw" target="_blank">
      <v-btn icon>
        <v-icon medium>fab fa-twitter</v-icon>
      </v-btn>
      </a>
      <!--
      <v-btn color="white" text to="/login" exact>Login</v-btn>
      //-->
      </div>
      </v-row>
      </v-container>
    </v-app-bar>
      <v-container fluid class="no-padding" style="width: 100%!important;padding:0px!important;">
        <v-slide-y-transition mode="out-in">
          <nuxt />
        </v-slide-y-transition>
      </v-container>
   









    <v-footer
    :fixed="fixed"
    padless
  >
    <v-card
      class="flex footer"
      flat
      tile
    >

      <v-card-title>
      <div class="social-links">
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
      drawer: false,
      clipped: false,
      fixed: false,
      items: [
        { icon: "fa-home", title: "Home", to: "/" },
        { icon: "fa-concierge-bell", title: "Services", to: "/services" },
        { icon: "fa-sitemap", title: "Projects", to: "/projects" },
        { icon: "fa-address-card", title: "Contact", to: "/contact" }, 
      ],
      title: 'Experienced Web and Software Developers in DFW Texas'
    }
  }
}
</script>
<style>
.app-bar-custom{
  background: #1565C0 url("https://www.transparenttextures.com/patterns/60-lines.png") repeat!important;
}
.app-bar-custom a{
  text-decoration: none;
}
.v-application--wrap{
  width: 100%!important;
  padding: 0px;
}
.no-padding{
padding: 0px!important;
}
.logo{
  max-width: 100%;
  height: 35px;
}
.drawer{
  color: #fff;
  background-image: url("../assets/img/black-twill.png");
  background-color: #37474F!important;
  background-repeat: repeat;
}
.footer{
  color: #fff;
  background-image: url("../assets/img/black-twill.png");
  background-color: #3E2723!important;
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