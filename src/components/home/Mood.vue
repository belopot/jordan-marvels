<template>
  <b-col cols="8" class="mood-component">
    <h1 class="title-1">What's your mood?</h1>

    <b-row>
      <b-col cols="6">
        <figure>
          <b-img src="../../assets/0011.png" fluid alt="Responsive image"></b-img>

          <figcaption>
            <h1>Gateway with friends</h1>
            <b-link>86 Destinations</b-link>
          </figcaption>
        </figure>
      </b-col>
      <b-col cols="6">
        <figure>
          <b-img src="../../assets/0012.png" fluid alt="Responsive image"></b-img>

          <figcaption>
            <h1>Gateway with friends</h1>
            <b-link>86 Destinations</b-link>
          </figcaption>
        </figure>
      </b-col>

      <b-col cols="6">
        <figure>
          <b-img src="../../assets/0013.png" fluid alt="Responsive image"></b-img>

          <figcaption>
            <h1>Gateway with friends</h1>
            <b-link>86 Destinations</b-link>
          </figcaption>
        </figure>
      </b-col>
      <b-col cols="6">
        <figure>
          <b-img src="../../assets/0014.png" fluid alt="Responsive image"></b-img>

          <figcaption>
            <h1>Gateway with friends</h1>
            <b-link>86 Destinations</b-link>
          </figcaption>
        </figure>
      </b-col>
    </b-row>
  </b-col>
</template>

<style lang="scss">
.mood-component {
  .row {
    margin-left: -10px;
    margin-right: -10px;

    > div{
      padding: 0 10px 20px;
    }
  }
  figure {
    position: relative;
    margin: 0;
    overflow: hidden;

    img{
      width: 100%;
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
      text-align: right;
      bottom: 0;
      width: 100%;
      padding: 20px;

      h1 {
        color: #fff;
        font-size: 24px;
        font-weight: bold;
        line-height: 1.1;
      }
      a {
        display: inline-flex;
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
}
</style>