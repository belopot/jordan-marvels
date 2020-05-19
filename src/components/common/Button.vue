<template>
  <b-link class="book-now"><slot></slot></b-link>
</template>

<style lang="scss">
a {
  &.book-now {
    background: var(--fifth);
    display: inline-block;
    color: #000;
    font-weight: bold;
    text-decoration: none;
    border-radius: 5px;
    padding: 12px 40px 12px 20px;
    text-transform: uppercase;
    font-size: 14px;
    position: relative;

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
      right: 20px;
      -webkit-transform: translateY(-50%);
      -moz-transform: translateY(-50%);
      transform: translateY(-50%);
    }
    &:hover {
      background: var(--secondary);
    }
  }
}
</style>
