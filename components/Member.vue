<template>
  <div class="member mx-auto">
    <div class="text-center px-2">
      <h2 class="member-title">我们的成员</h2>
      <br />
      <p>我们爱音乐！</p>
      <br />
      <p>
        XXX乐队由一群热爱
        音乐的年轻人组成。成立两年来，已经成为校园炙手可热的新生代摇滚团体。
        他们的音乐风格为流行朋克，旋律动听，节奏轻快。在经过多场演出的磨练之后，XXX乐队凭借着阳光健康的形象、
        充满活力的现场演出征服了许多年轻人，他们已成为目前中国校园里最受欢迎的乐队。
      </p>
    </div>
    <div class="row text-center my-5">
      <div v-for="item in proson" :key="item.name" class="member-son mx-auto">
        <h2>{{ item.name }}</h2>
        <img class="tximg" :src="item.imgsrc" alt="" />
        <br /><br />
        <p>
          {{ item.job }}
        </p>
        <p>
          <span> {{ item.data }}&nbsp;&nbsp;{{ item.addres }}</span>
        </p>
        <p>{{ item.Introduction }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import tx1 from "~/assets/tx1.jpg";
import tx2 from "~/assets/tx2.jpg";
import tx3 from "~/assets/tx3.jpg";
export default {
  data() {
    return {
      proson: [
        {
          name: "Shouzi",
          imgsrc: tx1,
          job: "主唱",
          data: "1998-08-26",
          addres: "江西新余人",
          Introduction: "擅长动人的抒情歌曲，喜欢RB，POP等风格",
        },
        {
          name: "ei",
          imgsrc: tx2,
          job: "主唱",
          data: "1998-08-26",
          addres: "江西新余人",
          Introduction: "擅长动人的抒情歌曲，喜欢RB，POP等风格",
        },
        {
          name: "Shi",
          imgsrc: tx3,
          job: "主唱",
          data: "1998-08-26",
          addres: "江西新余人",
          Introduction: "擅长动人的抒情歌曲，喜欢RB，POP等风格",
        },
      ],
    };
  },
};
</script>

<style>
.member {
  width: 80%;
  min-height: 100vh;
  padding-top: 7rem;
}
.member-son {
  max-width: 100%;
}
.tximg {
  width: 200px;
  border-radius: 200px;
}
.member-title {
  letter-spacing: 15px;
  text-indent: 15px;
}
</style>