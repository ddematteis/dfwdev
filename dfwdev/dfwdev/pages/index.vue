<template>
<div>
  <v-row class="d-flex flex-columnt" align="center" justify="center" id="get-quote">
    <JumboHome />
  </v-row>
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
          <v-container class="diag-content" >
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
            src="../assets/img/content-stock3.svg"
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
          <h2 class="font-weight-medium">Why Work With DfwDev?</h2>
          <p>
          Whether you are a small business owner needing a website or an agency needing help with overflow; we can help. 
          Our pragmatic approach to technical problems lets us offer the right solutions to help make your project a success.
          </p>
          <br/>
          
          <v-btn color="orange darken-4"
          @click="$vuetify.goTo('#get-quote')" 
          >
          Request a Quote
          </v-btn>
          </v-card>
          </v-col>
          </v-row>
          </v-container>
          </v-sheet>
          

</div>
</template>

<script>
import JumboHome from "~/components/JumboHome.vue";

export default {
  components: {
    JumboHome
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
  overflow: hidden;
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
  background: rgba(232,245,233,0.90)!important;
}
.content{
  color: #000!important;
}
.v-btn{
  color: #fff!important;
}
</style>
