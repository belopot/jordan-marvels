<template>
  <div>
    <heading
      heading="Discover Results"
      btnText="View All"
      btnLink="#"
    ></heading>  
    <b-container>
      <b-row>
        <premium-box
          tourName="PETRA BY DAY&NIGHT"
          imageUrl="0014.png"
        ></premium-box>
        <premium-box
          tourName="PETRA BY DAY&NIGHT"
          imageUrl="0014.png"
        ></premium-box>
        <premium-box
          tourName="PETRA BY DAY&NIGHT"
          imageUrl="0014.png"
        ></premium-box>
      </b-row>
      <b-row>
        <premium-box
          tourName="PETRA BY DAY&NIGHT"
          imageUrl="0014.png"
        ></premium-box>
        <premium-box
          tourName="PETRA BY DAY&NIGHT"
          imageUrl="0014.png"
        ></premium-box>
        <premium-box
          tourName="PETRA BY DAY&NIGHT"
          imageUrl="0014.png"
        ></premium-box>
      </b-row>
      <b-row>
        <premium-box
          tourName="PETRA BY DAY&NIGHT"
          imageUrl="0014.png"
        ></premium-box>
        <premium-box
          tourName="PETRA BY DAY&NIGHT"
          imageUrl="0014.png"
        ></premium-box>
        <premium-box
          tourName="PETRA BY DAY&NIGHT"
          imageUrl="0014.png"
        ></premium-box>
      </b-row>
      <discover-button>SEE MORE PLACES TO DISCOVER</discover-button>
    </b-container>    
  </div>
</template>

<script>
import PremiumBox from "./PremiumBox.vue";
import Heading from "./Heading.vue";
import DiscoverButton from "./DiscoverButton";
export default {
  components: {
    "premium-box": PremiumBox,
    heading: Heading,
    "discover-button": DiscoverButton
  }
};
</script>
