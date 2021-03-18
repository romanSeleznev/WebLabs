<template>
    <div>
            <h1>Name</h1>

            <p class="Error">{{Error}}</p>
            
            <v-text-field class="vInput"
                v-model="FirstName"
                label="First Name"
                placeholder="">
            </v-text-field>
            <v-text-field class="vInput"
                v-model="LastName"
                label="Last Name"
                placeholder="">
            </v-text-field>
            
            <v-btn @click="Accept()">Accept</v-btn>
    </div>
    
</template>

<script>
export default {
    name: 'Step1',
    data: function(){
        return{
            FirstName: "",
            LastName: "",
            Error: ""
        }
    },
    methods:{
        Accept: function(){
            if((this.FirstName == "")||(this.LastName == ""))
                this.Error = "Enter first or last name"
            else{
                this.Error = "",
                this.$emit('Accept',this.FirstName, this.LastName)
            }
        }
    }
}
</script>

<style scoped>
.vInput{
    width: 50%;
}
.Error{
    color: red;
}
</style>