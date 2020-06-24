<template>
  <div class="Page Rules">
    <div class="container">
      <MainTitle>Lou's Rules</MainTitle>
      <div class="columns">
        <div class="column">
          <section>
            <b-collapse
              v-for="(collapse, index) of collapses"
              :key="index"
              class="card"
              animation="slide"
              :open="isOpen == index"
              @open="isOpen = index"
            >
              <div
                slot="trigger"
                slot-scope="props"
                class="card-header"
                role="button"
              >
                <p class="card-header-title">
                  {{ collapse.title }}
                </p>
                <a class="card-header-icon">
                  <b-icon :icon="props.open ? 'menu-down' : 'menu-up'">
                  </b-icon>
                </a>
              </div>
              <div class="card-content">
                <div class="content" v-html="collapse.text"></div>
              </div>
            </b-collapse>
          </section>
        </div>
        <div class="column"></div>
      </div>
    </div>
  </div>
</template>

<script>
import MainTitle from '~/components/MainTitle'

export default {
  components: {
    MainTitle
  },
  data() {
    return {
      isOpen: 0,
      collapses: [
        {
          title: 'Pay Structure',
          text: `<strong>Weekly winner:</strong> $5<br /><br /><strong>Season Winners:</strong><br />1st Place	45% ($301.50)<br />
2nd Place	25% ($167.50)<br />
3rd Place	15% ($100.50)<br />
4th Place	10% ($67.00)<br />
5th Place	5% ($33.50)`
        },
        {
          title: 'Title 2',
          text: 'Text 2'
        },
        {
          title: 'Title 3',
          text: 'Text 3'
        }
      ]
    }
  }
}
</script>
