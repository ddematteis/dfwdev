<template>
<div>
<v-container class="jumbo-bg pa-5" fill-height fluid >
    <v-row align="center" justify="center">
    <v-col cols="12" md="10" lg="7" xl="7" align="center"  justify="center">
        <QuoteStepper/>
    </v-col>
    </v-row>   
</v-container>
<!--
<v-row >
    <v-col cols="12" style="background: #000;"  >

    </v-col>
</v-row> 
//-->
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
<style >
.jumbo-bg{
    /*background-color: linear-gradient( #1565C0, #01579B);*/
    background: #1565C0;
    background-image: url("https://www.transparenttextures.com/patterns/60-lines.png");
    height: 600px;
}
.jumbo-bg h1{
    color: #76FF03;
}
.jumbo-bg h2{
    color: #fff;
}
@media (min-width: 768px){
    .jumbo-bg{
        height: 900px;
    }
}
</style>