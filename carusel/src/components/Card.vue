<template>
    <div>
        <v-card width="600" class="mx-auto" elevation="10">
            <v-list-item>
                <v-list-item-content>
                    <v-list-item-title class="headline mb-1">
                        User Name
                    </v-list-item-title>
                    <v-list-item>
                        <div>
                            <v-list-item-title class="headline mb-4">
                                About:
                            </v-list-item-title>
                            <p>Name: {{Name}}</p>                            <p>Surname: {{Surname}}</p>
                            <p>Age: {{Age}}</p>
                            <p>Location: {{Location}}</p>
                        </div>
                    </v-list-item>
                </v-list-item-content>
                <v-list-item-avatar size="200">
                    <v-img
                    src="https://cdn.pixabay.com/photo/2020/06/24/19/12/cabbage-5337431_1280.jpg"
                    >
                    </v-img>
                </v-list-item-avatar>
                <v-list-item-action>
                </v-list-item-action>
            </v-list-item>
            <v-card-actions>
                <v-btn
                        color="orange lighten-2"
                        text
                    >
                        Photos
                    </v-btn>

                    <v-spacer></v-spacer>

                    <v-btn
                        icon
                        @click="Show = !Show"
                    >
                    <v-icon>{{ Show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                    </v-btn>
            </v-card-actions>
            <div>
                <Carusel v-show="Show"/>
            </div>
        </v-card>
    </div>
</template>

<script>
import Carusel from './Carusel'
export default {
    name: "Card",
    components:{
        Carusel
    },
    data: function(){
        return{
            Name: "Roman",
            Surname: "Seleznev",
            Age: "20",
            Location: "Russia",
            Show: false
        }
    }
}
</script>

<style>
#page{
    margin: 5%;
    padding: 5%;
}
</style>