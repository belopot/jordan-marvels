<template>
  <div class="relative home-view overflow-hidden">
    <div id="banner">
      <b-carousel
        :interval="4000"
        indicators
        background="#ababab"

      >
        <!-- Slide with blank fluid image to maintain slide aspect ratio -->
        <bannerContent svg_banner = "banner1.png"/>
        <bannerContent svg_banner = "banner2.png"/>
        <bannerContent svg_banner = "banner1.png"/>
        <bannerContent svg_banner = "banner2.png"/>
      </b-carousel>
    </div>

    <section>
      <b-container>
        <b-row>
          <b-col>
            <book-a-trip />
          </b-col>
        </b-row>
      </b-container>
    </section>

    <section class="section">
      <b-container>
        <b-row>
          <mood></mood>
          <traveling></traveling>
        </b-row>
      </b-container>
    </section>

    <section class="section mt-5">
      <featured></featured>
    </section>

    <section class="section mt-5">
      <premium-experience></premium-experience>
    </section>
    <section class="section mt-5">
      <travellers-use></travellers-use>
    </section>
    <section class="section">
      <featured-in></featured-in>
    </section>
  </div>
</template>

<script>
import BannerContent from "../components/home/BannerContent.vue";
import BookATrip from "../components/home/BookATrip.vue";
import Mood from "../components/home/Mood.vue";
import Traveling from "../components/home/Traveling.vue";
import Featured from "../components/home/Featured";
import PremiumExperience from "../components/home/PremiumExperience";
import TravellersUse from "../components/home/TravellersUse";
import FeaturedIn from "../components/home/FeaturedIn";

export default {
  name: "Home",
  components: {
    bannerContent: BannerContent,
    BookATrip,
    mood: Mood,
    traveling: Traveling,
    featured: Featured,
    "premium-experience": PremiumExperience,
    "travellers-use": TravellersUse,
    "featured-in": FeaturedIn
  }
};
</script>
<style>
</style>
