<template>
<div ill-height>
<v-sheet class="align-center" color="blue lighten-5" height="200" style="text-align: center;">
<h1 class="page-title">Contact Us</h1>
</v-sheet>
<v-sheet    fill-height
            tile="tile"
            :elevation="3"
            class="no-round d-flex pa-2 content"
            id="bottom-content"
            width="100%"
            color="white"
            style="height: 100%!important;"
          >

          
          <v-container fill-height>
          <v-row > 
          <v-col class="justify-center text-center align-center pa-10" style="margin-top: 50px;">
          <v-card class="pa-3 card content align-center text-center" flat color="blue darken-4" id="message-form-card">
          <div id="message-form">
          <h2 class="font-weight-medium" style="color: #fff;">Send Us a Message</h2>
          <p>
          <v-form>

          <v-text-field
            v-model="name"
            name="name"
            :rules="nameRules"
            label="Your Name"
            required
          ></v-text-field>

          <v-text-field
            v-model="email"
            name="email"
            :rules="emailRules"
            label="Your Email Address"
            required
            class="input-theme"
          ></v-text-field>
          
          <v-textarea
            v-model="message"
            filled
            name="message"
            :rules="messageRules"
            label="Type Your Message Here"
            class="input-theme"
          ></v-textarea>
          
          <v-btn
            :disabled="!valid" 
            color="orange darken-4"
            @click="onSubmit()"
          >
            Send Message
          </v-btn>

          </v-form>
          </p>
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
      title: 'Contact Us',
      meta: [
        { hid: 'description', name: 'description', content: 'Contact DFWDev.com'}

      ]
    }
  },
    data(){
        return{
            class: 'input-theme',
            valid: true,
            name: '',
            nameRules: [
            v => !!v || 'Name is required',
            v => (v && v.length <= 50) || 'Name must be less than 50 characters',
        ],
            email: '',
            emailRules: [
            v => !!v || 'E-mail is required',
            v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
        ],
            message: '',
            messageRules: [
            v => !!v || 'Name is required',
            v => (v && v.length <= 800) || 'Name must be less than 800 characters.',
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
            console.log({ name: this.name, email: this.email, message: this.message })
            
                this.$http.post('https://api.dfwdev.com/contact_requests', { 
                name: this.name,
                email: this.email,
                message: this.message
                })
                //document.getElementById("message-form-card").style.visibility = "hidden";
                document.getElementById("message-form").innerHTML = "<h3 class='display-2' style='color: #76FF03;'>We Have Received Your Message</h3>"+
                "<h4 class='subtitle-1' style='color: #ffffff'>Someone will contact you soon.</h4>";
                

        }
    }

}
</script>
<style scoped>
.page-title{
    color: #0D47A1;
    position: relative;
    top: 100px;
}
.content{
    color: #000!important;
}
.input-theme{
    color: #000!important;
}
.v-btn{
    color: #fff!important;
}
</style>