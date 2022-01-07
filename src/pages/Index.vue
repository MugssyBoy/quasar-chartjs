<template>
  <q-page class="flex flex-center">
    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-vertical.svg"
      style="width: 200px; height: 200px"
    >
    <q-chart
      identifier="myChart"
      style="height:30vh; width: 100%"
      :type="line"
      :labels="labels"
      :datasets="datasets"
      :options="options"
    />
  </q-page>
</template>

<script>
import QChart from 'components/Chart.vue'

export default {
  name: "PageIndex",
  components: {
    QChart
  },
  data() {
    return {
      line: "line",
      labels: [0, 10, 5, 2, 20, 30, 45],
      datasets: [
        {
          label: "My First dataset",
          backgroundColor: 'rgb(255, 99, 132)',
          borderColor: 'rgb(255, 99, 132)',
          data: [0, 10, 5, 2, 20, 30, 45]
        }
      ],
      options: {}
    }
  }
}
// import { defineComponent } from 'vue'

// export default defineComponent({
//   name: 'PageIndex'
// })
</script>
