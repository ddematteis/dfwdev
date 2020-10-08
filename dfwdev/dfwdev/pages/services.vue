<template>
<div>
<v-sheet class="align-center" color="blue lighten-5" height="200" style="text-align: center;">
<h1 class="page-title">Services We Offer</h1>
</v-sheet>
<v-sheet
            tile="tile"
            :elevation="3"
            class="no-round d-flex pa-2 content"
            id="bottom-content"
            width="100%"
            color="white"
          >

          
          <v-container>
          <v-row > 
          <v-col class="justify-center text-center align-center" style="margin-top: 50px;">
          <v-card class="pa-3 card content xs11 align-center text-center" flat color="white">
          <h2 class="font-weight-medium">Small Business Sites Starting at 150/mo</h2>
          <p>
          We can build you a great looking website to advertise your small business. Need more than a website?
          We can help with that too. 
          </p>
          </v-card>
          </v-col>
          <v-col align="center" class="hidden-md-and-down">
          <v-responsive>
          <img class="rounded" 
            src="../assets/img/content-stock4.svg"
            :elevation="1"
            height="300"
          />
          </v-responsive>
          </v-col> 
          </v-row>

          <!-- start lines //-->
          <v-container fluid >
          <div class="lines-wrapper">
          <v-row> 
          <v-col class="divider-col pb-0" >
          <div class="lines-top"></div>
          </v-col>
          </v-row >
          <v-row > 
          <v-col class="pt-0 pb-0">
          <div class="lines-bottom"></div>
          </v-col>
          </v-row>
          </div>
          </v-container>
          <!-- end lines //-->

          <v-row >
          <v-col align="center" class="hidden-md-and-down">
          <v-responsive>
          <img class="rounded" 
            src="../assets/img/content-stock5.svg"
            :elevation="1"
            height="300"
          />
          </v-responsive>
          </v-col>  
          <v-col class="justify-center text-center align-center" style="margin-top: 50px;">
          <v-card class="pa-3 card content xs11 align-center text-center" flat color="white">
          <h2 class="font-weight-medium">Custom Web Applications</h2>
          <p>
          Maybe you need to automate some business logic, or maybe you have an idea for a new app. 
          Whatever it may be, we have the ability to build full scale applications from the ground
          up on a variety of software stacks. 
          </p>
          </v-card>
          </v-col>
          </v-row>

          <!-- start lines //-->
          <v-container fluid>
          <div class="lines-wrapper">
          <v-row > 
          <v-col class="divider-col pt-0 pb-0">
          <div class="lines-top-mirror"></div>
          </v-col>
          </v-row >
          <v-row > 
          <v-col class="pt-0 pb-0">
          <div class="lines-bottom-mirror"></div>
          </v-col>
          </v-row>
          </div>
          </v-container>
          <!-- end lines //-->

          <v-row >
          <v-col class="justify-center text-center align-center" style="margin-top: 50px;">
          <v-card class="pa-3 card content xs11 align-center text-center" flat color="white">
          <h2 class="font-weight-medium">Overflow Services</h2>
          <p>
          We provide discreet and reliable overflow services to agencies that need some extra help on projects.
          Our experience on a variety of software stacks and open source software like Wordpress and Joomla 
          can help alleviate some of your workload; allowing you to focus on other things.    
          </p>
          </v-card>
          </v-col>
          <v-col align="center" class="hidden-md-and-down">
          <v-responsive>
          <img class="rounded" 
            src="../assets/img/content-stock6.svg"
            :elevation="1"
            height="300"
          />
          </v-responsive>
          </v-col>  
          </v-row>
          
          <!-- start lines //-->
          <v-container fluid>
          <div class="lines-wrapper">
          <v-row > 
          <v-col class="divider-col pt-0 pb-0" >
          <div class="lines-top"></div>
          </v-col>
          </v-row >
          <v-row > 
          <v-col class="pt-0 pb-0">
          <div class="lines-bottom"></div>
          </v-col>
          </v-row>
          </div>
          </v-container>
          <!-- end lines //-->

          <v-row >
          <v-col align="center" class="hidden-md-and-down">
          <v-responsive>
          <img class="rounded" 
            src="../assets/img/content-stock7.svg"
            :elevation="1"
            height="300"
          />
          </v-responsive>
          </v-col>  
          <v-col class="justify-center text-center align-center" style="margin-top: 50px;">
          <v-card class="pa-3 card content xs11 align-center text-center" flat color="white">
          <h2 class="font-weight-medium">E-commerce (Online Stores)</h2>
          <p>
          We can help you set up an online store to sell your products. We can use any of the existing
          e-commerce solutions like Shopify, Woocommerce or if you have more advanced needs we can build
          custom solutions as well. Our Wordpress packages start at 300/mo and includes support and setup.   
          </p>
          </v-card>
          </v-col>
          </v-row>

          </v-container>
    </v-sheet>
          </div>
</template>
<script>
export default {
    layout: 'default',
    head(){
    return {
      title: 'Our Services',
      meta: [
        { hid: 'description', name: 'description', content: 'We offer a wide range of web development services. We can help you with small-business websites, custom web applications, agency overflow services, and online stores.'}

      ]
    }
  },

}
</script>
<style>
.page-title{
    color: #0D47A1;
    position: relative;
    top: 100px;
}
.content{
    color: #000!important;
}
.lines-wrapper{
  padding-left: 20%;
}
.lines-top{
    width: 60%;
    height: 50px;
    border-left: 3px dashed #76FF03;
    border-bottom: 3px dashed #76FF03;
}
.lines-bottom{
    width: 60%;
    height: 50px;
    border-right: 3px dashed #76FF03;
}
/*reversed */
.lines-top-mirror{
    width: 60%;
    height: 50px;
    border-right: 3px dashed #76FF03;
    border-bottom: 3px dashed #76FF03;
}
.lines-bottom-mirror{
    width: 60%;
    height: 50px;
    border-left: 3px dashed #76FF03;
}
</style>