<template>
<v-stepper v-model="e1" id="quote_stepper3" class="quote-stepper elevation-0">
    <div id="jumbo-content">
    <v-form>
      <v-stepper-items>
        <!-------------------------//-->  
        <!--Step 1-----------------//-->  
        <!-------------------------//-->  
        <v-stepper-content step="1">
        <v-container>
        <v-row>
        <v-col cols="12" align="center" justify="center">
        <h1 class="display-1 mt-5 mb-5">We are Web and App Developers in Dallas, Texas</h1>
        <div class="subtitle-1 mb-5">
        We can create a web presence for you and help you reach more potential customers. Request a quote for a free consultation.
        </div>
          <v-btn
            color="orange darken-4"
            @click="e1 = 2"
          >
            Request a Quote
          </v-btn>
        </v-col>
        </v-row>
        </v-container>
        </v-stepper-content>
        <!-------------------------//-->  
        <!--Step 2-----------------//--> 
        <!-------------------------//-->
        <v-stepper-content step="2">
        <div class="subtitle-1 mb-5">
        What kind of project do you have?
        </div>
          <v-select class="mt-5 mb-5"
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
        <div class="subtitle-1 mb-5">
        What do you plan on doing with your site/app?
        </div>

          <v-select class="mt-5 mb-5"
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
        <div class="subtitle-1 mb-5">
        What type of organization are you with?
        </div>

          <v-select class="mt-5 mb-5"
          v-model="org_type"
          name="org_type"
          :items="org_type_items"
          label="What type of organization are you with?"
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
        <div class="subtitle-1 mb-5">
        How soon do you need your project done?
        </div>
          <v-select class="mt-5 mb-5"
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
        <div class="subtitle-1 mb-5">
        Please enter your name so we know who to contact
        </div>
          <v-text-field
          class="mt-5 mb-5"
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
        <div class="subtitle-1 mb-5">
        Please enter an email address where we can reach you.
        We will only contact you about this quote request. 
        </div>
          <v-text-field
          class="mt-5 mb-5"
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
      </div>
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
            
                this.$http.post('https://api.dfwdev.com/quote_requests', { 
                website_requirements: this.site_req,
                website_type: this.site_type,
                organization_type: this.org_type, 
                timeframe: this.timeframe,
                name: this.name,
                email: this.email
                })
                
                document.getElementById("jumbo-content").innerHTML = "<div class='confirm-wrap'><div class='display-1 mt-5 mb-5 info-received'>We Have Received Your Information</div>"+
                "<div class='subtitle-1'>A developer will contact you soon by email to begin discussing your project with you. "+
                "In the meantime, feel free to keep browsing our site to learn about your services.</div></div>";

        }
    }
}
</script>
<style>

.quote-stepper{
    background: none!important;
}
.confirm-wrap{
  text-align: center;
  padding: 10px;
}
.info-received {
    color: #76FF03!important;
}
</style>