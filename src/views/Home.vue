<template>
  <div>
    <CharacterList :characters="characters" />
  </div>
</template>

<script>
import CharacterList from "../components/Choose_Characters.vue"
export default {
  name: 'Home',
  components: {
    CharacterList,
  },
  data() {
    return {

    }
  },
  computed: {
    characters() {
      return this.$root.$data.characters;
    },
  },
}
</script>
