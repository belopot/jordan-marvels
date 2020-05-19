<template>
  <div id="bottom-footer" class="text-left">
    <b-container>
      <b-row class="align-items-center">
        <b-col cols="3">
          <div class="block">
            <img src="@/assets/images/bottom_footer_icon1.svg" />
          </div>
        </b-col>

        <b-col cols = "3">
          <div class="block">
            <img src="@/assets/images/bottom_footer_icon2.svg" />
          </div>
        </b-col>

        <b-col cols="3">
          <div class="block">
            <img src="@/assets/images/bottom_footer_icon3.svg" />
          </div>
        </b-col>

        <b-col cols="3">
          <div class="block">
            <img src="@/assets/images/bottom_footer_icon4.svg" />
          </div>
        </b-col>
      </b-row>

      <b-row class="mt-5">
        <b-col cols="9">
          <div class="copyright">
            Copyright 2020. All Rights Reserved.
          </div>
        </b-col>
        <b-col cols="3">
          <div class="block">
            <a href="javascript:void(0)" class="mr-5">Terms of use</a>

            <a href="javascript:void(0)">Privacy Policy</a>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "BottomFooter"
};
</script>

<style lang="scss">
#bottom-footer {
  background: #fff;
  padding-top: 35px;
  padding-bottom: 15px;
  font-weight: 600;
  font-size: 14px;
  color: var(--sixth);
  text-transform: uppercase;
    
  .copyright{
    font-size: 13px;
    text-transform: none;
  }
  a{
    color: inherit;

    &:hover{color: var(--secondary);text-decoration: none;}
  }
}
</style>
