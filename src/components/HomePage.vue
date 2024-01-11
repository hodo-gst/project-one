<template >
  <v-container fill-height fluid class="homepage-bg" :style="{ backgroundColor: '#edf2f4' }">
    <v-row align-content="center" justify="center" class="fill-height">
      <VButton name="Click me!" @button-click="handleClickEvent" :dark="false" />
    </v-row>
  </v-container>
</template>

<script>
import VButton from './VButton.vue';

export default {
  name: 'HomePage',
  components: {
    VButton
  },
  methods: {
    handleClickEvent() {
      alert('Button clicked!');
    }
  }
}
</script>