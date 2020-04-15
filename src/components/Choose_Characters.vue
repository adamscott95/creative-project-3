<template>
    <div class="wrapper">
    <div class="characters">
        <div class="character" v-for="character in characters" :key="character.id">
            <div class="info">
                <h1>{{character.name}}</h1>
                <p>{{character.species}}</p>
            </div>
            <div class="teams">
                <button class="auto" v-on:click="addToTeam1(character)">Add to Team 1</button>
                <button class="auto" v-on:click="addToTeam2(character)">Add to Team 2</button>
            </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {
  name: 'CharacterList',
  props: {
    characters: Array
  },
  methods: {
    addToTeam1(character) {
      if (!this.$root.$data.team_1.includes(character) & !this.$root.$data.team_2.includes(character)) {
        this.$root.$data.team_1.push(character);
      }
    },
    addToTeam2(character) {
      if (!this.$root.$data.team_1.includes(character) & !this.$root.$data.team_2.includes(character)) {
        this.$root.$data.team_2.push(character);
      }
    }
  },
}
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.characters {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.character {
  margin: 10px;
  margin-top: 50px;
  width: 200px;
}

.info {
  background: yellow;
  color: #000;
  padding: 10px 30px;
  height: 120px;
}

.info h1 {
  font-size: 20px;
}

.info p {
  margin: 0px;
  font-size: 15px;
}


.teams {
  display: flex;
}

button {
  height: 50px;
  background: #000;
  color: white;
  border: none;
}

.auto {
  margin-left: auto;
}
</style>