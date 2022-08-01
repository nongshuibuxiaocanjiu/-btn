<template>
  <div>
    <d-progress :percentage="100" :conFontColor="'white'" ></d-progress>
    <!-- <d-progress :percentage="33" color="orange"></d-progress>
    <d-progress :percentage="66" status="exception"></d-progress>
    <d-progress :percentage="100" status="success" ></d-progress> -->
  </div>
</template>

<script>
import dProgress from "./components/progressBar.vue";
export default {
  data() {
    return {};
  },
  components: {
    dProgress,
  },

  created() {},

  methods: {},
};
</script>

<style scoped lang="less">
.progress{
  width: 200px;
  height: 30px;

}
</style>
