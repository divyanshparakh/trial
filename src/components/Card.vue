<template>
  <div class="card">
    <div>
      <img
        id="logo"
        src="@/assets/iconfinder_secure-server_4417098.png"
        draggable="false"
        height="200px"
      />
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  props: {},
  data() {
    return {};
  },
  computed: {},
  methods: {},
  created() {},
  mounted() {}
};
</script>

<style lang="scss" scoped>
.card {
  position: absolute;
  top: 10vh;
  left: 15%;
  right: 50%;
  font-size: 16px;
  color: brown;
  height: 70vh;
  width: 20em;
  margin: auto;
  background-color: hsla(50, 25%, 65%, 0.7);
  overflow: hidden;
}

@media only screen and (min-width: 600px) {
  /* For tablets: */
  .card {
    top: 10%;
    left: 25vw;
    font-size: 18px;
    width: 50vw;
  }
}

@media only screen and (min-width: 768px) {
  /* For desktop: */
  .card {
    top: 10%;
    left: 34%;
    font-size: 24px;
    max-height: 80vh;
    max-width: 25em;
  }
}
</style>
