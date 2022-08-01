<template>
  <div>
    <!-- type: primary:粉色，success:绿色-->
    <!-- round 圆型 -->
    <!-- disabled 禁用-->
    <gButton type="primary" btnName="成功按钮" round @click="getType" 
></gButton>
<gButton type="primary" btnName="禁用" round @click="getType"  disabled
></gButton>
  </div>
</template>

<script>
import gButton from './components/changeBtn.vue'
export default {
  data() {
    return {};
  },
  components:{
    gButton
  },

  created() {},

  methods: {
    getType() {
      console.log(11);
    }
  },
};
</script>

<style scoped lang="less"></style>
