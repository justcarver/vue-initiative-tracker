<template>
  <v-container>
    <v-layout row wrap>
      <v-flex xs4 v-for="player in players">
	<v-card>
	  <v-card-title primary-title>
	    <div>
	      <h3 class="headline mb-0">{{ player.name }}</h3>
	      <div>{{ player.player }}</div>
	      <div>{{ player.dexterity}}</div>
	      <v-text-field type="number" v-model="player.initiative" />
	    </div>
	  </v-card-title>
	</v-card>
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
