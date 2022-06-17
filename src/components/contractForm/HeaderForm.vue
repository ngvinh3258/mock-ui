<template>
  <div class="header-container">
    <div class="header-box">
      <div class="logo"><img alt="" src="../../assets/logoForm.png" /></div>

      <div
        class="nav-link"
        v-for="(content, index) in list"
        :key="index"
        :class="[isActive === content ? activeClass : '']"
      >
        <a
          :class="[isActive === content ? activeClass : '']"
          href="#"
          @click="highlightHeader(content)"
          >{{ content }}</a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    list: Array,
  },
  data() {
    return {
      activeClass: "active",
      isActive: this.list[0],
    };
  },
  methods: {
    highlightHeader(e) {
      this.isActive = e;
    },
  },
};
</script>

<style scoped>
.header-container {
  height: 65px;
}
.header-box {
  display: flex;
  /* height: 50px; */
  height: 64px;
  width: 100%;
  box-shadow: 0px 0px 8px rgba(102, 102, 102, 0.24);
  left: 0px;
  align-items: center;
  position: absolute;
  top: 0px;
  background: #ffffff;
}
img {
  margin-left: 10px;
}

a {
  text-decoration: none;
  margin: 10px;
  color: #999999;

  font-family: Noto Sans;
  font-size: 16px;
  font-weight: 700;
  line-height: 24px;
  letter-spacing: 0px;
  text-align: center;
}
a.active {
  color: #333333;
}
.nav-link {
  height: 64px;
  display: flex;
  align-items: center;
}
.nav-link.active {
  border-bottom: 3px solid #007bc3;
}
</style>
