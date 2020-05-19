<template>
  <div>
    <b-modal id="sign-up-modal" size="lg" content-class="wrapper-auth" body-class="body"
         centered hide-header hide-footer no-stacking>
      <template v-slot:default="{ hide }">
        <a href="javascript:void(0)" class="close-btn" @click="hide()">
          <b-img :src="require(`../../assets/images/icons/close.svg`)"/>
        </a>

        <b-tabs content-class="mt-3">
          <b-tab title="Login" title-item-class="tab-title" title-link-class="tab" active>
            <div class="form-wrapper">
              <b-form class="form">

                <b-input-group class="field-wrap">
                  <template v-slot:prepend>
                    <b-img :src="require(`../../assets/images/icons/email.svg`)" class="ml-2" />
                  </template>
                  <b-input id="email" placeholder="E-mail"></b-input>
                </b-input-group>

                <b-input-group class="field-wrap mt-4">
                  <template v-slot:prepend>
                    <b-img :src="require(`../../assets/images/icons/lock.svg`)" class="ml-2" />
                  </template>
                  <b-input id="password" placeholder="Password"></b-input>
                  <template v-slot:append>
                    <b-img :src="require(`../../assets/images/icons/eye.svg`)" class="mr-2" />
                  </template>
                </b-input-group>

                <div class="text-right">
                  <a href="#" class="forgot-link" v-b-modal.forgot-password>Forgot your Password?</a>
                </div>
                <div class="w-100 text-center submit">
                  <submit>Login</submit>
                </div>
              </b-form>
            </div>
            <div class="divider">
              <div class="divider-title">or login using</div>
            </div>
            <div class="actions">
              <a href="#"><b-img :src="require(`../../assets/images/signup-facebook.svg`)"/></a>
              <a href="#"><b-img :src="require(`../../assets/images/signup-google.svg`)"/></a>
            </div>
          </b-tab>
          <b-tab title="Sign Up" title-item-class="tab-title" title-link-class="tab">
            <div class="form-wrapper">
              <b-form class="form">

                <b-row>
                  <b-col>
                    <b-input-group class="field-wrap">
                      <template v-slot:prepend>
                        <b-img :src="require(`../../assets/images/icons/person.svg`)" class="ml-2" />
                      </template>
                      <b-input id="first_name" placeholder="First Name"></b-input>
                    </b-input-group>
                  </b-col>
                  <b-col>
                    <b-input-group class="field-wrap">
                      <template v-slot:prepend>
                        <b-img :src="require(`../../assets/images/icons/person.svg`)" class="ml-2" />
                      </template>
                      <b-input id="last_name" placeholder="Last Name"></b-input>
                    </b-input-group>
                  </b-col>
                </b-row>

                <b-input-group class="field-wrap">
                  <template v-slot:prepend>
                    <b-img :src="require(`../../assets/images/icons/email.svg`)" class="ml-2" />
                  </template>
                  <b-input id="email" placeholder="E-mail"></b-input>
                </b-input-group>

                <b-input-group class="field-wrap mt-4">
                  <template v-slot:prepend>
                    <b-img :src="require(`../../assets/images/icons/lock.svg`)" class="ml-2" />
                  </template>
                  <b-input id="password" placeholder="Password"></b-input>
                  <template v-slot:append>
                    <b-img :src="require(`../../assets/images/icons/eye.svg`)" class="mr-2" />
                  </template>
                </b-input-group>

                <b-input-group class="field-wrap mt-4">
                  <template v-slot:prepend>
                    <b-img :src="require(`../../assets/images/icons/lock.svg`)" class="ml-2" />
                  </template>
                  <b-input id="password" placeholder="Confirm your Password"></b-input>
                  <template v-slot:append>
                    <b-img :src="require(`../../assets/images/icons/eye.svg`)" class="mr-2" />
                  </template>
                </b-input-group>

                <b-input-group class="field-wrap mb-3">
                  <template v-slot:prepend>
                    <b-img :src="require(`../../assets/images/icons/calendar.svg`)" class="ml-2" />
                  </template>
                  <b-input id="calendar" placeholder="Date of Birth*"></b-input>
                  <template v-slot:append>
                    <b-input-group-text class="append">DD/MM/YYYY</b-input-group-text>
                  </template>
                </b-input-group>

                <div class="text-left">
                  <a href="#" class="forgot-link">
                    <b-img :src="require(`../../assets/images/icons/checkbox.svg`)"/>
                    <span class="ml-2 terms">I agree to the terms and conditions</span>
                  </a>
                </div>
                <div class="w-100 text-center submit">
                  <submit>Sign Up</submit>
                </div>
              </b-form>
            </div>
            <div class="divider">
              <div class="divider-title">or sign in using</div>
            </div>
            <div class="actions">
              <a href="#"><b-img :src="require(`../../assets/images/signup-facebook.svg`)"/></a>
              <a href="#"><b-img :src="require(`../../assets/images/signup-google.svg`)"/></a>
            </div>
          </b-tab>
        </b-tabs>
      </template>
    </b-modal>
  </div>
</template>

<script>
import Button from "../common/SimpleButton";
export default {
  name: "SignUpModal",
  components: {
    "submit": Button
  }
};
</script>

<style lang="scss">
.wrapper-auth {
  border-radius: 4px;

  .body {
    padding: 0;

    .close-btn {
      position: absolute;
      z-index: 1200;
      top: 42px;
      right: 42px;
    }
    .tab-title {
      width: 50%;
      height: 105px;

      .tab {
        border: none;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        color: var(--seventh);
        font-size: 44px;
        font-weight: bold;
        border-bottom: 1px solid var(--eighth);
        outline: none;

        &.active {
          color: var(--tertiary);
          border-bottom: 3px solid var(--secondary);
        }
      }
    }
    .form-wrapper {
      width: 100%;
      display: flex;
      justify-content: center;
      padding: 40px 0 45px;

      .form {
        width: 50%;
      }
      .submit {
        margin-top: 50px;
      }
      .forgot-link {
        font-size: 14px;
        color: var(--seventh);
        &:hover {
          text-decoration: none;
        }
      }
      .append {
        font-size: 14px;
        color: var(--seventh);
        background: none;
        border: none;
      }
      .terms {
        font-size: 11px;
        color: var(--seventh);
      }
    }
    .divider {
      width: 100%;
      display: flex;
      justify-content: center;
      position: relative;
      background-image: url(../../assets/images/divider_line.svg);
      background-position: center;
      background-repeat: repeat-x;

      .divider-title {
        font-size: 11px;
        text-transform: uppercase;
        color: var(--seventh);
        font-weight: bold;
        background: #fff;
        padding: 0 40px;
      }
    }
    .actions {
      height: 120px;
      display: flex;
      justify-content: space-around;
      align-items: center;
      padding: 0 20%;
    }
    .field-wrap {
      border-bottom: 1px solid var(--seventh);
      margin-bottom: 10px;
      width: 100%;

      input {
        border-color: transparent;
        font-size: 14px;
        color: #000;
        outline: none;

        &:focus {
          border-color: transparent;
          outline: none !important;
        }
      }
    }
  }
}
</style>
