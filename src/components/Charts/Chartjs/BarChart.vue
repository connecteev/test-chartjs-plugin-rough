<script>
import { Bar } from "vue-chartjs";
// import ChartRough from "chartjs-plugin-rough";

export default {
  extends: Bar,
  props: ["data", "options"],
  // plugins: [ChartRough],
  mounted() {
    // this.addPlugin(ChartRough);
    this.renderChart(this.data, this.options);
  }
};
</script>
