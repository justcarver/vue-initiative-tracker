<template>
  <v-app dark>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Initiative Tracker</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>

    <v-content>
      <PlayerList v-bind:players="players" v-if="combat == false" />
    </v-content>
  </v-app>
</template>

<script>
import AddPlayerForm from './components/AddPlayerForm.vue'
import PlayerList from './components/PlayerList.vue'

let savedPlayers = []
if (window.localStorage.players) {
  savedPlayers = JSON.parse(window.localStorage.players);
}

export default {
  name: 'App',
  components: {
    AddPlayerForm,
    PlayerList
  },
  data () {
    return {
      addingPlayers: false,
      combat: false,
      currentOrder: [],
      editing: [],
      monsters: [],
      newMonster: {
	name: "Monster 1",
	initiative: 0,
	dexterity: 0,
	status: false
      },
      newPlayers: {
	name: "",
	players: "",
	dexterity: 0,
	initiative: 0,
	status: false
      },
      players: savedPlayers,
      round: 0,
      turn: 0
    }
  }
}
</script>
