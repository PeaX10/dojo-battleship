<script>
import PlayBoard from "./PlayBoard.vue";
export default {
  name: "BattleBoard",
  components: {
    PlayBoard,
  },
};
</script>

<template>
  <div class="battle-board">
    <p class="title">Battleship Game</p>
    <PlayBoard title="Player" :columns-count="10" :rows-count="10" />
  </div>
</template>

<style lang="scss" scoped>
.title {
  font-size: 30px;
  font-weight: bold;
  margin-bottom: 30px;
}
.battle-board {
  padding: 30px;
}
</style>
