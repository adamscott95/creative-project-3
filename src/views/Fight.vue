<template>
  <div class="body">
  <div class="header">
    <h1>{{empty}}</h1>
  </div>
    <div class="initiate">
      <button class="auto" v-on:click="fight()">Fight!</button>
    </div>
    <div class="team">
      <Team1 :characters="characters_1" />
      <Team2 :characters="characters_2" />
    </div>
  </div>
</template>

<script>
import Team1 from "../components/Team1.vue"
import Team2 from "../components/Team2.vue"
export default {
  name: 'Fight',
  components: {
    Team1,
    Team2
  },
  methods: {
    fight() {
      if (this.$root.$data.team_1.length < this.$root.$data.team_2.length) {
        this.$root.$data.team_1 = []
      }
      else {
        this.$root.$data.team_2 = []
      }
    }
  },
  computed: {
    characters_1() {
      return this.$root.$data.team_1;
    },
    characters_2() {
      return this.$root.$data.team_2;
    },
    empty(){
      if (this.$root.$data.team_1.length == 0 & this.$root.$data.team_2.length == 0) {
        return "Add people to teams in order to start a fight!"
      }
      else {
        return ""
      }
    },
  }
}
</script>

<style scoped>
button {
  height: 50px;
  background: #000;
  color: white;
  border: none;
}

</style>