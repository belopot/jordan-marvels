<template>
  <b-carousel-slide img-blank img-alt="Blank image" class="banner-carousel-component">
      <template v-slot:img>
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
                <div class="banner-text">Book your authentic trip, <br/>get the unique experience.</div>

                <div class="popular-div d-flex">
                  <img src="@/assets/images/outlined.map.svg" />

                  <div class="mt-2">
                    <div class="label">MOST POPULAR</div>
                    <p class="description">Al- Khazneh, Petra</p>
                    <a href="javascript:void(0)" class="link">DISCOVER DESTINATION</a>
                  </div>
                </div>
              </b-col>
            </b-row>
        </b-container>
      </div>
      
      </template>
  </b-carousel-slide>
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
.banner-carousel-component{
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
  .banner-text{
    font-weight: bold;
    font-size: 58px;
    line-height: 1.3;
  }
  .popular-div{
    margin-top: 70px;
    margin-left: auto;
    max-width: 370px;

    img{
      margin-right: 30px;
    }
    .label{
      font-weight: 600;
      text-transform: uppercase;
      line-height: 1.2;
      margin-top: 15px;
    }
    .description{
      font-size: 28px;
      font-weight: 300;
    }
    .link{
      display: flex;
      align-items: center;
      font-size: 14px;
      font-weight: 600;
      text-transform: uppercase;
      color: #fff;

      &:before{
        content: "";
        background-image: url("../../assets/images/destination_line.svg");
        width: 35px;
        height: 1px;
        margin-right: 10px;
      }
      &:after{
        content: "";
        background-image: url("../../assets/images/dropdown.sign.svg");
        width: 11.216px;
        height: 17.269px;
        margin-left: 10px;
      }
    }
  }
}

#banner .carousel-indicators {
  width: 100%;
  max-width: 1140px;
  margin: auto;
  text-align: right;
  justify-content: flex-end;
  padding: 0 15px;
  bottom: 100px;
  margin-bottom: 0;
  align-items: center;

  li {
    width: 14px;
    height: 14px;
    border-radius: 100%;
    background: #fff;
    opacity: 1;
    padding: 0;
    border: 1px solid #fff;
  }
  li.active {
    width: 16px;
    height: 16px;
    background: transparent;
    outline: none;
  }
}
@media (min-width: 576px){
    #banner .carousel-indicators {
        max-width: 540px;
    }
}
@media (min-width: 768px){
    #banner .carousel-indicators {
        max-width: 720px;
    }
}
@media (min-width: 992px){
    #banner .carousel-indicators {
        max-width: 960px;
    }
}
@media (min-width: 1200px){
    #banner .carousel-indicators {
        max-width: 1245px;
    }
}


</style>