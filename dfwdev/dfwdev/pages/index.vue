<template>
<div>
  <v-row class="d-flex flex-columnt" align="center" justify="center" >
    <JumboRequestQuote />
  </v-row>
 <!---- <v-row >
  <v-card   min-width="100%"
            color="white"
            class="text-center"
          >
            <v-card-title class="headline justify-center">Why Work With DFWDev?</v-card-title>
            <v-container>
            <v-row>
            <v-col style="background: #ff0000;text-align: center;">
            <v-card-text>
            
            Whether you are a small business owner needing a website or a web agency needing help with overflow we can help. 
            Our pragmatic approach helps us offer the right solution to help make your project a success.
            
            </v-card-text>
            </v-col>
            <v-col>
            <img class="vector-stock elevation-1" 
            src="../assets/img/jumboStock.svg"
            :elevation="1"
            />
            </v-col>
            </v-row>
            </v-container>
            <v-card-actions class="justify-center">
              <v-btn text>Request a Consultation</v-btn>
            </v-card-actions>
  </v-card>
  </v-row>
  //-->

          <v-sheet
            tile="tile"
            :elevation="3"
            class="no-round d-flex pa-2"
            height="400"
            width="100%"
            color="blue-grey lighten-5"
            style="padding: 0px!important;"
            fluid
          >

          <div class="diag-bg" style="padding: 0px; width:100%;">
          <div class="diag-box">
          <v-container class="diag-content">
          <v-row align="center" class="skew-reset" >
          <v-col >
          <v-card class="pa-3 card content xs11" >
          <h2 align="center" class="font-weight-medium">Who is DFWDev?</h2>
          <p align="center">
          Based in the Dallas-Fort Worth Metroplex, we are a small network of highly experienced professionals 
          with the ability to solve a wide array of your technical problems. We specialize in custom web application
          development. 
          </p>
          </v-card>
          </v-col>
          <v-col align="center" class="hidden-md-and-down">
          <v-responsive>
          <img class=" elevation-1 rounded" 
            src="../assets/img/jumboStock.svg"
            :elevation="1"
            height="300"
          />
          </v-responsive>
          </v-col>
          </v-row>
          </v-container>
          </div>
          </div>

          </v-sheet>

            <v-sheet
            tile="tile"
            :elevation="3"
            class="no-round d-flex pa-2 content"
            id="bottom-content"
            height="400"
            width="100%"
            color="blue lighten-5"
          >
          <v-container class="text-center align-center justify-center">
          <v-row  >
          <v-col align="center" class="hidden-md-and-down">
          <v-responsive>
          <img class=" elevation-1 rounded" 
            src="../assets/img/jumboStock.svg"
            :elevation="1"
            height="300"
          />
          </v-responsive>
          </v-col>  
          <v-col >
          <v-card class="pa-3 card content xs11" flat color="blue lighten-5">
          <h2 align="center" class="font-weight-medium">Who is DFWDev?</h2>
          <p align="center">
          Based in the Dallas-Fort Worth Metroplex, we are a small network of highly experienced professionals 
          with the ability to solve a wide array of your technical problems. We specialize in custom web application
          development. 
          </p>
          </v-card>
          </v-col>
          </v-row>
          </v-container>
          </v-sheet>
          

</div>
</template>

<script>
import JumboRequestQuote from "~/components/JumboRequestQuote.vue";

export default {
  components: {
    JumboRequestQuote
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
.skew-reset{
  transform: skewY(30deg);
  margin-top: 0;
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
  overflow: hidden;
  padding: 0px;
  margin: 0px;
}
.diag-box{
  background: rgba(100,221,23,0.73);
  transform: skewY(-30deg);
  height: 300px;
}
.diag-content{
  margin-top: 50px;
}
.card{
  background: rgba(232,245,233,0.90)!important;
}
.content{
  color: #000!important;
}
</style>
