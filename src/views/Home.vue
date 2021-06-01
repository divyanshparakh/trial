<template>
  <div class="home">
    <particles-bg
      color="#ffcd05"
      class="particles-bg"
      type="cobweb"
      num="100"
      :bg="true"
    />
    <Card><LR :F="false"></LR></Card>
  </div>
</template>

<script>
import { ParticlesBg } from "particles-bg-vue";
import Card from "@/components/Card";
import LR from "@/components/LR/LR";

export default {
  name: "Home",
  components: {
    ParticlesBg,
    Card,
    LR
  }
};
</script>
<style media="screen">
.particles-bg {
  /* background: url("https://maggenta.com/media/product/1056/black-white-world-map-with-country-names-written-wall-mural_1.jpg"); */
  /* background: url("https://wallpaperaccess.com/full/2603347.jpg"); */
  background-image: url("https://c4.wallpaperflare.com/wallpaper/685/901/258/orange-the-world-black-background-world-map-hd-wallpaper-preview.jpg");
  background-position: center;
  background-attachment: fixed;
  background-size: cover;
}
</style>
