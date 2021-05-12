<template>
<div>
<v-sheet class="align-center half-bg" >
<v-container fill-height>
    
    <v-row>
    <v-col class="pl-0 pt-15">
    <h1 class="page-title display-2 mt-10" id="top">Whitelabel Development and Design for Agencies</h1>
    </v-col>
    <v-col cols="12"  class="pl-0">
    <v-breadcrumbs
      :items="items"
      large
      class="breadcrumbs"
    ></v-breadcrumbs>
    </v-col>
    </v-row>
        <!-- row //-->
          <v-row >
          <v-col cols="12" md="1" lg="1" xl="1">
          </v-col>     
          <!-- col 1 //-->   
          <v-col cols="12" md="10" lg="10" xl="10" class="mt-10">
          
          <v-card class="pa-10"  elevation="0">
          <v-divider></v-divider>
          <br/>
          <h2>Professional Services for Your Peace of Mind</h2>
          <p class="pt-5 subtitle-1">
            Leverage our years of experience to handle your projects for you while you handle your clients.  
            We can work with various frameworks, APIs, and programming languages. We can also do business card design, presentation design, fliers, logos, and more. 
          </p>
          <v-divider></v-divider>
          <br/>
          <h2>Full Privacy and Confidentiality</h2>
          <p class="pt-5 subtitle-1">
            We take confidentiality very seriously with any overflow services we provide. Calling our work yours is not only ok, it's expected. We will
            not put any of the work we do for you in any of our portfolios. Your clients will stay your clients and privacy is guaranteed. Our approach is entirely
            flexible and based upon the needs of your business and our involvement in the project will be controlled by you. 
          </p>
          <v-divider></v-divider>
          <p class="pt-5 subtitle-1">
            Have a project to discuss?
            <br/>
            <v-btn class="mt-2 bottom-contact-btn" color="light-blue lighten-1" 
            to="/contact"
            >
            Get in Touch
            </v-btn>  
          </p>
          </v-card>
        

          </v-col>
          <!-- end col 1 //-->
          <v-col cols="12" md="1" lg="1" xl="1">
          </v-col>  
          </v-row>
        <!-- end row//-->
          
    

          </v-container>
</v-sheet>
</div>
</template>
<script>
export default {
    layout: 'default',
    scrollToTop: true,
    head(){
    return {
      title: 'Services - Agency Overflow',
      meta: [
        { hid: 'description', name: 'description', content: 'We offer a wide range of web development services including: Small-business websites, custom web applications, agency overflow services, and online stores.'}

      ]
    }
  },
  data: () => ({
      items: [
        {
          text: 'Services',
          disabled: false,
          href: '/services',
        },
        {
          text: 'Whitelabel Development and Design for Agencies',
          disabled: true,
          href: '/services/agency-overflow',
        },
      ],
    }),
}

</script>
<style>
.breadcrumbs{
   padding: 0px;
   margin-left: 0px;  
}
.breadcrumbs a{
    color: #00B0FF;
}
.breadcrumbs a:hover{
    color: #fff;
}
.v-breadcrumbs{
    padding-left: 5px!important;
    
}
.v-breadcrumbs__item--disabled{
    color: #B0BEC5!important;
}
.v-breadcrumbs__divider{
    color: #00B0FF!important;
}
.half-bg{
    /*background-color: linear-gradient( #1565C0, #01579B);*/
    min-height:100%;
    background:linear-gradient(0deg, rgba(26, 35, 126, 0.8), rgba(26, 35, 126, 0.8)), url(../../assets/img/city-stock.jpg);
    background-size: cover;
    animation: gradient 5s ease infinite;
    background-size: 100% 450px;
    background-repeat: no-repeat;
}
.page-title{
    color: #FFF;

}
.blue-block{
  color: #fff!important;
}
.bottom-contact{
  color: #fff!important;
}
.bottom-contact b{
  color: #76FF03;
}
.bottom-contact-btn{
  color: #fff!important;
}
.bottom-contact-btn:hover{
  color: #E1F5FE!important;
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
    border-left: 3px dashed #03A9F4;
    border-bottom: 3px dashed #03A9F4;
}
.lines-bottom{
    width: 60%;
    height: 50px;
    border-right: 3px dashed #03A9F4;
}
/*reversed */
.lines-top-mirror{
    width: 60%;
    height: 50px;
    border-right: 3px dashed #03A9F4;
    border-bottom: 3px dashed #03A9F4;
}
.lines-bottom-mirror{
    width: 60%;
    height: 50px;
    border-left: 3px dashed #03A9F4;
}
.waves {
  position: relative;
  width: 100%;
  height: 15vh;
  margin-bottom: 0px;
  /*Fix for safari gap*/
  min-height: 100px;
  max-height: 150px;
}
/* Animation */
.parallax>use {
  animation: move-forever 25s cubic-bezier(.55, .5, .45, .5) infinite;
}
.parallax>use:nth-child(1) {
  animation-delay: -2s;
  animation-duration: 7s;
}
.parallax>use:nth-child(2) {
  animation-delay: -3s;
  animation-duration: 10s;
}
.parallax>use:nth-child(3) {
  animation-delay: -4s;
  animation-duration: 13s;
}
.parallax>use:nth-child(4) {
  animation-delay: -5s;
  animation-duration: 20s;
}
@keyframes move-forever {
  0% {
    transform: translate3d(-90px, 0, 0);
  }
  100% {
    transform: translate3d(85px, 0, 0);
  }
}
/*Shrinking for mobile*/
@media (max-width: 768px) {
  .waves {
    height: 40px;
    min-height: 40px;
  }
  .half-bg{
        height: 500px;
    }
}
.service-subtitle{
  color: #546E7A;
}
.service-title{
  color: #37474F;
}
</style>