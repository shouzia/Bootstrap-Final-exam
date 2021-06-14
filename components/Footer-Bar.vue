<template>
  <div class="footer text-center py-3">
    <a
      style="color: #fff"
      v-scroll-to="{
        el: '#Home',
      }"
    >
      <b-icon-chevron-up></b-icon-chevron-up
    ></a>
    <h2>BootStrap</h2>
  </div>
</template>

<script>
import { BIcon, BIconChevronUp } from "bootstrap-vue";

export default {
  components: {
    BIcon,
    BIconChevronUp,
  },
};
</script>

<style>
.footer {
  width: 100%;
  height: 150px;
  font-size: 28px;
  text-decoration: none;
  background-color: #2d2d2d;
  color: white;
}
</style>