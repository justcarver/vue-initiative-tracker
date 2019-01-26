<template>
  <v-card class="player">
    <v-card-title primary-title>
      <div>
	<h3 class="headline mb-0">{{ player.name }}</h3>
	<div>{{ player.player }}</div>
	<div>{{ player.dexterity}}</div>
	<v-text-field type="number" v-model="player.initiative" />
      </div>
    </v-card-title>
  </v-card>
</template>

<script>
export default {
  name: 'Player',
  props: {
    player: Object,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
