<script>
export default {
  name: "PlayBoard",
  props: {
    title: String,
    columnsCount: Number,
    rowsCount: Number,
  },
};
</script>

<template>
  <div class="playboard">
    <h2>{{ title }} {{ `${columnsCount}x${rowsCount}` }}</h2>
    <div class="grid-container">
      <div class="line" v-for="rowIndex in rowsCount" :key="rowIndex">
        <div
          class="cell"
          v-for="columnIndex in columnsCount"
          :key="rowIndex + '-' + columnIndex"
        >
          {{ `${rowIndex}x${columnIndex}` }}
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.playboard {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.line {
  margin: 0px;
  width: fit-content;
  display: flex;
  border-top: 1px solid black;
  border-bottom: 1px solid black;
  & + & {
    border-top: none;
  }
}
.cell {
  border-left: 1px solid black;
  border-right: 1px solid black;
  & + & {
    border-left: none;
  }
  height: 3vw;
  width: 3vw;
}
</style>
