<template>
  <v-container>
    <v-row class="text-center">
    <draggable v-model="items" group="people" @start="drag=true" @end="drag=false">
      <div v-for="element in items" :key="element.id">{{element.title}}</div>
    </draggable>
    </v-row>
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
        title: 'Song X',
        list: 1
      },
      {
        id: 1,
        title: 'Song Y',
        list: 1
      },
      {
        id: 2,
        title: 'Song Z',
        list: 2
      }]
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
