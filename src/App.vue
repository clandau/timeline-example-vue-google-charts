<template>
  <div id="app">
    <GChart
      type="Timeline"
      :settings="{ packages: ['timeline'] }"
      :data="timelineData"
      :options="timelineOptions"
    />
  </div>
</template>

<script>
import { GChart } from "vue-google-charts";
export default {
  name: "App",
  components: {
    GChart
  },

  data() {
    return {
      timelineData: [
        ["name", "start", "end"],
        ["Washington", new Date(1789, 3, 30), new Date(1797, 2, 4)],
        ["Adams", new Date(1797, 2, 4), new Date(1801, 2, 4)],
        ["Jefferson", new Date(1801, 2, 4), new Date(1809, 2, 4)]
      ],
      timelineOptions: {
        timeline: {
          rowLabelStyle: { fontName: "Ariel" }
        },
        colors: ["#E74C3C", "#2C3E50", "#2980B9"],
        tooltip: { textStyle: { fontName: "Ariel", fontSize: 14 } }
      }
    };
  }
};
</script>

