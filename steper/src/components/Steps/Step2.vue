<template>
    <div>
        <h1>Registration</h1>
        <p class="Error">{{Errors.MailError}}</p>
        <p class="Error">{{Errors.PasswordError}}</p>
        <p class="Error">{{Errors.SecondPasswordError}}</p>
        
        <v-text-field class="vInput"
                v-model="Mail"
                label="Mail"
                placeholder="">
            </v-text-field>
        
        <v-text-field class="vInput"
                v-model="Password"
                label="Password"
                placeholder="">
            </v-text-field>
        
        <v-text-field class="vInput"
                v-model="SecondPassword"
                label="SecondPassword"
                placeholder="">
            </v-text-field>
        
        <button @click="Accept()">Accept</button>
    </div>
</template>

<script>
export default {
    name: 'Step2',
    data: function(){
        return{
            Mail:"",
            Password:"",
            SecondPassword:"",
            Errors:{
                MailError: "",
                SecondPasswordError: "",
                PasswordError: ""
            }
        }
    },
    methods:{
        Accept: function(){
            let count =0;
            if(!this.Mail.includes('@'))
               this.Errors.MailError = "Invalid mail"
            else{
                this.Errors.MailError = ""
                count = count+1
            }
            if(this.Password == "")
                this.Errors.PasswordError = "Emty password"
            else{
                this.Errors.PasswordError = ""
                count = count+1
            }
            if(this.Password != this.SecondPassword)
                this.Errors.SecondPasswordError = "Invalid second password"
            else{
                this.Errors.SecondPasswordError = ""
                count =count+1
            }
            if(count == 3)
                this.$emit('Accept', this.Mail, this.Password) 
        }
    }
}
</script>

<style scoped>
.Error{
    color: red;
}
.vInput{
    width: 50%;
}
</style>