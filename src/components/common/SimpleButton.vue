<template>
  <b-link class="button"><slot></slot></b-link>
</template>

<style lang="scss">
a {
  &.button {
    height: 45px;
    min-width: 200px;
    width: auto;
    margin: auto;
    background: var(--secondary);
    color: #000;
    font-weight: bold;
    text-decoration: none;
    border-radius: 5px;
    padding: 0 75px;
    font-size: 20px;
    line-height: 45px;
    display: inline-block;

    &:hover {
      background: var(--secondary);
    }
  }
}
</style>
