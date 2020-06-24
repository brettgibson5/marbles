<template>
  <div class="Page Standings">
    <div class="container">
      <MainTitle>Standings</MainTitle>
      <section>
        <b-table
          :data="standings"
          default-sort="total"
          sort-icon="arrow-up"
          sort-icon-size="is-small"
          default-sort-direction="desc"
          :show-detail-icon="true"
          detailed
          hoverable
          custom-detail-row
          detail-key="name"
        >
          <template slot-scope="props">
            <b-table-column field="name" label="Owner" sortable>
              {{ props.row.name }}
            </b-table-column>
            <b-table-column field="hero.label" label="Hero Marble" sortable>
              <span :class="`tag tag--${props.row.hero.value}`">
                {{ props.row.hero.label }}
              </span>
            </b-table-column>
            <b-table-column
              field="earnings"
              label="Total Winnings"
              sortable
              numeric
            >
              <span class="profit">${{ props.row.earnings }}</span>
            </b-table-column>
            <b-table-column
              field="total"
              label="Season Point Total"
              sortable
              numeric
            >
              {{ props.row.total }}
            </b-table-column>
          </template>

          <template slot="detail" slot-scope="props">
            <tr v-for="item in props.row.items" :key="item.label">
              <td v-if="showDetailIcon"></td>
              <td>&nbsp;&nbsp;&nbsp;&nbsp;{{ item.label }}</td>
              <td>{{ item.points }}</td>
            </tr>
          </template>
        </b-table>
      </section>
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
      standings: [
        {
          name: 'Lucas King',
          hero: {
            label: 'Thunderbolts',
            value: 'thunderbolts'
          },
          total: 21.5,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 21.5
            }
          ],
          earnings: 0
        },
        {
          name: 'Kevin Burke',
          hero: {
            label: 'Raspberry Racers',
            value: 'raspberry'
          },
          total: 61,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 61
            }
          ],
          earnings: 5
        },
        {
          name: 'Jon Leyh',
          hero: {
            label: 'Savage Speeders',
            value: 'savage'
          },
          total: 32,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 32
            }
          ],
          earnings: 0
        },
        {
          name: 'Ryan Ditty',
          hero: {
            label: 'Mellow Yellow',
            value: 'mellow'
          },
          total: 13,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 13
            }
          ],
          earnings: 0
        },
        {
          name: 'Stephen Murphy',
          hero: {
            label: 'Team Momo',
            value: 'momo'
          },
          total: 22,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 22
            }
          ],
          earnings: 0
        },
        {
          name: 'Joe Scheiner',
          hero: {
            label: 'Oceanics',
            value: 'oceanics'
          },
          total: 23,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 23
            }
          ],
          earnings: 0
        },
        {
          name: 'Jared Hyneman',
          hero: {
            label: 'Hazers',
            value: 'hazers'
          },
          total: 34.5,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 34.5
            }
          ],
          earnings: 0
        },
        {
          name: 'Steve Ormsbee',
          hero: {
            label: 'Midnight Wisps',
            value: 'wisps'
          },
          total: 58.5,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 58.5
            }
          ],
          earnings: 0
        },
        {
          name: 'Matthew Ogle',
          hero: {
            label: 'Team Momo',
            value: 'momo'
          },
          total: 32,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 32
            }
          ],
          earnings: 0
        },
        {
          name: "John O'Brien",
          hero: {
            label: 'Green Ducks',
            value: 'ducks'
          },
          total: 15.5,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 15.5
            }
          ],
          earnings: 0
        },
        {
          name: 'Andrew Craig',
          hero: {
            label: 'Minty Maniacs',
            value: 'maniacs'
          },
          total: 46.5,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 46.5
            }
          ],
          earnings: 0
        },
        {
          name: 'Katie Hodges',
          hero: {
            label: "Crazy Cat's Eyes",
            value: 'cat'
          },
          total: 35.5,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 35.5
            }
          ],
          earnings: 0
        },
        {
          name: 'Drew Murray',
          hero: {
            label: 'Balls of Chaos',
            value: 'chaos'
          },
          total: 41,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 41
            }
          ],
          earnings: 0
        },
        {
          name: 'John Englund',
          hero: {
            label: 'Team Momo',
            value: 'momo'
          },
          total: 36,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 36
            }
          ],
          earnings: 0
        },
        {
          name: 'Georges Mrad',
          hero: {
            label: 'Team Galactic',
            value: 'galactic'
          },
          total: 20.5,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 20.5
            }
          ],
          earnings: 0
        },
        {
          name: 'Ben Cox & Jess Ream',
          hero: {
            label: "Crazy Cat's Eyes",
            value: 'cat'
          },
          total: 26.5,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 26.5
            }
          ],
          earnings: 0
        },
        {
          name: 'Devin Emery',
          hero: {
            label: "O'rangers",
            value: 'orangers'
          },
          total: 28,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 28
            }
          ],
          earnings: 0
        },
        {
          name: 'Matt Galuppo',
          hero: {
            label: 'Hornets',
            value: 'hornets'
          },
          total: 29,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 29
            }
          ],
          earnings: 0
        },
        {
          name: 'Kelsey Payne',
          hero: {
            label: 'Bumblebees',
            value: 'bumblebees'
          },
          total: 27,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 27
            }
          ],
          earnings: 0
        },
        {
          name: 'Ian Henry',
          hero: {
            label: "O'rangers",
            value: 'orangers'
          },
          total: 30,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 30
            }
          ],
          earnings: 0
        },
        {
          name: 'Brian Nelson',
          hero: {
            label: 'Minty Maniacs',
            value: 'maniacs'
          },
          total: 42.5,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 42.5
            }
          ],
          earnings: 0
        },
        {
          name: 'Alex Ogle',
          hero: {
            label: 'Raspberry Racers',
            value: 'raspberry'
          },
          total: 50,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 50
            }
          ],
          earnings: 0
        },
        {
          name: 'Brett Gibson',
          hero: {
            label: 'Raspberry Racers',
            value: 'raspberry'
          },
          total: 23,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 23
            }
          ],
          earnings: 0
        },
        {
          name: 'Trevor Adams',
          hero: {
            label: 'Hornets',
            value: 'hornets'
          },
          total: 37,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 37
            }
          ],
          earnings: 0
        },
        {
          name: 'Asher Vollmer',
          hero: {
            label: 'Midnight Wisps',
            value: 'wisps'
          },
          total: 32,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 32
            }
          ],
          earnings: 0
        },
        {
          name: 'Jeff Myers',
          hero: {
            label: 'Hazers',
            value: 'hazers'
          },
          total: 17,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 17
            }
          ],
          earnings: 0
        },
        {
          name: 'Allen Reese',
          hero: {
            label: 'Thunderbolts',
            value: 'thunderbolts'
          },
          total: 36.5,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 36.5
            }
          ],
          earnings: 0
        },
        {
          name: 'Jean-Eric Khalife',
          hero: {
            label: "Crazy Cat's Eyes",
            value: 'cat'
          },
          total: 37.5,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 37.5
            }
          ],
          earnings: 0
        },
        {
          name: 'Kyle Wilhelm',
          hero: {
            label: 'Balls of Chaos',
            value: 'chaos'
          },
          total: 33,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 33
            }
          ],
          earnings: 0
        },
        {
          name: 'Chris DiBartolomeo',
          hero: {
            label: 'Hornets',
            value: 'hornets'
          },
          total: 19,
          weeks: [
            {
              label: 'Week 1: Balancing',
              points: 19
            }
          ],
          earnings: 0
        }
      ]
    }
  },
  methods: {
    getTotal(array) {
      return array.reduce((a, b) => a + b, 0)
    },
    toggle(row) {
      this.$refs.table.toggleDetails(row)
    },
    sortTotal(a, b, isAsc) {
      // console.log('b', b)
      // if (isAsc) return false
      // return true
      if (isAsc) {
        return this.getTotal(a.weekTotals) <= this.getTotal(b.weekTotals)
      } else {
        return this.getTotal(a.weekTotals) > this.getTotal(b.weekTotals)
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.Page.Standings {
  .profit {
    color: #4caf50;
  }
}
</style>
