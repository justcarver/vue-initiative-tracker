<template>
  <v-container>
    <v-layout>
      <v-flex xs12 sm6 md4 v-for="player in players">
	test
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'PlayerList',
  props: {
    players: Object,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
