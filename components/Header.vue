<template>
  <b-navbar :fixed-top="true">
    <template slot="brand">
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        <img class="Header__logo" src="/img/logo.png" />
      </b-navbar-item>
    </template>
    <template slot="end">
      <b-navbar-item v-for="link in links" :key="link.url" :href="link.url">
        {{ link.label }}
      </b-navbar-item>
    </template>
  </b-navbar>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          label: 'Rules',
          url: '/rules'
        },
        {
          label: 'Teams',
          url: '/teams'
        },
        {
          label: 'Press Releases',
          url: '/press/'
        },
        {
          label: 'Schedule',
          url: '/schedule'
        },
        {
          label: 'Standings',
          url: '/standings'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.navbar-item {
  &:hover {
    color: #e2190a;
  }
  img {
    max-height: 70px;
  }
}
</style>
