<script>
import { Line } from "vue-chartjs";

export default {
  extends: Line,
  data() {
    return {
      gradient: null,
      gradient2: null
    };
  },
  mounted() {
    this.gradient = this.$refs.canvas
      .getContext("2d")
      .createLinearGradient(0, 0, 0, 450);
    this.gradient2 = this.$refs.canvas
      .getContext("2d")
      .createLinearGradient(0, 0, 0, 450);

    // this.gradient.addColorStop(0, "rgba(51, 108, 251, 0.2)");
    // this.gradient.addColorStop(0.5, "rgba(51, 108, 251, 0.2)");
    // this.gradient.addColorStop(1, "rgba(51, 108, 251, 0.02)");

    this.gradient2.addColorStop(0, "rgba(51, 108, 251, 0.2");
    this.gradient2.addColorStop(1, "rgba(51, 108, 251, 0.02)");

    this.renderChart(
      {
        labels: [
          "2020-1",
          "2020-2",
          "2020-3",
          "2020-4",
          "2020-5",
          "2020-6",
          "2020-7",
          "2020-8",
          "2020-9",
          "2020-10",
          "2020-11",
          "2020-12",
        ],
        datasets: [
          {
            label: "Patients 2019",
            borderColor: "#FAC032",
            pointBackgroundColor: "white",
            borderWidth: 2,
            pointBorderColor: "white",
            backgroundColor: this.gradient,
            data: [40, 39, 10, 40, 39, 80, 40, 10, 40, 39, 21, 66]
          },
          {
            label: "Patients 2020",
            borderColor: "#336CFB",
            pointBackgroundColor: "white",
            pointBorderColor: "white",
            borderWidth: 2,
            backgroundColor: this.gradient2,
            data: [60, 55, 32, 10, 2, 12, 53, 70, 40, 39, 52, 34]
          }
        ]
      },
      { responsive: true, maintainAspectRatio: false }
    );
  }
};
</script>