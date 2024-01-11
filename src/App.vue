<template>
  <v-app>
    <v-main>
      <HomePage/>
    </v-main>
  </v-app>
</template>

<script>
import HomePage from './components/HomePage';

export default {
  name: 'ProjectOne',

  components: {
    HomePage,
  },

  data: () => ({
    //
  }),
};
</script>
