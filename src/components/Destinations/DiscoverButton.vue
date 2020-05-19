<template>
  <b-link class="btn-discover"><slot></slot></b-link>
</template>

<style lang="scss">
a {
  &.btn-discover {
    width: 100%;
    height: 100px;
    background: var(--fifth);
    display: inline-block;
    color: #000;
    font-weight: bold;
    text-align: center;
    text-decoration: none;
    border-radius: 5px;
    padding: 38px 40px 12px 20px;
    text-transform: uppercase;
    font-size: 18px;
    position: relative;
  }
}
</style>
