<template>
  <v-app>
    <v-navigation-drawer
      temporary
      v-model="drawer"
      :clipped="clipped"
      fixed
      app
      color="blue-grey darken-3"
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
      
      <a href="https://instagram.com/dfwdev" target="_blank">
      <v-btn icon>
        <v-icon small>fab fa-instagram</v-icon>
      </v-btn>
      </a>
      </v-container>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      color="blue darken-3" 
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
      <a href="https://instagram.com/dfwdev" target="_blank">
      <v-btn icon>
        <v-icon medium>fab fa-instagram</v-icon>
      </v-btn>
      </a>
      </div>
      </v-row>
      </v-container>
    </v-app-bar>
      <v-container fluid class="no-padding" style="width: 100%!important;padding:0px!important;">
        <v-slide-y-transition mode="out-in">
          <nuxt />
        </v-slide-y-transition>
      </v-container>
    
    <v-footer :fixed="fixed" class="d-flex justify-center footer">
      <div >
        <v-row class="justify-center align-center">
          <router-link to="/" tar>
          <img
            src="../assets/img/logo.svg"
            height="20"
            style="vertical-align:middle;margin-right:5px;"
          />
          </router-link>
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
      <a href="https://instagram.com/dfwdev" target="_blank">
      <v-btn icon>
        <v-icon small>fab fa-instagram</v-icon>
      </v-btn>
      </a>
      </div>
      </v-row>
      <v-row class="justify-center align-center mt-1">
         <b> &copy; {{ new Date().getFullYear() }} - DFW Dev All Rights Reserved </b>
      </v-row>
      </div>
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
        { icon: "fa-sitemap", title: "Services", to: "/services" },
        { icon: "fa-address-card", title: "Contact", to: "/contact" }, 
      ],
      title: 'DfwDev.com'
    }
  }
}
</script>
<style>
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
</style>