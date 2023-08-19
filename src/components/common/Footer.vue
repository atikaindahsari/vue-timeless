<template>
  <v-container>
    <v-footer class="text-center d-flex flex-column">
      <div>
        <v-btn
          v-for="(icon, index) in icons"
          :key="index"
          class="mx-4"
          :icon="icon"
          variant="text"
        >
          <v-icon class="icon-black" @click="openLink(icon)">{{ icon }}</v-icon>
        </v-btn>
      </div>

      <div class="mt-6 text-black">
        Through the lens of creativity and passion, we capture moments that tell your unique story. Let us frame your memories with artistry and emotion, turning fleeting seconds into timeless treasures. Experience the art of photography with TIMELESS, where every snapshot becomes a masterpiece.
      </div>

      <v-divider></v-divider>

      <div class="mt-6 text-black">
        {{ new Date().getFullYear() }} — <strong>Timeless - Vue Project</strong>
      </div>
    </v-footer>
  </v-container>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Footer',

  data: () => ({
    icons: [
      'mdi-facebook',
      'mdi-youtube',
      'mdi-linkedin',
      'mdi-instagram',
    ],
  }),

  methods: {
    openLink(icon) {
      switch (icon) {
        case 'mdi-facebook':
          window.open('https://www.facebook.com/TimelessPhotography2021', '_blank');
          break;
        case 'mdi-youtube':
          window.open('https://www.youtube.com/@TimelessPhotographyMadison', '_blank');
          break;
        case 'mdi-linkedin':
          window.open('https://www.linkedin.com/company/timeless-photography-llc', '_blank');
          break;
        case 'mdi-instagram':
          window.open('https://www.instagram.com/timeless_photography____/', '_blank');
          break;
        default:
          break;
      }
    },
  },
};
</script>
