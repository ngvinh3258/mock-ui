<template>
  <div class="box-content">
    <div class="box-header">
      <slot name="headerBox">
        <img class="confirm-img" src="../../assets/warning.png" alt="" />
        <p>ご確認ください</p></slot
      >
    </div>
    <div class="box-body">
      <slot name="bodyBox"
        >表示されている内容を確認いただき、認識に相違が無ければ同意するにチェックをしてください。</slot
      >
    </div>
    <div class="box-handle"><slot name="handleBox"></slot></div>
  </div>
</template>

<script>    
export default {
  props: {},
};
</script>

<style scoped>
.box-content {
  align-self: start;
  background-color: #f1f2f7;
}
.box-header {
  display: flex;
  height: 20px;
  justify-content: start;
}
p {
  height: 20px;
  color: #000;
  margin: -1px 4px;
  font-weight: bold;
}
</style>
