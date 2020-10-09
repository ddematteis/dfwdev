<template>
<div class="pa-0">
    <JumboHome />
  
    <v-parallax
    :src="require('@/assets/img/bottom-stock.jpg')"
    id="bottom-content"
      >
      <v-container>
      <v-row
      align="center"
      justify="center"
      >
      <v-col
        class="text-center"
        cols="12"
        >
        <v-card class="pa-3 card content" >
          <h3 align="center" class="font-weight-medium">Who is DFW Dev?</h3>
          <p align="center">
          We are a network of highly experienced developers based in the Dallas-Fort Worth Metroplex. We specialize in building SEO ready custom web applications
          and websites to help you meet your business needs. 
          </p>
          </v-card>
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
          <p>
          We are expert web and software developers with 15 years of experience. Our pragmatic 
          approach to technical problems lets us offer the right solutions to help make your 
          project a success.
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
  head(){
    return {
      title: 'We can help you with your web projects',
      meta: [
        { hid: 'description', name: 'description', content: 'Based in DFW, we can build anything from small business websites to custom software.'}

      ]
    }
  },
  
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
.content{
  color: #000!important;
}
.v-btn{
  color: #fff!important;
}
</style>
