<template>
<div class="root-div">
<!-- Small Screens (iphone, galaxy, etc.)//-->
<v-sheet class="jumbo-bg-sm hidden-md-and-up" > 
<v-container fluid class="fill-height" >
<v-row >
<v-col class="pa-5 pt-5">
<div id="jumbo-content1">    
<div id="stepper-header">    
<h1 class="display-1">We are Experienced Web and Software Developers</h1>
<h2 class="subtitle-1 mt-5">
Small business websites, custom software development, online stores, DFW Dev can provide solutions. 
Browse our <router-link to="/services">services</router-link> or request a quote to get started.
</h2>
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
<v-container>
<div id="jumbo-content2">  
<div id="stepper-header">    
<h1 class="display-2">We are Experienced Web and Software Developers</h1>
<h2 class="subtitle-1 mt-10">
Small business websites, custom software development, online stores, DFW Dev can provide solutions. 
Browse our <router-link to="/services">services</router-link> or request a quote to get started.
</h2>
</div>
<QuoteStepper/>
</div>
</v-container>
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
<!-- End Med Screens //-->

<!-- Large Screens //-->
<v-sheet class="jumbo-bg-lg hidden-md-and-down " > 
<v-container class="fill-height text-center" >
<v-row align="center" justify="center">
<v-col >
<div id="jumbo-content3">  
<div id="stepper-header">    
<h1 class="display-2">We are Experienced Web and Software Developers</h1>
<h2 class="subtitle-1">
Small business websites, custom software development, online stores, DFW Dev can provide solutions. 
Browse our <router-link to="/services">services</router-link> or request a quote to get started.
</h2>
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

<style scoped>
.root-div{
    padding: none;
    min-width: 100%;
}
.root-div h1{
    color: #76FF03;
}
.root-div h2{
    color: #fff;
}
.root-div h2 a{
    color: #E65100;
    text-decoration: none;
}
.root-div h2 a:hover{
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
    height: 600px;
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
