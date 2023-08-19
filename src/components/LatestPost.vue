<template>
  <div class="block latestPostBlock">
    <v-container>
      <h2 class="text-center">Latest Post</h2>
      <v-row>
        <v-col cols="12" md="4" v-for="item in items" :key="item.id">
          <v-card outlined class="mx-auto">
            <v-img class="white--text align-end" height="200" :src="item.src" cover>
              <v-card-title>{{ item.title}}</v-card-title>
            </v-img>

            <v-card-subtitle class="pt-4">
              {{ item.subtitle }}
            </v-card-subtitle>

            <v-card-text>
              <div> {{ item.description }}</div>
            </v-card-text>

            <v-card-actions>
              <v-btn color="primary" text :href="item.link" target="_blank">Read</v-btn>
            </v-card-actions>
            
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'LatestPost',

  data: () => {
    return {
      items: [
        {
          id: 1,
          title: "Incredible Road Trips",
          subtitle: "1,000 miles of wonder",
          description: "Embark on a scenic journey through the American West, with breathtaking landscapes and historic landmarks. A road trip to remember",
          src: require("../assets/images/img1.jpg"),
          link: "https://www.afar.com/magazine/best-road-trips-in-the-us-to-take"

        },
        {
          id: 2,
          title: "American Folktales & Stories",
          subtitle: "2,000 miles of wonder",
          description: "Spread joy and cheer this holiday season with festive decor, warm gatherings, and meaningful gifts. Make memories to cherish forever.",
          src: require("../assets/images/img2.jpg"),
          link: "https://www.americanfolklore.net/sindex.html"

        },
        {
          id: 3,
          title: "Upcoming Movies 2023",
          subtitle: "3,000 miles of wonder",
          description: "Escape reality and immerse yourself in a world of imagination through the magic of movies. Discover new stories, emotions, and adventures.",
          src: require("../assets/images/img3.jpg"),
          link: "https://www.movieinsider.com/movies/2023"
        }

      ]
    }
  },
}
</script>
