<template>
  <div class="BIg-Buy" v-show="flag">
    <div class="Buy">
      <div
        class="
          Buy-title
          text-center
          d-flex
          justify-content-center
          align-items-center
        "
      >
        <b-icon-lock-fill></b-icon-lock-fill>
        <h2>Tickets</h2>
        <b-icon-X class="b-icon-x" @click="Sms"></b-icon-X>
      </div>
      <div class="Buy-body text-left px-5 py-3">
        <div class="my-3">
          <b-icon-cart style="font-size: 20px"></b-icon-cart
          ><span>Tickets,每人23元</span>
          <b-form-input
            id="input-2"
            placeholder="How Many?"
            required
          ></b-form-input>
        </div>
        <div class="my-3">
          <b-icon-Person></b-icon-Person>
          <span>发送</span>
          <b-form-input
            id="input-2"
            placeholder="Enter Email"
            required
          ></b-form-input>
        </div>
        <div class="my-3">
          <b-button variant="success" style="width: 100%"
            ><b-icon-Check></b-icon-Check>支付</b-button
          >
        </div>
        <div class="my-5 d-flex justify-content-center align-items-center">
          <div style="min-width: 50%">
            <b-button variant="danger" @click="Sms">
              <b-icon-X></b-icon-X>
              取消
            </b-button>
          </div>
          <div style="min-width: 50%" class="text-right">
            <span><a href="#">需要</a>帮助？</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {
  BIcon,
  BIconLockFill,
  BIconX,
  BIconCart,
  BIconPerson,
  BIconCheck,
} from "bootstrap-vue";

export default {
  components: {
    BIcon,
    BIconLockFill,
    BIconX,
    BIconCart,
    BIconPerson,
    BIconCheck,
  },

  data() {
    return {
      flag: false,
    };
  },
  methods: {
    Sms() {
      this.flag != this.flag;
      this.$emit("ObtainMessage", this.flag);
    },
  },
};
</script>

<style>
.BIg-Buy {
  width: 100%;
  height: 100vh;
  background: transparent;
  position: fixed;
  top: 0;
  z-index: 100000;
  left: 0;
}
.Buy {
  width: 40%;
  height: 60%;
  background: white;
  position: fixed;
  left: 30%;
  top: 20%;
}
@media screen and (max-width: 980px) {
  .Buy {
    width: 100%;
    height: 60%;
    background: white;
    position: fixed;
    left: 0%;
    top: 20%;
  }
}
.Buy-title {
  width: 100%;
  height: 30%;
  background: #2d2d2d;
}
.Buy-body {
  width: 100%;
  height: 70%;
  color: black;
}
.b-icon-x {
  font-size: 2rem;
  position: absolute;
  right: 20px;
  top: 20px;
}
</style>