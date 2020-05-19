<template>
  <div>
    <b-modal id="reset-password" size="lg" content-class="wrapper" body-class="body" centered hide-header hide-footer>
      <template v-slot:default="{ hide }">
        <a href="javascript:void(0)" class="close-btn" @click="hide()">
          <b-img :src="require(`../../assets/images/icons/close.svg`)"/>
        </a>

        <div class="modal-title">Reset Password</div>
        <div class="text-center w-100">
            <div class="subtitle">
              Forgot your password? No worries. Just enter the email you used to sign up and we'll send you a link to reset it
            </div>
        </div>
        <div class="form-wrapper">
          <b-form class="form">

            <b-input-group class="field-wrap">
              <template v-slot:prepend>
                <b-img :src="require(`../../assets/images/icons/email.svg`)" class="ml-2" />
              </template>
              <b-input id="email" placeholder="E-mail"></b-input>
            </b-input-group>

            <div class="w-100 text-center submit">
              <submit>Reset Password</submit>
            </div>

          </b-form>
        </div>
      </template>
    </b-modal>
  </div>
</template>

<script>
import Button from "../common/SimpleButton";
export default {
  name: "ResetPassword",
  components: {
    "submit": Button
  }
};
</script>

<style lang="scss">
.wrapper {
  border-radius: 4px;
  padding: 55px 0 60px;
  position: relative;

  .body {
    padding: 0;

    .modal-title {
      color: var(--tertiary);
      width: 100%;
      font-size: 44px;
      font-weight: bold;
      text-align: center;
    }
    .subtitle{
      font-size: 14px;
      color: var(--primary);
      max-width: 60%;
      margin: auto;
    }
    .close-btn {
      position: absolute;
      z-index: 1200;
      top: 22px;
      right: 42px;
    }
    .form-wrapper {
      width: 100%;
      display: flex;
      justify-content: center;
      padding: 40px 0 0;

      .form {
        width: 50%;
      }
      .submit {
        margin-top: 50px;
      }
      .append {
        font-size: 14px;
        color: var(--seventh);
        background: none;
        border: none;
      }
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
    .textarea-wrap {
      border: 2px solid var(--primary);
      font-size: 14px;
      color: #000;
      height: 100px;
      border-radius: 0;

      &::placeholder {
        font-size: 12px;
        color: var(--seventh);
      }
    }
    .left-column {
      width: 170px;
      max-width: 170px;
    }
  }
}
</style>
