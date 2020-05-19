<template>
  <div class="relative home-view overflow-hidden">
    <div id="banner">          
        <bannerContent svg_banner = "banner1.png"/>    
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
    <section class="section mt-5">
      <featured></featured>
    </section>
    <section class="section mt-5">
      <premium-experience></premium-experience>
    </section>        
    <section class="section">
      <featured-in></featured-in>
    </section>    
  </div>
</template>

<script>
import BannerContent from "../components/Destinations/BannerContent.vue";
import BookATrip from "../components/Destinations/BookATrip.vue";
import Featured from "../components/home/Featured";
import PremiumExperience from "../components/Destinations/PremiumExperience";

import FeaturedIn from "../components/home/FeaturedIn";

export default {
  name: "Destinations",
  components: {
    bannerContent: BannerContent,
    BookATrip,    
    featured: Featured,
    "premium-experience": PremiumExperience,  
    "featured-in": FeaturedIn,     
  }
};
</script>
<style>
</style>
