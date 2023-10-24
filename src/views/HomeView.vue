<script setup>
import HomeTeam from '../components/HomeTeam.vue'
import AwayTeam from '../components/AwayTeam.vue'

import { ref } from 'vue'
const teamOne = ref([
  {
    id: 1,
    name: 'J. Hurts',
    position: 'QB',
    thumbnail: 'image',
    points: 0,
    team: 'Phi'
  },
  {
    id: 2,
    name: 'T. Hill',
    position: 'WR',
    thumbnail: 'image',
    points: 0,
    team: 'Mia'
  },
  {
    id: 3,
    name: 'M. Evans',
    position: 'WR',
    thumbnail: 'image',
    points: 0,
    team: 'TB'
  },
  {
    id: 4,
    name: 'C. McCaffrey',
    position: 'RB',
    thumbnail: 'image',
    points: 0,
    team: 'SF'
  },
  {
    id: 5,
    name: 'A. Kamara',
    position: 'RB',
    thumbnail: 'image',
    points: 0,
    team: 'NO'
  },
  {
    id: 6,
    name: 'M. Andrews',
    position: 'TE',
    thumbnail: 'image',
    points: 0,
    team: 'KC'
  },
  {
    id: 7,
    name: 'J. Tuckers',
    position: 'K',
    thumbnail: 'image',
    points: 0,
    team: 'BAL'
  },
  {
    id: 8,
    name: 'Cleveland',
    position: 'DEF',
    thumbnail: 'image',
    points: 0,
    team: 'CLE'
  }
])

const teamTwo = ref([
  {
    id: 9,
    name: 'P. Mahomes',
    position: 'QB',
    thumbnail: 'image',
    points: 0,
    team: 'KC'
  },
  {
    id: 10,
    name: 'J. Chase',
    position: 'WR',
    thumbnail: 'image',
    points: 0,
    team: 'CIN'
  },
  {
    id: 11,
    name: 'C. Ridley',
    position: 'WR',
    thumbnail: 'image',
    points: 0,
    team: 'JAX'
  },
  {
    id: 12,
    name: 'A. Ekeler',
    position: 'RB',
    thumbnail: 'image',
    points: 0,
    team: 'LAC'
  },
  {
    id: 13,
    name: 'D. Henry',
    position: 'RB',
    thumbnail: 'image',
    points: 0,
    team: 'TEN'
  },
  {
    id: 14,
    name: 'T. Kelce',
    position: 'TE',
    thumbnail: 'image',
    points: 0,
    team: 'KC'
  },
  {
    id: 15,
    name: 'R. Patterson',
    position: 'K',
    thumbnail: 'image',
    points: 0,
    team: 'DET'
  },
  {
    id: 16,
    name: 'Dallas',
    position: 'DEF',
    thumbnail: 'image',
    points: 0,
    team: 'DAL'
  }
])
</script>

<template>
  <h1 class="week">Week 1 Matchup!</h1>
  <container class="container">
    <div class="home-team">
      <HomeTeam v-for="team in teamOne" :key="team.id" :team="team" />
    </div>
    
    <div class="away-team">
      <AwayTeam v-for="team in teamTwo" :key="team.id" :team="team" />
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
