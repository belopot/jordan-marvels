<template>
  <b-col cols="4" class="premuim-box">    
    <figure>
      <b-img
        :src="require(`../../assets/${imageUrl}`)"
        fluid
        class="w-100"
      ></b-img>
    </figure>
    <div class="details-wrap">
      <h1 class="text-right">{{ tourName }}</h1>
      <div class="text-right price-wrap">        
          <span class="start-price">starting from</span>          
          <strong>$464</strong>        
      </div>
    </div>    
    <div class="text-right btn-book-wrap">
      <book-now>Book Now</book-now>
    </div>
    
  </b-col>
</template>
<script>
import Button from "../common/Button";
export default {
  name: "PremiumBox",
  props: {
    tourName: String,
    imageUrl: String,
    stratingPrice: String,
    tourUrl: String
  },
  components: {
    "book-now": Button
  }
};
</script>
<style lang="scss">
.premuim-box {
  
  figure {
    margin-bottom: 0;
  }
  .details-wrap {
    transform: translateY(-100px);
    h1 {
      color: white;
      font-size: 18px;
      margin-right: 30px;
      font-weight: 700;
    }
  }
  .price-wrap {    
    margin-right: 30px;
    color:white;         
    .start-price {      
      font-size: 14px;      
      font-weight: 300;
      margin-right: 16px;
      display: inline-block;
      transform: translateY(-5px);
    }
    strong {
      font-size: 28px;
      font-weight: 700;
    }
  }
  .btn-book-wrap {
      transform: translateY(-90px);
      margin-right: 30px;
  }
}
</style>
