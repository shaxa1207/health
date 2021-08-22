<template>
  <div class="about">
    <search-bar :card="cardItem" />
  </div>
</template>
<script>
import searchBar from '../components/searchBar.vue';

export default {
  components: { searchBar },
  name: "About",
  data(){
    return{
      cardItem: [
        {
          img: require("../assets/images/svg4.svg"),
          title: "Appointments",
          titleNumber: "213"
        },
        {
          img: require("../assets/images/svg3.svg"),
          title: "New Patients",
          titleNumber: "104"
        },
        {
          img: require("../assets/images/svg2.svg"),
          title: "Operations",
          titleNumber: "24"
        },
        {
          img: require("../assets/images/svg1.svg"),
          title: "Hospital Earnings",
          titleNumber: "$ 12,174"
        },
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
.area-card {
  margin: 30px 0;
  cursor: pointer;
  .card-item {
    padding: 24px;
    background: #ffffff;
    box-shadow: 0px 12px 26px rgba(16, 30, 115, 0.06);
    border-radius: 8px;
    img{
      margin-right: 24px;
    }
    .title {
      font-family: Lato;
      font-weight: bold;
      font-size: 14px;
      line-height: 20px;
      letter-spacing: 0.1px;
      color: #25282b;
      margin-bottom: 4px;
    }
    .title-number {
      font-family: Lato;
      font-size: 18px;
      line-height: 24px;
      letter-spacing: 0.1px;
      color: #336cfb;
      margin: 0;
    }
  }
}
</style>