<template>
  <div class="featured-in">
    
    <div class="top-heading text-center">
      <span>Jordan Marvels Has Been Fetures In</span>
    </div>
    
    <b-container class="jordan-featured-wrap">
      <b-row>
        <b-col>
          <carousel :items="4" :nav="false" :dots="false" :margin="20">
            <img src="../../assets/freatured-1.jpg" />

            <img src="../../assets/freatured-2.jpg" />

            <img src="../../assets/freatured-3.jpg" />

            <img src="../../assets/freatured-4.jpg" />
          </carousel>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
import carousel from "vue-owl-carousel2";
export default {
  components: { carousel }
};
</script>
<style lang="scss">
.featured-in {

  .top-heading {
    position: relative;
    font-size: 16px;
    font-weight: bold;
    text-transform: uppercase;
    color: var(--primary);

    span{
      display: inline-block;
      background: #fff;
      padding: 0 30px;
    }
    &::after {
      content: "";
      width: 100%;
      border-top: 1px solid var(--primary);
      position: absolute;
      z-index: -1;
      top: 50%;
      -webkit-transform: translateY(-50%);
      -moz-transform: translateY(-50%);
      transform: translateY(-50%);
      left: 0;
      right: 0;
    }
  }
  h6 {
    position: relative;
    text-transform: uppercase;
    color: #c7b298;
    font-weight: bold;
    padding: 0 20px;
    background: #fff;
    display: inline-block;
    z-index: 2;
  }
}
.jordan-featured-wrap {
  padding: 40px 0;
}
</style>
