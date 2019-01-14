<template>
  <v-form v-model="newPlayer">
    <v-container>
      <v-layout>
        <v-flex xs12>
          <h3>Add Player</h3>
        </v-flex>
      </v-layout>
      <v-layout>
        <v-flex xs12>
          <v-text-field v-model="characterName" label="Character Name" required>
          </v-text-field>
        </v-flex>
        <v-flex xs12>
          <v-text-field v-model="playerName" label="Player Name" required>
          </v-text-field>
        </v-flex>
        <v-flex xs12>
          <v-text-field v-model="dexterity" label="Dexterity" required>
          </v-text-field>
        </v-flex>
      </v-layout>
      <v-layout>
	<v-flex xs12>
          <v-btn>Add Player</v-btn>
          <v-btn>Cancel</v-btn>
	</v-flex>
      </v-layout>
    </v-container>
  </v-form>
</template>

<script>
export default {
  name: 'AddPlayerForm',
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
