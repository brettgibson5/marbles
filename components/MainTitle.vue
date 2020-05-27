<template>
  <h1 class="MainTitle"><slot /></h1>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.MainTitle {
  font-size: 70px;
  font-weight: 800;
  margin-bottom: 1rem;
}
</style>
