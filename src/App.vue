<template>
  <div id="app">
    <ContractForm :headerList="header" :heading="heading"
      ><template slot="body">
        <ContractView></ContractView>
      </template>
    </ContractForm>
  </div>
</template>

<script>
import ContractForm from "./components/ContractForm.vue";
import ContractView from "./components/contractForm/ContractView.vue";

export default {
  name: "App",
  components: {
    ContractForm,
    ContractView,
  },
  data() {
    return {
      header: ["入社手続き", "ヘルプ"],
      heading: "入社手続きの登録をお願いいたします",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
