<template>
<div class="pa-0">
    <Jumbotron />
  
    <v-parallax
    :src="require('@/assets/img/city-stock.jpg')"
    id="bottom-content"
      >
    <v-container fill-height>
    <v-row align="center" justify="center">
    <v-col cols="12" md="10" lg="6" xl="6"  justify="center">
    <v-card class="pa-5 card content align-center text-center" flat color="white">
        <h2 class="font-weight-medium">Who is DFW Dev?</h2>
        <p class="mt-5">
        We are a group of highly experienced web and software developers based in the Dallas-Fort Worth Metroplex. 
        We specialize in providing a search engine friendly web presence for small and large businesses. 
        </p>
    </v-card>
    </v-col>
    <v-col align="center" class="hidden-md-and-down">
          <v-responsive>
          <img class="rounded" 
            src="../assets/img/txBig.svg"
            :elevation="1"
            height="300"
          />
          </v-responsive>
          </v-col> 
     </v-row>   
     
    </v-container>
      </v-parallax>  

         

            <v-sheet
            tile="tile"
            :elevation="3"
            class="no-round d-flex pa-2 content"
            height="400"
            width="100%"
            color="blue lighten-5"
          >
          <v-container class="text-center align-center justify-center">
          <v-row >
          <v-col align="center" class="hidden-md-and-down">
          <v-responsive>
          <img class="rounded" 
            src="../assets/img/content-stock2.svg"
            :elevation="1"
            height="300"
          />
          </v-responsive>
          </v-col>  
          <v-col class="justify-center text-center align-center" style="margin-top: 50px;">
          <v-card class="pa-3 card content xs11 align-center text-center" flat color="blue lighten-5">
          <h2 class="font-weight-medium">Why Work With DFW Dev?</h2>
          <p class="mt-5">
          We have been building web applications and websites for 15 years and are based in sunny (and windy) Dallas, Texas. Our experience 
          and pragmatic approach to technical problems allows us to offer the right solutions to help make your project a success. 
          </p>
          <br/>
          
          <v-btn color="orange darken-4" 
          to="/services#services-top"
          >
          View Our Services
          </v-btn>
          </v-card>
          </v-col>
          </v-row>
          </v-container>
          </v-sheet>
          

</div>
</template>

<script>
import Jumbotron from "~/components/Jumbotron.vue";

export default {
  head(){
    return {
      title: 'Experienced Web and Software Developers in DFW Texas',
      meta: [
        { hid: 'description', name: 'description', content: 'Based in DFW, we can build anything from small business websites to custom software.'}

      ]
    }
  },
  
  components: {
    Jumbotron
  },

  data: () => (
    {
    contentStock: require('~/assets/img/jumboStock.svg'),
    name: "",
    result: " "
  }),

  
};
</script>

<style>
.no-round{
  border-radius: 0px;
}
.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.result {
  height: 30px;
  line-height: 30px;
}
.diag-bg{
  background: url('../assets/img/bottom-stock.jpg');
  background-position: center;
  overflow: hidden!important;
  padding: 0px;
  margin: 0px;
}
/*div on top of stock bg rotated Y-axis to -10 degrees */
.diag-box{
  background: rgba(100,221,23,0.73);
  transform: skewY(-10deg);
  height: 300px;
}
/*rotating the div causes the content to be skewed, 
counter this by skewing content back to 10 deg  */
.skew-reset{
  transform: skewY(10deg);
  margin-top: 0;
}
.diag-content{
  margin-top: 50px;
}
.card{
  background: rgba(227,242,253,0.90)!important;
}
.card h2{
  color: #01579B;
}
.content{
  color: #000!important;
}
.v-btn{
  color: #fff!important;
}
</style>
