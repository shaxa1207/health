<template>
  <div class="chard-wrapper">
      <div class="chard-header">
          <h3 class="title">Hospital Survey</h3>
      </div>
    <health-chart />
  </div>
</template>
<script>
import healthChart from "./healthChart.vue";

export default {
  name: "chardWrapper",
  components: {
    healthChart,
  },
};
</script>
<style lang="scss" scoped>
.chard-wrapper{
    padding: 24px;
    margin: 38px 0;
    background: #FFFFFF;
    box-shadow: 0px 12px 26px rgba(16, 30, 115, 0.06);
    border-radius: 8px;
    .title{
        font-family: Lato, sans-serif;
        font-weight: bold;
        font-size: 20px;
        line-height: 26px;
        letter-spacing: 0.2px;
        color: #25282B;
    }
}
</style>
