<template>
  <div class="contract-container">
    <HeaderForm :list="headerList"></HeaderForm>
    <div class="contract-body">
      <div class="contract-heading">
        <div class="return-group">
          <img class="return-button" alt="" src="../assets/ArrowLeft.png" />
          <p class="return-content">雇用契約に戻る</p>
        </div>
        <div class="heading">{{ heading }}</div>
        <ProgressBarForm :currentStep="3"></ProgressBarForm>
        <div class="return-group">
          <img class="date-button" alt="" src="../assets/calendar 2.png" />
          <p class="date-content">2021/09/01までご登録ください</p>
        </div>
      </div>
      <slot name="body"></slot>
    </div>
    <div class="button-next-step"><slot name="button"></slot></div>
  </div>
</template>

<script>
import HeaderForm from "./contractForm/HeaderForm.vue";
import ProgressBarForm from "./contractForm/ProgressBarForm.vue";
export default {
  components: {
    HeaderForm,
    ProgressBarForm,
  },
  props: {
    headerList: Array,
    heading: String,
  },
};
</script>

<style scoped>
.contract-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.contract-body {
  width: 50%;
}
.heading {
  text-align: start;
  margin: 10px 0;
}
.return-group {
  display: flex;
  margin: 10px 0;
}
.return-button {
  height: 16px;
}
.return-content {
  font-size: 12px;
  margin: 0;
}
.date-content {
  font-size: 16px;
  margin: 0 5px;
}
</style>
