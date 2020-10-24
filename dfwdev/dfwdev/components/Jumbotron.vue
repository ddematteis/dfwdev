<template>
<v-container class="jumbo-bg" fill-height fluid >
    <v-row align="center" justify="center">
    <v-col cols="12" md="10" lg="7" xl="7"  justify="center">
        <QuoteStepper/>
    </v-col>
     </v-row>   
     
</v-container>
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
    background: linear-gradient( #1565C0, #01579B);
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
        height: 800px;
    }
}
</style>