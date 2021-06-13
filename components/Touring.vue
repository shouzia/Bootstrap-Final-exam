<template>
  <div class="Touring text-center">
    <div class="mx-auto Touring-min-box">
      <h2 class="member-title">巡演日期</h2>
      <br />
      <i>我门将会演绎自己的音乐。</i><br /><br />
      <i> 快来购票吧！</i>

      <div class="mt-3">
        <b-list-group style="color: #000" class="text-left">
          <b-list-group-item v-for="(item, index) in list" :key="item.data">
            {{ item.data }}
            <b-badge
              :variant="index <= 1 ? 'danger' : 'dark'"
              :class="index == 2 ? 'float-right' : ''"
              pill
            >
              {{ item.message }}</b-badge
            >
          </b-list-group-item>
          <div class="row" style="margin: 0; background-color: #fff">
            <div
              v-for="item in boxs"
              :key="item.addres"
              class="text-center mx-auto my-3"
              style="max-width: 100%; min-width: 33.3%"
            >
              <img :src="item.imgsrc" alt="" width="200px" />
              <i>
                <h4>{{ item.addres }}</h4>
                <p>{{ item.data }}</p>
              </i>
              <b-button variant="outline-primary" @click="flag = !flag">{{
                item.btntext
              }}</b-button>
            </div>
          </div>
        </b-list-group>
      </div>
    </div>
    <Buy v-show="flag" v-on:ObtainMessage="ShowFlag" />
  </div>
</template>

<script>
import tx1 from "~/assets/tx1.jpg";
import tx2 from "~/assets/tx2.jpg";
import tx3 from "~/assets/tx3.jpg";
import Buy from "./Buy.vue";
export default {
  components: { Buy },
  data() {
    console.log(this.flag);
    return {
      list: [
        { data: "September ", message: "售空！" },
        { data: "October ", message: "售空！" },
        { data: "November ", message: "3" },
      ],
      boxs: [
        {
          imgsrc: tx1,
          addres: "北京",
          data: "Set. 28 November 2017",
          btntext: "购票",
        },
        {
          imgsrc: tx2,
          addres: "上海",
          data: "Set. 29 November 2017",
          btntext: "购票",
        },
        {
          imgsrc: tx3,
          addres: "武汉",
          data: "Set. 27 November 2017",
          btntext: "购票",
        },
      ],
      flag: "",
    };
  },
  methods: {
    ShowFlag(data) {
      this.flag = data;
      // console.log(data);
    },
  },
};
</script>

<style>
.Touring {
  width: 100%;
  min-height: 100vh;
  background: black;
  color: white;
  padding: 5.5rem 0;
}
.Touring-min-box {
  width: 80%;
}
</style>