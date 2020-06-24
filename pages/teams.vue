<template>
  <div class="Page Teams">
    <div class="container">
      <div class="columns">
        <div v-for="team in teams" :key="team.player.name" class="column">
          <Team v-bind="team" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Team from '~/components/Team'
export default {
  components: {
    Team
  },
  data() {
    return {
      teams: [
        {
          player: {
            name: 'Alex Ogle',
            imgUrl: '/img/alex.JPG'
          },
          marble: {
            name: 'Hornets',
            imgUrl: '/img/hornets.png'
          },
          description:
            'Burr, it’s cold on top of the mountain is what Andy hopes to scream as an avalanche cascades on his competitors.'
        },
        {
          player: {
            name: 'Alex Ogle',
            imgUrl: '/img/alex.JPG'
          },
          marble: {
            name: 'Hornets',
            imgUrl: '/img/hornets.png'
          },
          description:
            'Burr, it’s cold on top of the mountain is what Andy hopes to scream as an avalanche cascades on his competitors.'
        }
      ]
    }
  }
}
</script>
