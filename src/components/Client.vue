<template>
  <v-row class="mt-10 mb-5">
    <v-col
      cols="12"
      xs="12"
      sm="6"
      md="4"
      v-for="(client, i) in clients"
      :key="i"
    >
      <v-card class="elevation-16 mx-auto" width="300">
        <v-list subheader two-line>
          <v-list-item>
            <v-list-item-avatar>
              <v-img :src="client.img"></v-img>
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>{{ client.title }}</v-list-item-title>

              <v-list-item-subtitle>{{ client.subtitle }}</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>
        <v-card-text>
          <div class="mt-n7">
            <v-rating
              v-model="rating"
              color="yellow darken-3"
              background-color="grey darken-1"
              empty-icon="$ratingFull"
              half-increments
              hover
              small
            ></v-rating>
          </div>
          {{ client.bio }}
        </v-card-text>
      </v-card>
     
    </v-col>
    
    
  </v-row>
</template>

<script>
export default {
  data: () => ({
    rating: 4.5,
  
    clients: [
      {
        img: "https://cdn.vuetifyjs.com/images/lists/1.jpg",
        title: "Kareem Benji",
        subtitle: "CPO on Maqua",
        bio: "If you enjoy using Vuetify, please take a few seconds to rate your experience with the framework. It really helps!",
      },
      {
        img: "https://cdn.vuetifyjs.com/images/lists/2.jpg",
        title: "AAE IdeaPro",
        subtitle: "CPO on Maqua",
        bio: "If you enjoy using Vuetify, please take a few seconds to rate your experience with the framework. It really helps!",
      },
      {
        img: "https://cdn.vuetifyjs.com/images/lists/3.jpg",
        title: "Raul Seem ",
        subtitle: "CPO on Maqua",
        bio: "If you enjoy using Vuetify, please take a few seconds to rate your experience with the framework. It really helps!",
      },
    ],
  }),
};
</script>

<style>
</style>