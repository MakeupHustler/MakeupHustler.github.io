<template>
  <section id="hero">
    <v-carousel
      height="calc(100vh - 64px)"
      dark
      cycle
      show-arrows-on-hover
      draggable="true"
      hide-delimiter-background
    >
      <v-carousel-item
        v-for="(carousel, carindex) in carouselsData"
        :key="carindex"
        :src="carousel.src"
        class="gradient-fill"
      >
        <v-container fill-height>
          <div style="max-width: 600px">
            <div class="text-md-h2 mb-3 text-sm-h3 text-h5 font-weight-black">
              {{ carousel.heading.toUpperCase() }}
            </div>
            <p class="mb-5">{{ carousel.subHeading }}</p>
            <v-btn
              :x-large="$vuetify.breakpoint.smAndUp"
              class="my-3 primary"
              href="/contact"
              >Get Started</v-btn
            >
            <span class="mx-2 my-4"></span>
            <v-btn
              :x-large="$vuetify.breakpoint.smAndUp"
              text
              class="my-3"
              outlined
              :href="carousel.href"
              ><v-icon left large color="primary">mdi-play</v-icon>Learn
              More</v-btn
            >
          </div>
        </v-container>
      </v-carousel-item>
    </v-carousel>
  </section>
</template>

<script>
export default {
  data() {
    return {
      carouselsData: [
        {
          src: '/bridal/bridal-050-crop.jpg',
          heading: ' MAKEUP HUSTLER SA',
          subHeading: '@makeuphustersa',
          href: '/contact',
        },
        {
          src: '/creative/creative-014-crop.jpg',
          heading: ' BRIDAL ',
          subHeading:
            'Designs that lead to beautiful photos for your special day',
          href: '/bridal',
        },
        {
          src: '/creative/creative-050-crop.jpg',
          heading: ' CREATIVE ',
          subHeading: 'Uniquely inspired looks for every occassion',
          href: '/creative',
        },
        {
          src: '/creative/creative-009-crop.jpg',
          heading: ' CUSTOM ',
          subHeading: 'Delivering just the right look for your needs.',
          href: '/creative',
        },
      ],
    }
  },
}
</script>

<style scoped>
.gradient-fill .v-responsive__content {
  background: rgb(0, 0, 0);
  background: linear-gradient(
    to right,
    rgba(78, 78, 78, 0.25),
    rgba(78, 78, 78, 0.35)
  );
}
</style>
