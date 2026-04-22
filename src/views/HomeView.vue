

<template>
    <v-container>
    <v-row justify="center">
    <v-col cols="12" xs="12">
        <v-carousel>
    <v-carousel-item 
    v-for="ad in ads.filter(ad => ad.promo === true)"
                        :key="ad.id"
                        :src="ad.src"
    cover
    ></v-carousel-item>
    </v-carousel>
</v-col>
</v-row>
</v-container>
<v-container>
  <v-row justify="center">
  <v-col cols="12" xs="12">
    v-for="ad in ads"
                :key="ad.id"

  <v-card>
        <v-img
    height="200px"
    :src="ad.src"
      ></v-img>
  <v-card-title primary-title>

<div>

                            <!-- ЗДЕСЬ меняем: статические тексты на динамические -->
                            <h3 class="headline mb0">{{ ad.title }}</h3>
                            <div>{{ ad.desc }}</div>
                        </div>

  </v-card-title>
  <v-card-actions>
    <v-spacer></v-spacer>
    <v-btn text>Open</v-btn>
    <v-btn raised color="primary">
              Buy
</v-btn>
</v-card-actions>
</v-card>
</v-col>
</v-row>
</v-container>
</template>

<script>
export default {
    data() {
        return {
            ads: [
                {
                    title: "First",
                    desc: "First Desc",
                    promo: true,
                    src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg",
                    id: "1"
                },
                {
                    title: "Second",
                    desc: "Second Desc",
                    promo: true,
                    src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg",
                    id: "2"
                },
                {
                    title: "Third",
                    desc: "Third Desc",
                    promo: true,
                    src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg",
                    id: "3"
                },
                {
                    title: "Fourth",
                    desc: "Fourth Desc",
                    promo: true,
                    src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg",
                    id: "4"
                }
            ]
        }
    }
}
</script>