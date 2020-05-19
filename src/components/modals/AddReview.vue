<template>
  <div>
    <b-modal id="add-review" size="lg" content-class="wrapper-review" body-class="body" centered hide-header hide-footer>
      <template v-slot:default="{ hide }">
        <a href="javascript:void(0)" class="close-btn" @click="hide()">
          <b-img :src="require(`../../assets/images/icons/close.svg`)"/>
        </a>

        <div class="modal-title">Add Your Review</div>
        <div class="text-center">
            <span class="ml-2 subtitle">I agree to the terms and conditions</span>
        </div>
        <div class="form-wrapper">
          <b-row>
            <b-col class="left-column">
              <a href="javascript:void(0)">
                <b-img :src="require(`../../assets/images/icons/empty_photo.svg`)" class="" />
              </a>
            </b-col>
            <b-col>
              <b-form class="form">

                <b-input-group class="field-wrap mb-3">
                  <template v-slot:prepend>
                    <b-img :src="require(`../../assets/images/icons/person.svg`)" class="ml-2" />
                  </template>
                  <b-input id="name" placeholder="Name"></b-input>
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

                <b-input-group class="field-wrap mb-3">
                  <template v-slot:prepend>
                    <b-img :src="require(`../../assets/images/icons/age.svg`)" class="ml-2" />
                  </template>
                  <b-input id="age" placeholder="Age"></b-input>
                </b-input-group>

                <b-form-textarea
                  id="text"
                  placeholder="Enter Review Content"
                  class="textarea-wrap"
                ></b-form-textarea>

                <div class="w-100 text-left submit">
                  <submit>Add Review</submit>
                </div>

              </b-form>
            </b-col>
          </b-row>
        </div>
      </template>
    </b-modal>
  </div>
</template>

<script>
import Button from "../common/SimpleButton";
export default {
  name: "AddReview",
  components: {
    "submit": Button
  }
};
</script>

<style lang="scss">
.wrapper-review {
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
        width: 100%;
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
