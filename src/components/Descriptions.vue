<template>
    <div class="wrapper">
    <div class="characters">
        <div class="character" v-for="character in characters" :key="character.id">
            <div class="info">
                <h1>{{character.name}}</h1>
                <p>Species: {{character.species}}</p>
                <p>House: {{character.house}}</p>
                <p>Status: {{character.bloodStatus}}</p>
                <p>Role: {{character.role}}</p>
            </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {
  name: 'DescriptionList',
  props: {
    characters: Array
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
  width: 400px;
}

.info {
  background: #a2b9bc;
  color: #000;
  padding: 10px 30px;
  height: 265px;
}

.info h1 {
  font-size: 30px;
  font-family: Arial, Helvetica, sans-serif;
}

.info p {
  margin: 0px;
  font-size: 25px;
}
</style>