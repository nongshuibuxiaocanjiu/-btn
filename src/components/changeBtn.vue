<template>
  <div>
    <button
      class="g-button"
      :class="[
        `g-btn-${type}`,
        {
          'is-round': round,
          'is-disabled': disabled,
        },
      ]"
      @click="btnclick"
      :disabled="disabled"
    >
      {{ btnName }}
    </button>
  </div>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: "default",
    },
    btnName: {
      type: String,
      default: "默认按钮",
    },
    round: {
      type: Boolean,
      default: false,
    },
    disabled: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    btnclick(e) {
      this.$emit("click", e);
    },
  },
};
</script>

<style scoped lang="less">
.g-btn-primary {
  background-color: pink;
  width: 100px;
  height: 40px;
  border: 1px solid #fff;
  &:hover {
    background: pink;
    background-color: pink;
    color: #fff;
  }
}
.g-btn-success {
  background-color: #71c216;
  width: 100px;
  height: 40px;
  border: 1px solid #ccc;
  &:hover {
    background: #85ce61;
    background-color: #85ce61;
    color: #fff;
  }
}
.is-round {
  border-radius: 15px;
  padding: 2px 3px;
}
// 意思是只要类名中包括g-icon就调用该样式
[class*="g-icon"] {
  font-family: "iconfont" !important;
  font-size: 16px;
  font-style: normal;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
// disabled样式
.g-btn.is-disabled {
  cursor: no-drop;
}
</style>
