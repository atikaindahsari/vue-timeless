<template>
  <v-container>
    <div class="heroBlock">
      <v-carousel hide-delimiters cycle>
        <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src" cover>
          <div class="d-flex fill-height title justify-center align-center">
            <div class="hidden-xs-only">
              {{ item.title }}
            </div>
          </div>
        </v-carousel-item>
      </v-carousel>
    </div>
  </v-container>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Hero',

  data() {
    return {
      items: [
        {
          src: require('../assets/images/carousel1.jpg'),
          title: "Picture Perfect Memories"
        },
        {
          src: require('../assets/images/carousel2.jpg'),
          title: "Photography with Heart and Art"
        },
        {
          src: require('../assets/images/carousel3.jpg'),
          title: "Turning Visions into Visuals"
        },
        {
          src: require('../assets/images/carousel4.jpg'),
          title: "Capture the Beauty"
        },
        {
          src: require('../assets/images/carousel5.jpg'),
          title: "Snap. Click. Cherish"
        },
      ],
    }
  },
}
</script>
