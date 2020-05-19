<template>  
<div class="banner-component">
  <img
      class="d-block img-fluid w-100"
      width="1024"
      height="480"
      :src="require(`../../assets/png/${svg_banner}`)"
      alt="image slot"
  />

  <div class="fields-wrap">
    <b-container>
        <b-row>
          <b-col>
            <div class="banner-large-text">Discover</div>                
            <div class="banner-small-text">918 DESTINATIONS FOUND</div>                
          </b-col>
        </b-row>
    </b-container>
  </div>
</div>                  
</template>

<script>
export default {
  name: "BannerContent",
  props:{
    svg_banner: String
  }
}
</script>
<style lang="scss">
.banner-component{
  position: relative;
  max-height: 660px;
  overflow: hidden;

  .fields-wrap{
    position: absolute;
    top: 50%;
    left: 0;
    width: 100%;
    -webkit-transform: translateY(-50%);
    -moz-transform: translateY(-50%);
    transform: translateY(-50%);
    color: #FFFFFF;
  }
  .banner-large-text{
    font-weight: bold;
    font-size: 58px;
    line-height: 1.3;
  } 
  .banner-small-text{
    font-weight: bold;
    font-size: 16px;    
  }  
}


</style>