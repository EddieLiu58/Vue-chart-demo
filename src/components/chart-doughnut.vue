<template>
  <div>
    <h2>甜甜圈</h2>

    <div class="card">
      <chartjs-doughnut
        :bind="true"
        :datasets="datasets"
        :labels="labels"
        :option="option"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      datasets: [
        {
          data: [20, 30, 50],
          backgroundColor: ["#b388ff", "#82b1ff", "#80d8ff"],
          hoverBackgroundColor: ["#673ab7", "#2196f3", "#03a9f4"]
        }
      ],
      labels: ["碳水化合物", "蔬菜", "蛋白質"],
      option: {}
    };
  }
};
</script>