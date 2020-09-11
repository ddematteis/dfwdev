<template>
  <v-app>
    <v-navigation-drawer fixed :mini-variant="miniVariant" :clipped="clipped" v-model="drawer" app>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title"><img
            src="../assets/img/logo.png"
            height="35"
          />
          </v-list-item-title>
          <v-list-item-subtitle>Web Application Development</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item router :to="item.to" :key="i" v-for="(item, i) in items" exact>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>


    <v-app-bar fixed app :clipped-left="clipped" color="blue darken-3" elevate-on-scroll style="margin-bottom: 0px;">
    <v-app-bar-nav-icon color="white" class="hidden-md-and-up"  @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <!--
      <v-btn icon @click.stop="miniVariant = !miniVariant">
      <v-icon v-html="miniVariant ? 'mdi-chevron-right' : 'mdi-chevron-left'"></v-icon>
      </v-btn>
      <v-toolbar-title v-text="title"></v-toolbar-title>
      //-->
      <v-toolbar-title>
      <img  class="logo"
            src="../assets/img/logo.png"
            
          />
      </v-toolbar-title>
      <v-toolbar-items class="ml-10 hidden-sm-and-down">
        <v-btn color="white" text to="/" exact>Home</v-btn>
        <v-btn color="white" text to="/services" exact>Services</v-btn>
        <v-btn color="white" text to="/projects" exact>Projects</v-btn>
        <v-btn color="white" text to="/contact" exact>Contact</v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
      <v-toolbar-item >
      <v-icon x-large>mdi-github</v-icon>
      </v-toolbar-item>

    </v-app-bar>

    <v-content>
      <v-container fluid class="no-padding">
        <v-slide-y-transition mode="out-in">
          <nuxt />
        </v-slide-y-transition>
      </v-container>
    </v-content>
    <v-footer :fixed="fixed" class="d-flex justify-center footer">
      <div style="margin:10px">
        <div>
          <img
            src="../assets/img/logo.png"
            height="32"
            style="vertical-align:middle;margin-right:5px;"
          />
         <b> &copy; 2020 DFWDev All Rights Reserved </b>
        </div>
      </div>
    </v-footer>
  </v-app>
</template>
<style>
.no-padding{
padding: 0px!important;
}
.logo{
  max-width: 100%;
  height: 35px;
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
<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        { icon: "mdi-home", title: "Home", to: "/" },
        { icon: "mdi-chart-bubble", title: "About", to: "/about" },
        { icon: "mdi-contacts", title: "Contact", to: "/contact" },
        { icon: "mdi-message", title: "Post 1", to: "/posts/1" },
        { icon: "mdi-message", title: "Post 2", to: "/posts/2" },
        { icon: "mdi-message", title: "Post 3", to: "/posts/3" },
        { icon: "mdi-message", title: "Post 4", to: "/posts/4" },
        { icon: "mdi-message", title: "Post 5", to: "/posts/5" }
      ],
      miniVariant: false,
      right: true,
      title: "dfwdev"
    };
  }
};
</script>
