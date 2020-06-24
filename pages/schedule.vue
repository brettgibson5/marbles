<template>
  <div class="Page Schedule">
    <div class="container">
      <MainTitle>Schedule</MainTitle>
      <ul>
        <li v-for="item in dates" :key="item.week">
          <strong>Week {{ item.week }}:</strong> {{ item.event }}
          <span class="fa fa-calendar-alt"></span> {{ item.date }}
        </li>
      </ul>
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
      dates: [
        {
          week: 1,
          event: 'Balancing',
          date: 'June 21, 2020'
        },
        {
          week: 2,
          event: 'Halfpipe',
          date: 'June 28, 2020'
        },
        {
          week: 3,
          event: "Newton's Cradle",
          date: 'July 3, 2020'
        },
        {
          week: 4,
          event: 'Funnel Endurance',
          date: 'July 10, 2020'
        },
        {
          week: 5,
          event: 'Long Jump',
          date: 'July 12, 2020'
        },
        {
          week: 6,
          event: 'TBD',
          date: 'TBD'
        },
        {
          week: 7,
          event: 'TBD',
          date: 'TBD'
        },
        {
          week: 8,
          event: 'TBD',
          date: 'TBD'
        },
        {
          week: 9,
          event: 'TBD',
          date: 'TBD'
        },
        {
          week: 10,
          event: 'TBD',
          date: 'TBD'
        },
        {
          week: 11,
          event: 'TBD',
          date: 'TBD'
        },
        {
          week: 12,
          event: 'TBD',
          date: 'TBD'
        },
        {
          week: 13,
          event: 'TBD',
          date: 'TBD'
        },
        {
          week: 14,
          event: 'TBD',
          date: 'TBD'
        },
        {
          week: 15,
          event: 'TBD',
          date: 'TBD'
        },
        {
          week: 16,
          event: 'TBD',
          date: 'TBD'
        }
      ]
    }
  }
}
</script>
