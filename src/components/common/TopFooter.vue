<template>
  <div id="top-footer" class="text-left">
    <b-container>
      <b-row>
        <b-col cols="3">
          <div class="block">
            <h6 class="title">Destinations</h6>
            <ul>
              <li>
                <b-button variant="link">Petra</b-button>
              </li>
              <li>
                <b-button variant="link">Dead Sea</b-button>
              </li>
              <li>
                <b-button variant="link">Amman</b-button>
              </li>
              <li>
                <b-button variant="link">Magic Bedouin Star</b-button>
              </li>
            </ul>
          </div>
        </b-col>

        <b-col cols = "3">
          <div class="block">
            <h6 class="title">ABOUT US</h6>
            <ul>
              <li>
                <b-button variant="link">Our agenda</b-button>
              </li>
              <li>
                <b-button variant="link">Benefits</b-button>
              </li>
              <li>
                <b-button variant="link">Contact</b-button>
              </li>
            </ul>
          </div>
        </b-col>

        <b-col cols="3">
          <div class="block">
            <h6 class="title">HELP</h6>
            <ul>
              <li>
                <b-button variant="link">Payments</b-button>
              </li>
              <li>
                <b-button variant="link">Frequenty Asked Questions</b-button>
              </li>
              <li>
                <b-button variant="link">Support Service</b-button>
              </li>
              <li>
                <b-button variant="link">Guanrantee</b-button>
              </li>
            </ul>
          </div>
        </b-col>

        <b-col cols="3">
          <div class="block">
            <img class="mb-5" src="@/assets/images/footer_logo.svg" />
            <img src="@/assets/images/footer_payment.svg" />
          </div>
        </b-col>
      </b-row>
      
    </b-container>
  </div>
</template>

<script>
export default {
  name: "TopFooter"
};
</script>

<style lang="scss">
#top-footer {
  background: var(--sixth);
  padding: 50px 0;
  color: #fff;
  font-weight: 300;
  font-size: 16px;
    
  .block .title{
    font-size: 14px;
    font-weight: bold;
    text-transform: uppercase;
    margin-bottom: 20px;
  }
  .block ul{
    list-style: none;
    margin: 0;
    padding: 0;
  }
  .block ul li{
    margin-bottom: 8px;
  }
  .block button{
    padding: 0;
    color: inherit;
    font-weight: inherit;
    font-size: inherit;
    opacity: 0.85;
    text-transform: capitalize;

    &:hover{
      opacity: 1;
      text-decoration: none;
    }
  }
}
</style>
