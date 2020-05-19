<template>
  <div id="app">
    <top-header></top-header>
    <router-view />
    <sign-up-modal></sign-up-modal>
    <add-review></add-review>
    <reset-password></reset-password>
    <footer>
      <top-footer></top-footer>
      <bottom-footer></bottom-footer>
    </footer>
  </div>
</template>

<script>
import TopHeader from "./components/common/TopHeader.vue";
import TopFooter from "./components/common/TopFooter";
import BottomFooter from "./components/common/BottomFooter";
import SignUpModal from './components/modals/SignUpModal';
import AddReview from './components/modals/AddReview';
import ResetPassword from './components/modals/ResetPassword';

export default {
  components: {
    "sign-up-modal": SignUpModal,
    "add-review": AddReview,
    "reset-password": ResetPassword,
    "top-header": TopHeader,
    "top-footer": TopFooter,
    "bottom-footer": BottomFooter
  }
};
</script>
