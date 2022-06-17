<template>
  <div class="progress-bar-container">
    <div class="step-box">
      <div v-for="step in 5" class="" :key="step">
        <div v-if="step % 2 !== 0">
          <img
            alt=""
            src="../../assets/viewPre.png"
            v-if="currentStep < step"
          />
          <img
            alt=""
            src="../../assets/viewActive.png"
            v-if="currentStep >= step"
          />
        </div>
        <div v-else>
          <img alt="" src="../../assets/penPre.png" v-if="currentStep < step" />
          <img
            alt=""
            src="../../assets/penActive.png"
            v-if="currentStep >= step"
          />
        </div>
      </div>
    </div>
    <div class="line-box">
      <div class="line-content" :style="{ width: widthLine + '%' }"></div>
    </div>
  </div>
</template>

<script>
export default {
  props: { currentStep: Number },
  data() {
    return {
      widthLine: 25 * (this.currentStep - 1),
    };
  },
};
</script>

<style scoped>
.progress-bar-container {
  position: relative;
}
.progress-bar-form {
  width: 100%;
}
.step-box {
  display: flex;
  justify-content: space-between;
}
.line-box {
  position: absolute;
  top: 20px;
  width: 100%;
  height: 5px;
  background-color: #dcdcdc;
  border-radius: 12px;
  overflow: hidden;
  z-index: -1;
}
.line-content {
  /* width: 100%; */
  height: 100%;
  background-color: #b2b1ff;
  border-radius: 12px;
  transition: width 0.5s ease;
}
</style>
