<template>
  <div>
    <h2>柱狀圖</h2>

    <div  class="card">
      <canvas id="fooCanvas" count="2" />

      <chartjs-bar
        v-for="(item, i) in types"
        :key="i"
        :backgroundcolor="item.bgColor"
        :beginzero="beginZero"
        :bind="true"
        :bordercolor="item.borderColor"
        :data="item.data"
        :datalabel="item.dataLabel"
        :labels="labels"
        target="fooCanvas"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      beginZero: true,
      labels: ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"],
      types: [
        {
          bgColor: "#FFD78C",
          borderColor: "#e91e63",
          data: [2, 4, 7, 9, 6, 5, 6],
          dataLabel: "收入"
        },
        {
          bgColor: "#00EBEB",
          borderColor: "#9c27b0",
          data: [1, 5, 2, 6, 3, 8, 5],
          dataLabel: "支出"
        }
      ]
    };
  }
};
</script>

