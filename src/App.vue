<template>
  <v-app>
    <v-app-bar
      app
      color="black"
      dark
    >
    MUSAE - Mercedes Benz Music Experience
    <v-spacer></v-spacer>
        <v-avatar color="grey darken-3">
      <v-icon dark>
        mdi-account-circle
      </v-icon>
    </v-avatar>
    </v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
