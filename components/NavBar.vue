<template>
  <div class="NavBar-Color">
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <b-navbar-brand href="#">NavBar</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-navbar-nav v-for="item in NavData" :key="item.href">
            <b-nav-item
              v-scroll-to="{
                el: item.href,
              }"
              >{{ item.title }}</b-nav-item
            >
          </b-navbar-nav>

          <b-nav-item-dropdown text="更多" right>
            <b-dropdown-item href="#">专辑</b-dropdown-item>
            <b-dropdown-item href="#">单曲</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>


//  v-scroll-to="{
//                 el: item.Navhref,
//                 offset: -280,
//               }"
<script>
export default {
  data() {
    return {
      NavData: [
        {
          title: "主页",
          href: "#Home",
        },
        {
          title: "成员",
          href: "#Member",
        },
        {
          title: "巡演",
          href: "#Touring",
        },
        {
          title: "联系我们",
          href: "#Contact",
        },
      ],
    };
  },
};
</script>

<style>
.NavBar-Color {
  background: rgba(128, 128, 128, 0.8);
  width: 100%;
  z-index: 1000;
  position: fixed;
  left: 0%;
  top: 0%;
}
</style>