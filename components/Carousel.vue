<template>
  <div id="Home" class="Carousel-Box">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="100vh"
      style="text-shadow: 1px 1px 2px #333; height: 100%"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide
        caption="北京"
        text="我们来了"
        img-src="https://picsum.photos/1024/480/?image=52"
      ></b-carousel-slide>

      <b-carousel-slide
        caption="武汉"
        text="T一夜"
        img-src="https://picsum.photos/1024/480/?image=52"
      ></b-carousel-slide>

      <b-carousel-slide
        caption="123"
        text="123123"
        img-src="https://picsum.photos/1024/480/?image=52"
      ></b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null,
    };
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
    },
    onSlideEnd(slide) {
      this.sliding = false;
    },
  },
};
</script>


<style>
.Carousel-Box {
  width: 100%;
  height: 100vh;
}
.img-fluid {
  height: 100vh;
  object-fit: cover;
}
</style>