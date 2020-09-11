<template>
<div style="width:100%;">
    <div class="jumbotron ">
    <v-container fill-height text-center >
    <v-row class="hidden-sm-and-up">
    <v-col>
        
         <h3 class="display-2">We Can Help You With Your Web Projects</h3>
    <h4 class="subtitle-1">Any kind of web project from simple websites to custom business applications. </h4>
    <br/>
    <!--
    <v-form center>
    <v-container fluid>
    <v-layout row>
    <v-flex xs8>
      <v-text-field
            label="Create a Room"
            solo
          >
    </v-text-field>
    </v-flex>
    <v-flex xs2>
     <v-btn color="error" large>Create Room</v-btn>
    </v-flex>
    </v-layout> 
    </v-container>
    </v-form>
//-->
    </v-col>
    </v-row>

    <v-row class="hidden-xs-only">
    <v-col class="sm-8" align-center justify-center>
        
    <h3 class="display-2">We Can Help You With Your Web Projects</h3>
    <h4 class="subtitle-1">From simple websites to custom business applications DFWDev has a solution. Browse our Services or request a quote to get started.</h4>
    <br/>
    </v-col>
    <v-col>
    <v-responsive>
    <img class="vector-stock elevation-1 rounded" 
            src="../assets/img/jumboStock.svg"
            :elevation="1"
          />
    </v-responsive>
    </v-col>
    </v-row>
    </v-container>
    <transition name="custom-classes-transition" enter-active-class="animate__bounce">
    <v-btn class="mx-2 animate__animated animate__bounce" small fab dark color="white" style="position: relative;bottom:25px;"
    @click="$vuetify.goTo('#bottom-content')"
    >
    <v-icon color="brown darken-3">mdi-arrow-down</v-icon>
    </v-btn>
    </transition>
    </div>
</div>
</template>

<script>
import AppLogo from "~/components/AppLogo.vue";

export default {
  components: {}
  };
</script>

<style >
.vector-stock{
    max-width: 100%;
    height: 300px;
}
.wrapper-div{
    padding-top: 0px;
    width: 100%;
}
.top-spacer{
    width: 100%;
    height: 25px;
    background: #1565C0;
}
.jumbotron{
    width: 100%;
    height: 800px;
    background: linear-gradient( #1565C0, #29B6F6);
    text-align: center;
	
}
.jumbotron h3, h4{
    color: #fff;
}
.rounded{
    border-radius: 0 20px 0 20px;
}
@keyframes bounce{
    0% { transform: translateY(0)!important; }
    100% { transform: translateY (-50px)!important; }
}
.bounce{
    animation: bounce 2s;
    animation-direction: alternate;
    animation-iteration-count: infinite;
}
</style>
