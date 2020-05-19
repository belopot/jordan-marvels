<template>
  <b-col cols="4" class="traveling">
    <div class="travel-wrap">
      <h1 class="title-1 text-left">Traveling with us</h1>
      <div class="home-beniffit">
        <ul>
          <li>
            Discover Genuine
            <br />Experiences
          </li>
          <li>
            Secure and
            <br />Safe Payments
          </li>
          <li>
            Give back and
            <br />Have Fun
          </li>
        </ul>
      </div>
      <book-now-btn>All Benefits</book-now-btn>
    </div>
  </b-col>
</template>
<script>
import Button from "../common/Button";
export default {
  components: {
    "book-now-btn": Button
  }
};
</script>
<style lang="scss">
.travel-wrap {
  position: relative;
  a {
    position: absolute;
    bottom: -10px;
    right: 30px;
  }
}
.home-beniffit {
  padding: 40px 40px 100px 40px;
  background-image: url(../../assets/images/benefits_bg_long.svg);
  background-position: top right;
  background-size: auto 100%;
  background-repeat: no-repeat;

  ul {
    margin: 0;
    padding: 0;
    list-style: none;
    li {
      padding-left: 80px;
      color: var(--tertiary);
      font-size: 20px;
      font-weight: bold;
      text-align: left;
      margin-bottom: 30px;
      &:nth-child(1) {
        background: url(../../assets/images/discover.svg) no-repeat -12px;
        background-size: 74px;
      }
      &:nth-child(2) {
        background: url(../../assets/images/secure_payment.svg) no-repeat center left;
        background-size: 55px;
      }
      &:nth-child(3) {
        background: url(../../assets/images/giveback.svg) no-repeat center left;
        background-size: 55px;
      }
    }
  }
}
</style>
