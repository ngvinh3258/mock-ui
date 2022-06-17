<template>
  <div class="contract-container">
    <BoxContent></BoxContent>
  </div>
</template>

<script>
import BoxContent from './BoxContent.vue';
export default {
    props: {},
    components: { BoxContent }
};
</script>

<style scoped>
.box-content {
  align-self: start;
  background-color: #f1f2f7;
  
}
.confirm-header {
  display: flex;
  height: 20px;
  justify-content: start;
}
.confirm-img {
}
p {
  height: 20px;
  color: #000;
  margin: -1px 4px;
  font-weight: bold;
}
</style>
