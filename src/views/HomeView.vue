<script setup>
import HomeTeam from '../components/HomeTeam.vue'
import AwayTeam from '../components/AwayTeam.vue'

import { ref } from 'vue'
const teamOne = ref([
  {
    id: 1,
    name: 'J. Hurts',
    position: 'QB',
    thumbnail: " ../src/assets/images/hurtsthumbnail.png ",
    points: 0,
    team: 'Phi'
  },
  {
    id: 2,
    name: 'T. Hill',
    position: 'WR',
    thumbnail: " ../src/assets/images/hillthumbnail.png ",
    points: 0,
    team: 'Mia'
  },
  {
    id: 3,
    name: 'M. Evans',
    position: 'WR',
    thumbnail: " ../src/assets/images/evansthumbnail.png ",
    points: 0,
    team: 'TB'
  },
  {
    id: 4,
    name: 'C. McCaffrey',
    position: 'RB',
    thumbnail: " ../src/assets/images/mccaffreythumbnail.png ",
    points: 0,
    team: 'SF'
  },
  {
    id: 5,
    name: 'A. Kamara',
    position: 'RB',
    thumbnail: " ../src/assets/images/kamarathumbnail.png ",
    points: 0,
    team: 'NO'
  },
  {
    id: 6,
    name: 'M. Andrews',
    position: 'TE',
    thumbnail: " ../src/assets/images/andrewsthumbnail.png ",
    points: 0,
    team: 'KC'
  },
  {
    id: 7,
    name: 'J. Tucker',
    position: 'K',
    thumbnail: " ../src/assets/images/tuckerthumbnail.png ",
    points: 0,
    team: 'BAL'
  },
  {
    id: 8,
    name: 'Cleveland',
    position: 'DEF',
    thumbnail: " ../src/assets/images/cleveland.png ",
    points: 0,
    team: 'CLE'
  }
])

const teamTwo = ref([
  {
    id: 9,
    name: 'P. Mahomes',
    position: 'QB',
    thumbnail: " ../src/assets/images/mahomesthumbnail.png ",
    points: 0,
    team: 'KC'
  },
  {
    id: 10,
    name: 'J. Chase',
    position: 'WR',
    thumbnail: " ../src/assets/images/chasethumbnail.png ",
    points: 0,
    team: 'CIN'
  },
  {
    id: 11,
    name: 'J. Jefferson',
    position: 'WR',
    thumbnail: " ../src/assets/images/jeffersonthumbnail.png ",
    points: 0,
    team: 'MIN'
  },
  {
    id: 12,
    name: 'A. Ekeler',
    position: 'RB',
    thumbnail: " ../src/assets/images/ekelerthumbnail.png ",
    points: 0,
    team: 'LAC'
  },
  {
    id: 13,
    name: 'D. Henry',
    position: 'RB',
    thumbnail: " ../src/assets/images/henrythumbnail.png ",
    points: 0,
    team: 'TEN'
  },
  {
    id: 14,
    name: 'T. Kelce',
    position: 'TE',
    thumbnail: " ../src/assets/images/kelcethumbnail.png ",
    points: 0,
    team: 'KC'
  },
  {
    id: 15,
    name: 'R. Patterson',
    position: 'K',
    thumbnail: " ../src/assets/images/pattersonthumbnail.png ",
    points: 0,
    team: 'DET'
  },
  {
    id: 16,
    name: 'Dallas',
    position: 'DEF',
    thumbnail: " ../src/assets/images/cowboys.png ",
    points: 0,
    team: 'DAL'
  }
])
</script>

<template>
  <h1 class="week">Week 1 Matchup!</h1>
  <container class="container">
    <div class="home-team">
      <HomeTeam v-for="player in teamOne" :key="player.id" :player="player" />
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
  border: 1px solid black;
}
.home-team {
  
  
}
.away-team {
  
}
</style>
