<template>
<div class="root-div" >
<!-- Changing height based on screen size this is a lazy quick way of doing it, needs a redo later. //-->
<!-- Small Screens (iphone, galaxy, etc.)//-->
<v-sheet class="jumbo-bg-sm hidden-md-and-up" > 
<v-container fluid class="fill-height" >
<v-row >
<v-col class="pa-10">
<div id="jumbo-content1">    
<div id="stepper-header">    
<h3 class="display-2">We Can Help You With Your Web Projects</h3>
<h4 class="subtitle-1">From simple websites to custom business applications DFWDev has a solution. Browse our <router-link to="/services">services</router-link> or request a quote to get started.</h4>
</div>
<QuoteStepper/>
</div>
</v-col>
</v-row>

</v-container>
</v-sheet>
<!-- End Small Screens //-->

<!-- Med Screens (tablets)//-->
<v-sheet class="jumbo-bg-md hidden-lg-and-up hidden-sm-and-down" > 
<v-container fluid class="fill-height" >
<v-row >
<v-col >
<v-row >
<v-col class="pa-10">
<div id="jumbo-content2">  
<div id="stepper-header">    
<h3 class="display-2">We Can Help You With Your Web Projects</h3>
<h4 class="subtitle-1">From simple websites to custom business applications DFWDev has a solution. Browse our <router-link to="/services">services</router-link> or request a quote to get started.</h4>
</div>
<QuoteStepper/>
</div>
</v-col>
</v-row>
</v-col>
</v-row>
</v-container>
</v-sheet>
<!-- End Med Screens //-->

<!-- Large Screens //-->
<v-sheet class="jumbo-bg-lg hidden-md-and-down " > 
<v-container class="fill-height text-center" >
<v-row align="center" justify="center">
<v-col >
<div id="jumbo-content3">  
<div id="stepper-header">    
<h3 class="display-2">We Can Help You With Your Web Projects</h3>
<h4 class="subtitle-1">From simple websites to custom business applications DFWDev has a solution. Browse our <router-link to="/services">services</router-link> or request a quote to get started.</h4>
</div>
<QuoteStepper/>
</div>
</v-col>
<v-col >
<v-responsive>
    <img class="vector-stock elevation-1 rounded" 
            src="../assets/img/jumbo-stock.svg"
            :elevation="1"
          />
    </v-responsive>
</v-col>
</v-row>
</v-container>
</v-sheet>
<!-- End Large Screens //-->
<!-- Bottom Button //-->
<v-container fluid style="padding: 0px;margin-top: 0px;">
<v-row>
<v-col class="jumbo-bottom-border pt-0" align="center" justify="center">
<v-btn class="mx-auto scroll-btn" small fab color="white"
    @click="$vuetify.goTo('#bottom-content')"
    >
    <v-icon color="brown darken-3">mdi-arrow-down</v-icon>
    </v-btn>
</v-col>
</v-row>
</v-container>
<!-- End Bottom Button //-->
</div>
</template>
<script>
import QuoteStepper from "~/components/QuoteStepper.vue";
export default {
  components: {
    QuoteStepper
  },

}
</script>
<style>
.root-div{
    padding: none;
    min-width: 100%;
}
.root-div h3{
    color: #fff;
}
.root-div h4{
    color: #fff;
}
.root-div h4 a{
    color: #42A5F5;
    text-decoration: none;
}
.root-div h4 a:active{
    color: #42A5F5;
    text-decoration: none;
}
.root-div h4 a:hover{
    color: #90CAF9;
    text-decoration: none;
}
.jumbo-bg-lg{
    height: 800px;
    background: linear-gradient( #1565C0, #01579B);
    text-align: center;
}
.jumbo-bg-md{
    height: 700px;
    background: linear-gradient( #1565C0, #01579B);
    text-align: center;
}
.jumbo-bg-sm{
    height: 500px;
    background: linear-gradient( #1565C0, #01579B);
    text-align: center;
}
.jumbo-stock{
    max-width: 100%;
    border-radius: 0 20px 0 20px;
}
.jumbo-bottom-border{
    height: 25px;
    width: 100%;
    background: #37474F;
}
.scroll-btn{
    position: relative;
    bottom: 10px;
}
.subtitle-1 a{
    color: #42A5F5;
}
.subtitle-1 a:active{
    color: #42A5F5;
}
.subtitle-1 a:hover{
    color: #fff;
}
</style>
