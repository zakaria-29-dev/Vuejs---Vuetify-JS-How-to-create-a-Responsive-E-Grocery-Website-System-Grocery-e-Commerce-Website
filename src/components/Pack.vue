<template>
  <v-row justify="center" class="space px-16 pb-5">
    <v-col cols="12" xs="12" sm="6" md="4" v-for="(pack, i) in packs" :key="i">
      <v-card class="mx-auto rounded-xl" max-width="300" color="" flat outlined>
        <div align="center" justify="center">
          <v-img
            max-height="300"
            max-width="300"
            contain
            :src="pack.img"
          ></v-img>
        </div>

        <v-card-title class="">{{ pack.title }}</v-card-title>
        <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">{{
          pack.subtitle
        }}</v-card-title>
        <v-card-title class="mt-n4">{{ pack.price }}</v-card-title>

        <v-card-actions class="mx-2 mt-n4">
          <v-btn outlined class="mt-n2 add">
            <v-icon color="green" @click="decrement"> mdi-minus </v-icon>
          </v-btn>

          <strong class="mx-2" v-text="bpm"></strong>
          <v-btn outlined class="mt-n2 add">
            <v-icon color="green" @click="increment"> mdi-plus </v-icon>
          </v-btn>
          <v-spacer></v-spacer>
          <v-btn class="mx-2 mt-n3" fab dark small color="green">
            <v-icon dark> mdi-shopping </v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
      bpm: 1,
    packs: [
      { img: "p1.png", title: "Medium Box", subtitle: "Tomato, Cabbage, Oil, Cauliflower", price: "$55" },
      { img: "p2.png", title: "Big Pack", subtitle: "Tomato, Cabbage, Oil, Cauliflower", price: "$55" },
      { img: "p3.png", title: "Small", subtitle: "Tomato, Cabbage, Oil,Cauliflower ", price: "$55" },
      { img: "p4.png", title: "Medium Box", subtitle: "Tomato, Cabbage, Oil,Cauliflower", price: "$55" },
      { img: "p5.png", title: "Medium Box", subtitle: "Tomato, Cabbage, Oil,Cauliflower", price: "$55" },
      { img: "p6.png", title: "Medium Box", subtitle: "Tomato, Cabbage, Oil,Cauliflower", price: "$55" },
    ],
  }),
   methods: {
      decrement () {
        this.bpm--
      },
      increment () {
        this.bpm++
      },
     
    },
};
</script>

<style>
</style>