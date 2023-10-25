<script setup>
import HomeTeam from '../components/HomeTeam.vue'
import AwayTeam from '../components/AwayTeam.vue'
import PositionColumn from '../components/PositionColumn.vue';

import { ref } from 'vue'
const teamOne = ref([
  {
    id: 1,
    name: 'J. Hurts',
    position: 'QB',
    thumbnail: "hurtsthumbnail.png",
    points: 0,
    team: 'Phi'
  },
  {
    id: 2,
    name: 'T. Hill',
    position: 'WR',
    thumbnail: "hillthumbnail.png ",
    points: 0,
    team: 'Mia'
  },
  {
    id: 3,
    name: 'M. Evans',
    position: 'WR',
    thumbnail: "evansthumbnail.png ",
    points: 0,
    team: 'TB'
  },
  {
    id: 4,
    name: 'C. McCaffrey',
    position: 'RB',
    thumbnail: "mccaffreythumbnail.png ",
    points: 0,
    team: 'SF'
  },
  {
    id: 5,
    name: 'A. Kamara',
    position: 'RB',
    thumbnail: "kamarathumbnail.png ",
    points: 0,
    team: 'NO'
  },
  {
    id: 6,
    name: 'M. Andrews',
    position: 'TE',
    thumbnail: "andrewsthumbnail.png ",
    points: 0,
    team: 'KC'
  },
  {
    id: 7,
    name: 'J. Tucker',
    position: 'K',
    thumbnail: "tuckerthumbnail.png ",
    points: 0,
    team: 'BAL'
  },
  {
    id: 8,
    name: 'Cleveland',
    position: 'DEF',
    thumbnail: "cleveland.png ",
    points: 0,
    team: 'CLE'
  }
])

const teamTwo = ref([
  {
    id: 9,
    name: 'P. Mahomes',
    position: 'QB',
    thumbnail: "mahomesthumbnail.png ",
    points: 0,
    team: 'KC'
  },
  {
    id: 10,
    name: 'J. Chase',
    position: 'WR',
    thumbnail: "chasethumbnail.png ",
    points: 0,
    team: 'CIN'
  },
  {
    id: 11,
    name: 'J. Jefferson',
    position: 'WR',
    thumbnail: "jeffersonthumbnail.png ",
    points: 0,
    team: 'MIN'
  },
  {
    id: 12,
    name: 'A. Ekeler',
    position: 'RB',
    thumbnail: "ekelerthumbnail.png ",
    points: 0,
    team: 'LAC'
  },
  {
    id: 13,
    name: 'D. Henry',
    position: 'RB',
    thumbnail: "henrythumbnail.png ",
    points: 0,
    team: 'TEN'
  },
  {
    id: 14,
    name: 'T. Kelce',
    position: 'TE',
    thumbnail: "kelcethumbnail.png ",
    points: 0,
    team: 'KC'
  },
  {
    id: 15,
    name: 'R. Patterson',
    position: 'K',
    thumbnail: "pattersonthumbnail.png ",
    points: 0,
    team: 'DET'
  },
  {
    id: 16,
    name: 'Dallas',
    position: 'DEF',
    thumbnail: "cowboys.png ",
    points: 0,
    team: 'DAL'
  }
])

const positions = ref([
  {
    id: 1,
  pos: 'QB'
},
{
  id: 2,
  pos: 'WR'
},
{
  id: 3,
  pos: 'WR'
},
{
  id: 4,
  pos: 'RB'
},
{
  id: 5,
  pos: 'RB'
},
{
  id: 6,
  pos: 'TE'
},
{
  id: 7,
  pos: 'K'
},
{
  id: 8,
  pos: 'DEF'
}
])

</script>

<template>
  <h1 class="week">Week 1 Matchup!</h1>
  <container class="container">
    <div class="home-team">
      <HomeTeam v-for="player in teamOne" :key="player.id" :player="player" />
    </div>
    <div class="position-label">
      <PositionColumn class="position-marker" v-for="position in positions" :key="position.id" :position="position"/>
    </div>
    <div class="away-team">
      <AwayTeam v-for="player in teamTwo" :key="player.id" :player="player" />
    </div>
  </container>
</template>

<style>
.week {
  text-align: center;
  padding: 30px;
  font-size: 45px;
}
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}
.home-team {
  width: 45%;
}
.away-team {
  width: 45%
}
.position-label {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  border: 20px white;
}
.home-team-column {
  padding: 20px;
  border: 0.5px solid gray;
}
h2 {
  border-top: 1px whitesmoke
}

</style>
