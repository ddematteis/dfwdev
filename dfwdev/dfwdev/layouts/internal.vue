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
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="hidden-md-and-up"/>
      
      <v-toolbar-title >
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
      <a href="https://github.com/ddematteis/dfwdev/tree/master/dfwdev" target="_blank">
      <v-tooltip bottom color="green">
        <template v-slot:activator="{ on, attrs }">
      <v-icon x-large class="github-icon" v-bind="attrs"
            v-on="on">mdi-github</v-icon>
      </template>
        <span>View this site's code on github</span>
      </v-tooltip>
      </a>
    </v-app-bar>

      <v-container fluid class="no-padding">
        <v-slide-y-transition mode="out-in">
          <nuxt />
        </v-slide-y-transition>
      </v-container>
    
    <v-footer :fixed="fixed" class="d-flex justify-center footer">
      <div style="margin:10px">
        <div>
          <router-link to="/" tar>
          <img
            src="../assets/img/logo.png"
            height="32"
            style="vertical-align:middle;margin-right:5px;"
          />
          </router-link>
         <b> &copy; {{ new Date().getFullYear() }} DFWDev All Rights Reserved </b>
        </div>
      </div>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  theme:{
      light: true,
      dark: false,
    },
  data () {
    return {
      drawer: false,
      clipped: false,
      fixed: false,
      items: [
        { icon: "mdi-home", title: "Home", to: "/" },
        { icon: "mdi-chart-bubble", title: "Services", to: "/services" },
        { icon: "mdi-contacts", title: "Contact", to: "/contact" }, 
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
</style>