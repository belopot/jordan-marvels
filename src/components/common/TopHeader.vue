<template>
  <b-navbar
    toggleable="lg"
    type
    variant
    class="align-items-stretch p-0 bg-white"
    id="nav"
    :sticky="true"
  >

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    
    <b-navbar-nav>
      <b-nav-item-dropdown text="Lang" class="text-uppercase font-weight-bold languages">
        <b-dropdown-item href="#">EN</b-dropdown-item>
        <b-dropdown-item href="#">ES</b-dropdown-item>
        <b-dropdown-item href="#">RU</b-dropdown-item>
        <b-dropdown-item href="#">FA</b-dropdown-item>
      </b-nav-item-dropdown>
    </b-navbar-nav>
    <b-navbar-brand href="#">
      <div class="d-flex align-items-center h-100">
        <b-img src="@/assets/images/logo.svg" fluid alt="Fluid image"></b-img>
      </div>
    </b-navbar-brand>

    <b-collapse id="nav-collapse" is-nav class="align-items-stretch">
      <b-navbar-nav class="text-uppercase main-nav mx-auto">
        <b-nav-item href="#" active>Home</b-nav-item>
        <b-nav-item href="#">Destinations</b-nav-item>
        <b-nav-item href="#">Stores</b-nav-item>
        <b-nav-item href="#">About Us</b-nav-item>
        <b-nav-item href="#">Help</b-nav-item>
      </b-navbar-nav>
      
      <b-navbar-nav class="text-uppercase font-weight-bold">
        <b-nav-item-dropdown text="USD">
          <b-dropdown-item href="#">INR</b-dropdown-item>
          <b-dropdown-item href="#">SGD</b-dropdown-item>
          <b-dropdown-item href="#">EURO</b-dropdown-item>
        </b-nav-item-dropdown>
        
        <b-nav-item href="#" v-b-modal.sign-up-modal><span class="dropdown-toggle">Sign up</span></b-nav-item>
        <b-nav-item href="#" class="active" v-b-modal.add-review><span class="dropdown-toggle">Get App</span></b-nav-item>
        
      </b-navbar-nav>
    </b-collapse>

  </b-navbar>
</template>
<style lang="scss">
#nav {
  height: 100px;
  border-bottom: 1px solid var(--fourth);

  .dropdown-toggle::after {
    display: block;
    width: 0;
    height: 0;
    margin: auto;
    border-top-width: 0.5em;
    border-right-width: 0.5em;
    border-left-width: 0.5em;
  }
  .dropdown-menu{
    border: 0;
    border-top: 1px solid var(--fourth);
    margin: 0;
    border-radius: 0;
    font-size: 14px;
  }
  .navbar-nav:not(.main-nav) {
    font-size: 12px;
    
    
    > li{
      padding: 0 10px;
      min-width: 80px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-left: 1px solid var(--fourth);

      &:last-child:not(:first-child){
        border-right: 0;
      }

      &.languages{
        border-left: 0;
        border-right: 1px solid var(--fourth);
      }
    }

    a{
      color: #000;
      outline: none;
    }
    > li.active,
    > li:hover{
      background: var(--primary);
      
      > a{color: #fff;}
    }
  }
  > .navbar-nav:not(.main-nav) > li{
    min-width: 0;
  }
  > .navbar-brand{
    padding: 0 25px;
  }

  .navbar-nav.main-nav {
    
    > li{
      margin: 0 15px;
      padding: 0;

      > a {
        padding: 3px;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100%;
        border-top: 5px solid transparent;
      }
    }
    a{ 
      padding: 0;
      color: #000;
      outline: none;
    }
    > li > a.active,
    > li:hover > a{border-color: var(--primary);color: var(--primary);}
    > li > a.active{font-weight: bold;}
    
  }
}
</style>