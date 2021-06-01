<template>
  <div id="navbar">
    <ul>
      <li><a href="">Jhol</a></li>
    </ul>
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
#navbar {
  position: absolute;
  width: 100%;
  background-color: hsla(32, 82%, 56%, 1);
  height: 4em;
  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
@media only screen and (min-width: 600px) {
  /* For tablets: */
}

@media only screen and (min-width: 768px) {
  /* For desktop: */
}
</style>
