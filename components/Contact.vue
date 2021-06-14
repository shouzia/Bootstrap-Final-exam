<template>
  <div id="Contact" class="Contact-us">
    <div class="Contact-body">
      <div class="Contact-title mx-auto text-center">
        <h2 class="member-title">联系我们</h2>
        <br />
        <p><i>我们热爱我们的粉丝</i></p>
        <div class="row text-left Contact-boyd-icon">
          <div class="Contact-Body-text">
            <p>喜欢我们，就给我们留言吧</p>
            <p><b-icon-X></b-icon-X>武汉*中国</p>
            <p><b-icon-phone></b-icon-phone>电话:15979899465</p>
            <p><b-icon-mailbox></b-icon-mailbox>武汉*中国</p>
          </div>
          <div style="min-width: 75%">
            <div class="row mx-0 mb-3">
              <b-form-input
                style="width: 45%"
                class="mx-auto"
                id="input-2"
                placeholder="Name"
                required
              ></b-form-input
              ><b-form-input
                style="width: 45%"
                class="mx-auto"
                id="input-2"
                placeholder="Email"
                required
              ></b-form-input>
            </div>
            <b-form-textarea
              class="mx-auto"
              style="width: 95%"
              id="textarea-default"
              placeholder="Comment"
              rows="3"
            ></b-form-textarea>
            <b-button variant="outline-primary" class="mt-3 mr-3 float-right"
              >发送</b-button
            >
          </div>
        </div>
      </div>
      <div id="BaiduMap"></div>
    </div>
  </div>
</template>

<script>
import { BIcon, BIconX, BIconPhone, BIconMailbox } from "bootstrap-vue";
export default {
  components: {
    BIcon,
    BIconX,
    BIconPhone,
    BIconMailbox,
  },
  mounted() {
    let map = new BMap.Map("BaiduMap");
    map.centerAndZoom(new BMap.Point(114.309531, 30.59619), 50);
    map.addControl(new BMap.MapTypeControl());
    map.setCurrentCity("武汉");
    map.enableScrollWheelZoom(true);
  },
};
</script>

<style>
.Contact-us {
  width: 100%;
  min-height: 100vh;
}
.Contact-body {
  width: 100%;
  height: 100%;
}
.Contact-title {
  width: 90%;
  height: 70%;
  padding: 10%;
}
.Contact-boyd-icon {
  font-size: 1.2rem;
}
#BaiduMap {
  width: 100%;
  height: 30%;
}
.Contact-Body-text {
  width: 25%;
}
@media screen and (max-width: 1100px) {
  .Contact-Body-text {
    width: 100%;
  }
}
</style>