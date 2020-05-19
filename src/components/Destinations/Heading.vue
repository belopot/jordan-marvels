<template>
  <b-container class="title-container">
    <b-row class="align-items-center mb-4">
      <b-col cols="9"
        ><h1 class="title-1 text-left mb-0">{{ heading }}</h1></b-col
      >
      <b-col cols="3 text-right">
        <a class="btnlink" :href="`${btnLink}`">{{ btnText }} </a>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: "Heading",
  props: {
    heading: String,
    btnText: String,
    btnLink: String
  }
};
</script>

<style lang="scss">
.btnlink {
  padding-right: 25px;
  margin-right: 20px;
  display: inline-block;
  color: var(--tertiary);
  font-weight: bold;
  text-decoration: none;
  text-transform: uppercase;
  position: relative;
  font-size: 13px;

  &::after {
    content: "";
    background-image: url("../../assets/images/btn_right_arrow.svg");
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center;
    width: 9px;
    height: 14px;
    position: absolute;
    top: 50%;
    right: 0;
    -webkit-transform: translateY(-50%);
    -moz-transform: translateY(-50%);
    transform: translateY(-50%);
  }
  &:hover {
    text-decoration: none;
    color: var(--secondary);
  }
}
</style>
