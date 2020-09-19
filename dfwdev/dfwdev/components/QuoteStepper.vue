<template>
<v-stepper v-model="e1" id="quote_stepper3" class="quote-stepper elevation-0">
    <v-form>
      <v-stepper-items>
        <!-------------------------//-->  
        <!--Step 1-----------------//-->  
        <!-------------------------//-->  
        <v-stepper-content step="1">
          <v-btn
            color="green darken-3"
            @click="e1 = 2"
          >
            Request a Quote
          </v-btn>
        </v-stepper-content>
        <!-------------------------//-->  
        <!--Step 2-----------------//--> 
        <!-------------------------//-->
        <v-stepper-content step="2">
          <v-select
          v-model="site_req"
          name="site_req"
          :items="site_req_items"
          label="What type of project do you have?"
          :rules="[v => !!v || 'This field is required']"
          required
          ></v-select>
  
          <v-btn
            :disabled="!site_req"
            color="orange darken-4"
            @click="e1 = 3"
          >
            Continue
          </v-btn>
        </v-stepper-content>
        <!-------------------------//-->  
        <!--Step 3-----------------//--> 
        <!-------------------------//-->
        <v-stepper-content step="3">
          <v-select
          v-model="site_type"
          name="site_type"
          :items="site_type_items"
          label="What do you plan on doing with your site/app?"
          :rules="[v => !!v || 'This field is required']"
          required
          ></v-select>
  
          <v-btn
            :disabled="!site_type"
            color="orange darken-4"
            @click="e1 = 4"
          >
            Continue
          </v-btn>
        </v-stepper-content>
        <!-------------------------//-->  
        <!--Step 4-----------------//--> 
        <!-------------------------//-->
        <v-stepper-content step="4">
          <v-select
          v-model="org_type"
          name="org_type"
          :items="org_type_items"
          label="What type of organization are you?"
          :rules="[v => !!v || 'This field is required']"
          required
          ></v-select>
  
          <v-btn
            :disabled="!org_type"
            color="orange darken-4"
            @click="e1 = 5"
          >
            Continue
          </v-btn>
        </v-stepper-content>
        <!-------------------------//-->  
        <!--Step 5-----------------//--> 
        <!-------------------------//-->
        <v-stepper-content step="5">
          <v-select
          v-model="timeframe"
          name="timeframe"
          :items="timeframe_items"
          label="How soon do you need your project done?"
          :rules="[v => !!v || 'This field is required']"
          required
          ></v-select>
  
          <v-btn
            :disabled="!timeframe"
            color="orange darken-4"
            @click="e1 = 6"
          >
            Continue
          </v-btn>
        </v-stepper-content>
        <!-------------------------//-->  
        <!--Step 6-----------------//--> 
        <!-------------------------//-->
        <v-stepper-content step="6">
          
          <v-text-field
          v-model="name"
          name="name"
          label="Your name"
          :rules="nameRules"
          required
          ></v-text-field>  
          <v-btn
            :disabled="!name"
            color="orange darken-4"
            @click="e1 = 7"
          >
            Continue
          </v-btn>
        </v-stepper-content>
        <!-------------------------//-->
        <!--Step 7-----------------//--> 
        <!-------------------------//-->
        <v-stepper-content step="7">
          
          <v-text-field
          v-model="email"
          name="email"
          label="Your Email (Will only be used by us to contact you)"
          :rules="emailRules"
          required
          ></v-text-field>  
          <v-btn
            :disabled="!email" 
            color="light-green darken-1"
            @click="onSubmit()"
          >
            Request a Quote
          </v-btn>
        </v-stepper-content>
      </v-stepper-items>
      </v-form>
    </v-stepper>    
</template>
<script>
export default {
    data(){
        return{
            valid: true,
            name: '',
            nameRules: [
            v => !!v || 'Name is required',
            v => (v && v.length <= 30) || 'Name must be less than 30 characters',
        ],
            email: '',
            emailRules: [
            v => !!v || 'E-mail is required',
            v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
        ],
            select: null,
            e1: 1,
            site_req: '',
            site_type: '',
            org_type: '',
            timeframe: '',
            name: '',
            email: '',
            site_req_items: 
            [
                "New Website", 
                "Major Changes on Existing Site/App", 
                "Minor Changes on Existing Site/App", 
                "Not Sure"
            ],
            site_type_items: 
            [
                "Advertise My Business", 
                "Sell Products with an Online Store", 
                "Sell a Subscription Service", 
                "Not Sure"
            ],
            org_type_items: 
            [
                "Small Business", 
                "Large Business/Corporate", 
                "Non-Profit/Charity",
                "Personal Website",  
                "Not Sure"
            ],
            timeframe_items: 
            [
                "ASAP/Time-Sensitive", 
                "Weeks", 
                "Months", 
                "Not Sure"
            ],
        }
        

    },
    methods:{
            validate () {
            this.$refs.form.validate()
        },
            reset () {
            this.$refs.form.reset()
        },
            onSubmit (){   
            console.log({ site_req: this.site_req, site_type: this.site_type, org_type: this.org_type, timeframe: this.timeframe, name: this.name, email: this.email})
            
                this.$http.post('http://35.239.79.126/quote_requests', { 
                website_requirements: this.site_req,
                website_type: this.site_type,
                organization_type: this.org_type, 
                timeframe: this.timeframe,
                name: this.name,
                email: this.email
                })
                document.getElementById("stepper-header").style.visibility = "hidden";
                document.getElementById("jumbo-content1").innerHTML = "<h3 class='display-2' style='color: #76FF03;'>We Have Received Your Request</h3>"+
                "<h4 class='subtitle-1'>Someone will email you within 24 hours at the address you provided to discuss your project.</h4>";
                document.getElementById("jumbo-content2").innerHTML = "<h3 class='display-2' style='color: #76FF03;'>We Have Received Your Request</h3>"+
                "<h4 class='subtitle-1'>Someone will email you within 24 hours at the address you provided to discuss your project.</h4>";
                document.getElementById("jumbo-content3").innerHTML = "<h3 class='display-2' style='color: #76FF03;'>We Have Received Your Request</h3>"+
                "<h4 class='subtitle-1'>Someone will email you within 24 hours at the address you provided to discuss your project.</h4>";

        }
    }
}
</script>
<style>
.quote-stepper{
    background: none!important;
}
.request-received h1{
    color: #7CB342!important;
}
</style>