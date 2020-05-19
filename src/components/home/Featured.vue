<template>
  <section class="text-left">
    <heading
      heading="Featured Programs"
      btnText="View All"
      btnLink="#"
    ></heading>

    <div class="featured-wrap">
      <b-container>
        <b-row>
          <b-col>
            <carousel :items="4" :nav="true" :dots="false" :margin="20">
              <div class="featured-box">
                <h2>Weekend In Joradn</h2>
                <figure>
                  <div class="image-div"><img src="../../assets/0015.png" alt="" /></div>
                  <figcaption>
                    <div class="price-start">
                      starting from <strong> $240</strong>,00
                    </div>
                    <book-now-btn>Book Now</book-now-btn>
                  </figcaption>
                </figure>
              </div>
              <div class="featured-box">
                <h2>Weekend In Joradn</h2>
                <figure>
                  <div class="image-div"><img src="../../assets/0016.png" alt="" /></div>
                  <figcaption>
                    <div class="price-start">
                      starting from <strong> $240</strong>,00
                    </div>
                    <book-now-btn>Book Now</book-now-btn>
                  </figcaption>
                </figure>
              </div>
              <div class="featured-box">
                <h2>Weekend In Joradn</h2>
                <figure>
                  <div class="image-div"><img src="../../assets/0017.png" alt="" /></div>
                  <figcaption>
                    <div class="price-start">
                      starting from <strong> $240</strong>,00
                    </div>
                    <book-now-btn>Book Now</book-now-btn>
                  </figcaption>
                </figure>
              </div>
              <div class="featured-box">
                <h2>Weekend In Joradn</h2>
                <figure>
                  <div class="image-div"><img src="../../assets/0018.png" alt="" /></div>
                  <figcaption>
                    <div class="price-start">
                      starting from <strong> $240</strong>,00
                    </div>
                    <book-now-btn>Book Now</book-now-btn>
                  </figcaption>
                </figure>
              </div>
              <div class="featured-box">
                <h2>Weekend In Joradn</h2>
                <figure>
                  <div class="image-div"><img src="../../assets/0015.png" alt="" /></div>
                  <figcaption>
                    <div class="price-start">
                      starting from <strong> $240</strong>,00
                    </div>
                    <book-now-btn>Book Now</book-now-btn>
                  </figcaption>
                </figure>
              </div>
              <div class="featured-box">
                <h2>Weekend In Joradn</h2>
                <figure>
                  <div class="image-div"><img src="../../assets/0015.png" alt="" /></div>
                  <figcaption>
                    <div class="price-start">
                      starting from <strong> $240</strong>,00
                    </div>
                    <book-now-btn>Book Now</book-now-btn>
                  </figcaption>
                </figure>
              </div>
            </carousel>
          </b-col>
        </b-row>
      </b-container>
    </div>
  </section>
</template>

<script>
import carousel from "vue-owl-carousel";
import Button from "../common/Button";
import heading from "./Heading";

export default {
  components: { carousel, "book-now-btn": Button, heading }
};
</script>

<style lang="scss">
.featured-box {
  position: relative;
  padding: 20px 0;
  
  h2 {
    font-size: 16px;
    text-transform: uppercase;
    color: #000;
    text-align: center;
    font-weight: bold;
  }
  figure {
    position: relative;
    
    .image-div{overflow: hidden;}
    img{
      -webkit-transition: all ease 0.3s;
      -moz-transition: all ease 0.3s;
      transition: all ease 0.3s;
    }
    &:hover img{
      -webkit-transform: scale(1.2);
      -moz-transform: scale(1.2);
      transform: scale(1.2);
    }
    figcaption {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      padding: 20px;
      a {
        right: 20px;
        bottom: -30px;
        position: absolute;
      }
      .price-start {
        color: #fff;
        position: absolute;
        right: 20px;
        bottom: 30px;
        font-weight: 300;
        font-size: 14px;

        strong {
          font-size: 30px;
          font-weight: bold;
        }
      }
    }
  }
}
.featured-wrap{
  position: relative;

  .container > .row > div{position: static;}
  .owl-carousel{position: static;}
  .owl-nav .owl-prev,
  .owl-nav .owl-next {
    position: absolute;
    top: 10%;
    left: 0;
    width: 100px;
    height: 81%;
    border-radius: 0 !important;
    margin: 0 !important;
    padding: 0 !important;
    font-size: 0 !important;
    display: flex !important;
    align-items: center;
    justify-content: center;
    background: var(--fifth) !important;

    &:hover{
      background: var(--secondary) !important;
    }
  }
  .owl-nav .owl-next{
    right: 0;
    left: auto;
  }
  .owl-nav .owl-prev:before{
    content:"";
    display: block;
    width: 22px;
    height: 39px;
    background-image: url("../../assets/images/featured_arrow_left.svg");
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center;
  }
  .owl-nav .owl-next:before{
    content:"";
    display: block;
    width: 22px;
    height: 39px;
    background-image: url("../../assets/images/featured_arrow_right.svg");
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center;
  }
}
</style>
