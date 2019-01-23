<template>
  <div>
    <h2>折線圖</h2>

    <div class="card">
      <header>
        <chartjs-line
          :backgroundcolor="bgColor"
          :beginzero="beginZero"
          :bind="true"
          :bordercolor="borderColor"
          :data="data[radio]"
          :datalabel="dataLabel"
          :labels="labels[radio]"
        />
      </header>

      <footer class="flex two">
        <label>
          <input v-model="radio" :name="dataLabel" type="radio" value="day">
          <span class="checkable">今天</span>
        </label>
        <label>
          <input v-model="radio" :name="dataLabel" type="radio" value="week">
          <span class="checkable">本週</span>
        </label>
      </footer>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      beginZero: true,
      bgColor: "#ff8a80",
      borderColor: "#f44336",
      data: {
        day: [1, 3, 5, 3, 1],
        week: [12, 14, 16, 18, 11, 13, 15]
      },
      dataLabel: "Foo",
      labels: {
        day: [8, 10, 12, 14, 16],
        week: ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"]
      },
      radio: "day"
    };
  }
};
</script>