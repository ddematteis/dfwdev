<template>
<div class="pa-0">
    <v-container class="jumbo-bg pa-5" fill-height fluid >
    <v-row align="center" justify="center">
    <v-col cols="12" md="10" lg="7" xl="7" align="center"  justify="center">
       <v-container class="texture-layer elevation-1">
        <v-row>
        <v-col class="pa-10" cols="12" align="center" justify="center">
        <h1 class="display-1">Experienced Web App Developers and Designers</h1>
        <div class="subtitle-4 mt-5 jumbo-subtitle">
        We can help you reach more potential customers with a search engine optimized web presence,
        develop web applications from the ground up, and more.
        </div>
        </v-col>
        </v-row>
        </v-container>
    </v-col>
    </v-row>   
</v-container>
    <v-parallax
    :src="require('@/assets/img/dfwStock3.jpg')"
    id="bottom-content"
    
      >
    <v-container fill-height>
    <v-row align="center" justify="center">
    <v-col cols="12" md="10" lg="6" xl="5"  >
    <v-card class="pa-5 card content align-center text-left" flat color="white">
        <h2 class="font-weight-medium">Who is DFW Dev?</h2>
        <p class="mt-5">
        We are a group of experienced web application developers and graphic designers based in the Dallas-Fort Worth Metroplex. 
        With our expertise in bespoke software engineering, web development, graphic design, WordPress development, 
        and digital marketing/SEO services we can help businesses of any size with all of their web development needs. 
        </p>
        <v-btn color="orange darken-4" 
          to="/services#top"
          >
          Our Services
          </v-btn>
    </v-card>
    </v-col>
    <v-col cols="12" md="10" lg="6" xl="4"  align="center" class="hidden-md-and-down">
          <v-responsive>
          <img 
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
            class="no-round d-flex pa-2 content footer-sheet"
            width="100%"
            color="white"
            style="border-top: 5px solid #1565C0!important;"
          >
          <v-container class="text-center align-center justify-center">
          <v-row >
            
          <v-col cols="12" sm="12" md="6" xl="4" >
          <v-card
            color="pa-10 blue darken-3"
            tile
            hover
            class="service-card"
            to="/services/web-development"
          >
            
              <div>
                <v-card-title
                  class="headline"
                >Web Development</v-card-title>

                <v-card-text class="body-1" align="left">
                 We are expert software engineers with
                 18 years of experience. If you need 
                 software developed for your business we
                 can provide white label software development
                 services to help solve your business problems. 
                 We can work with PHP, Core, Go, Vue, Angular, 
                 React, and more.   
                </v-card-text> 
            </div>
          </v-card> 
          </v-col>
          <v-col cols="12" sm="12" md="6" xl="4" >
          <v-card
            color="pa-10 blue darken-3"
            tile
            hover
            class="service-card"
            to="/services/graphic-design/website-design"
          >
            
              <div>
                <v-card-title
                  class="headline"
                >Web Design</v-card-title>

                <v-card-text class="body-1" align="left">
                 If you are starting a business or have an
                 existing business, now more than ever, having an
                 effective web presence is a crucial component of success. 
                 We can help you through the process of building a website and
                 helping customers find your business.     
                </v-card-text> 
          </div>
          </v-card>   
          </v-col> 
          <v-col cols="12" sm="12" md="6" xl="4" >
          <v-card
            color="pa-10 blue darken-3"
            tile
            hover
            class="service-card"
            to="/services/agency-overflow"
          >
            
              <div>
                <v-card-title
                  class="headline"
                >Agency Overflow</v-card-title>

                <v-card-text class="body-1" align="left">
                 We provide reliable agency services for web development
                 and marketing agencies. Our experience with a variety of
                 software stacks and apis can allieviate some of your workload
                 and help you focus on other things.     
                </v-card-text> 
          </div>
          </v-card>   
          </v-col> 
          <v-col cols="12" sm="12" md="6" xl="4" >
          <v-card
            color="pa-10 blue darken-3"
            tile
            hover
            class="service-card"
            to="/services/graphic-design/logo-design"
          >
            
              <div>
                <v-card-title
                  class="headline"
                >Logo Design</v-card-title>

                <v-card-text class="body-1" align="left">
                 Get a logo that is custom designed
                 to reflect your brand.  
                </v-card-text> 
          </div>
          </v-card>   
          </v-col> 
          <v-col cols="12" sm="12" md="6" xl="4" >
          <v-card
            color="pa-10 blue darken-3"
            tile
            hover
            class="service-card"
            to="/services/graphic-design"
          >
            
              <div>
                <v-card-title
                  class="headline"
                >Graphic Design</v-card-title>

                <v-card-text class="body-1" align="left">
                 We can provide graphic design services which include
                 web design, brochure design, UI design, and more.     
                </v-card-text> 
          </div>
          </v-card>   
          </v-col> 
          <v-col cols="12" sm="12" md="6" xl="4" >
          <v-card
            color="pa-10 blue darken-3"
            tile
            hover
            class="service-card"
            to="/services/graphic-design/presentations"
          >
            
              <div>
                <v-card-title
                  class="headline"
                >Brochure and Flier Design</v-card-title>

                <v-card-text class="body-1" align="left">
                 We can help you improve your business's 
                 rank on search engine which helps customers
                 find you online. We can do technical SEO on your web
                 presence and provide copywriting services.     
                </v-card-text> 
          </div>
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
      title: 'Expert Web and Software Developers in DFW Texas',
      meta: [
        { hid: 'description', name: 'description', content: 'Based in DFW, we can build anything from small business websites to custom software.'}

      ]
    }
  },
  
  components: {
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
.jumbo-bg{
    /*background-color: linear-gradient( #1565C0, #01579B);*/
    background: linear-gradient(-45deg, #0D47A1, #0D47A1, #1E88E5, #42A5F5);
    animation: gradient 5s ease infinite;
    height: 600px;
    border-bottom: 10px solid #42A5F5;
}
.texture-layer{
    background: url("../assets/img/60-lines.png");
    border: dashed 1px #76FF03;
    border-radius: 20px;
    animation: fadeIn ease 3s;
    -webkit-animation: fadeIn ease 3s;
    -moz-animation: fadeIn ease 3s;
    -o-animation: fadeIn ease 3s;
    -ms-animation: fadeIn ease 3s;
}
@keyframes fadeIn {
0% {opacity:0;}
100% {opacity:1;}
}

@-moz-keyframes fadeIn {
0% {opacity:0;}
100% {opacity:1;}
}

@-webkit-keyframes fadeIn {
0% {opacity:0;}
100% {opacity:1;}
}

@-o-keyframes fadeIn {
0% {opacity:0;}
100% {opacity:1;}
}

@-ms-keyframes fadeIn {
0% {opacity:0;}
100% {opacity:1;}
}
.jumbo-bg h1{
    color: #E1F5FE;
    text-shadow: 1px 1px #000000;
}
.jumbo-bg h2{
    color: #fff;
}
.jumbo-subtitle{
    color: #76FF03;
}
@media (min-width: 768px){
    .jumbo-bg{
        height: 900px;
    }
}
.v-parallax__content{
  background: rgba(144,202,249,0.3)!important;
}
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
.service-card{
  color: #fff!important;
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
