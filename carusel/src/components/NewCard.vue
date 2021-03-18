<template>
  <v-card width="600" class="mx-auto" elevation="10">
      <v-list-item>
          <v-list-item-title>
              <v-list-item-avatar size="80">
                    <v-img
                    src="https://cdn.pixabay.com/photo/2020/06/24/19/12/cabbage-5337431_1280.jpg"
                    >
                    </v-img>
                </v-list-item-avatar>
             {{Com.UserName}} comment:
          </v-list-item-title>
          <v-list-item>
              <div>
                  <p>{{Com.Massage}}</p>
              </div>
          </v-list-item>
      </v-list-item>
  </v-card>
</template>

<script>
export default {
    name: 'NewCard',
    props: ['Com'],
    
}
</script>

<style>

</style>