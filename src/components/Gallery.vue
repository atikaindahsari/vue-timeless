<template>
  <div class="block galleryBlock">
    <v-container>
      <h2 class="text-center">Gallery</h2>
      <v-row>
        <v-col v-for="item in items" :key="item.id" class="d-flex child-flex" cols="6" md="4">
          <v-img :src="item.src" aspect-ratio="1" cover class="bg-grey-lighten-2">
            <template v-slot:placeholder>
              <v-row class="fill-height ma-0" align="center" justify="center">
                <v-progress-circular indeterminate color="grey-lighten-5"></v-progress-circular>
              </v-row>
            </template>
          </v-img>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Gallery',

  data: () => {
    return {
      items: [
        {
          id: 1,
          src: require("../assets/images/gallery1.jpg")
        },
        {
          id: 2,
          src: require("../assets/images/gallery2.jpg")
        },
        {
          id: 3,
          src: require("../assets/images/gallery3.jpg")
        },
        {
          id: 4,
          src: require("../assets/images/gallery4.jpg")
        },
        {
          id: 5,
          src: require("../assets/images/gallery5.jpg")
        },
        {
          id: 6,
          src: require("../assets/images/gallery6.jpg")
        },
        {
          id: 7,
          src: require("../assets/images/gallery7.jpg")
        },
        {
          id: 8,
          src: require("../assets/images/gallery8.jpg")
        },
        {
          id: 9,
          src: require("../assets/images/gallery9.jpg")
        },
      ]
    }
  },
}
</script>
