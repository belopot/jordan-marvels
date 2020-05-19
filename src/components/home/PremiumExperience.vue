<template>
  <div>
    <heading
      heading="Premium Jordan experience"
      btnText="View All"
      btnLink="#"
    ></heading>
    <b-container>
      <b-row>
        <premium-box
          tourName="Helicopter tour"
          imageUrl="0019.png"
        ></premium-box>
        <premium-box
          tourName="Helicopter tour"
          imageUrl="00120.png"
        ></premium-box>
        <premium-box
          tourName="Helicopter tour"
          imageUrl="001.png"
        ></premium-box>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import PremiumBox from "./PremiumBox.vue";
import Heading from "./Heading.vue";
export default {
  components: {
    "premium-box": PremiumBox,
    heading: Heading
  }
};
</script>
