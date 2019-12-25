<script>
import { Bar } from "vue-chartjs";
// import { Rough } from "roughjs";
import ChartRough from "chartjs-plugin-rough";

export default {
  extends: Bar,
  props: ["data", "options"],
  plugins: [ChartRough],
  // plugins: [Rough, ChartRough],
  mounted() {
    // this.addPlugin(Rough);
    this.addPlugin(ChartRough);
    this.renderChart(this.data, this.options);
  }
};
</script>
