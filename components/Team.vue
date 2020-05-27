<template>
  <div class="Team">
    <div class="Team__player">
      <div
        class="Team__player-image"
        :style="{ 'background-image': player.imgUrl }"
      ></div>
      <h3 class="Team__player-name">{{ player.name }}</h3>
    </div>
    <div class="Team__marble">
      <div
        class="Team__marble-image"
        :style="{ 'background-image': marble.imgUrl }"
      ></div>
      <h3 class="Team__marble-name">{{ marble.name }}</h3>
    </div>
    <p>{{ description }}</p>
  </div>
</template>

<script>
export default {
  props: {
    player: {
      type: Object,
      default: () => {}
    },
    marble: {
      type: Object,
      default: () => {}
    },
    description: {
      type: String,
      default: ''
    }
  }
}
</script>
