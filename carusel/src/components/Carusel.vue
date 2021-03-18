<template>
  <v-carousel
      :continuous="false"
      :cycle="cycle"
      
      hide-delimiter-background
      delimiter-icon="mdi-minus"
      height="300"
    >
      <v-carousel-item
        v-for="(Comment, i) in Comments"
        :key="i"
      >
          <NewCard :Com="Comment"/>
      </v-carousel-item>
    </v-carousel>
</template>

<script>
import NewCard from './NewCard.vue'
export default {
    name: 'Carusel',
    components:{
      NewCard
    },
    data: function(){
        return{
            model: 0,
            items: [
                        {
                            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
                        },
                        {
                            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
                        },
                        {
                            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
                        },
                        {
                            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
                        },
                    ],
          Comments: [
            {
                UserName: 'Bob', Massage: 'BobBobBobBobBobBobBobBobBobBob'
            },
            {
                UserName: 'Sara', Massage: 'SaraSaraSaraSaraSaraSaraSaraSara'
            },
            {
                UserName: 'Jon', Massage: 'JonJonJonJonJonJonJonJonJonJonJon'
            },
            {
                UserName: 'Luck', Massage: 'LuckLuckLuckLuckLuckLuckLuckLuckLuck'
            }
          ]
        }
    }
}
</script>

<style>

</style>