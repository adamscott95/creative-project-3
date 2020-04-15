<template>
  <div>
    <DescriptionList :characters="characters" />
  </div>
</template>

<script>
import DescriptionList from "../components/Descriptions.vue"
export default {
  name: 'About',
  components: {
    DescriptionList,
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
