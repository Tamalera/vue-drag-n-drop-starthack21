<template>
  <v-container>
    <!-- START DRAG AND DROP PLAYLIST -->
    <v-list>
      <v-subheader>Playlist</v-subheader>
      <v-list-item-group
        color="primary"
      >
        <draggable v-model="items" group="people" @start="drag=true" @end="drag=false">
          <v-list-item v-for="element in items" :key="element.id">{{element.title}} 
            <v-spacer></v-spacer>
            <v-chip class="mx-1" v-for="e in element.emotion" :key="e.id" :color="e.colour">{{e.name}}</v-chip>
          </v-list-item>
        </draggable>
        </v-list-item-group>
    </v-list>
    <!-- END DRAG AND DROP PLAYLIST -->

  </v-container>
</template>

<script>
  import draggable from 'vuedraggable'

  export default {
    components: {
      draggable,
    },

    name: 'HelloWorld',

    data: () => ({
      items: [
      {
        id: 0,
        title: 'Mercedes - Good Mood Storeroom Mix',
        emotion: [{name: 'calm', colour: 'pink lighten-3'}, {name: 'relaxing', colour: 'blue lighten-3'}]
      },
      {
        id: 1,
        title: 'Mercedes - Sunny Day',
        emotion: [{name: 'calm', colour: 'pink lighten-3'}, {name: 'cheerful', colour: 'purple lighten-3'}]
      },
      {
        id: 2,
        title: 'Mercedes - Pump it II',
        emotion: [{name: 'energetic', colour: 'lime lighten-3'}]
      },
      {
        id: 3,
        title: 'Mercedes - The Fast and the Furious',
        emotion: [{name: 'energetic', colour: 'lime lighten-3'}, {name: 'ecstatic', colour: 'lime accent-1'}, {name: 'heroic', colour: 'orange lighten-3'}]
      },
      {
        id: 4,
        title: 'Mercedes - A new Day, a New Challenge',
        emotion: [{name: 'proud', colour: 'teal lighten-3'}, {name: 'heroic', colour: 'orange lighten-3'}]
      }
      ]
    }),
  }
</script>

<style scoped>
.drop-zone {
  background-color: #eee;
  margin-bottom: 10px;
  padding: 10px;
}

.drag-el {
  background-color: #fff;
  margin-bottom: 10px;
  padding: 5px;
}
</style>
