<template>
  <div>
    <div class="Progress">
      <div class="small" :style="`width:${30}%`">30%</div>
      <slot></slot>
    </div>
    <div class="Progress">
      <div class="small" :style="`width:${70}%`">
        <!--  -->
        70%
      </div>
      <slot></slot>
    </div>
    <div class="Progress">
      <div class="small" :style="`width:${percentage}%`">
        <!--  `background-color: (${percentage} == 100 ? : ${conFontColor} :'red') `, -->
        100%
      </div>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: ["percentage", "conFontColor"],

  created() {
    console.log(this.conFontColor);
    console.log(typeof this.conFontColor);
  },

  methods: {},
};
</script>

<style scoped lang="less">
.Progress {
  width: 200px;
  height: 30px;
  line-height: 30px;
  background-color: pink;
  border-radius: 5px;
}
.small {
  width: 10%;
  height: 100%;
  // line-height: 100%;
  border-radius: 5px;
  background-color: red;
  font-size: 14px;
  text-align: center;
}
</style>
