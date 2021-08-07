<template>
  <div class="home d-flex">
    <ch-aside />
    <div class="main-part">
      <search-bar :card="cardItem"/>
      <ch-table />
    </div>
  </div>
</template>

<script>
import ChAside from "../components/ch-aside.vue";
import SearchBar from "../components/searchBar.vue";
import ChTable from "../components/ch-table.vue";


export default {
  name: "Home",
  components: {
    ChAside,
    SearchBar,
    ChTable,
  },
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
};

</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap");
.home {
  background: #f6f8fb;
  .main-part {
    width: 100%;
    padding: 24px 36px;
  }
}
</style>
