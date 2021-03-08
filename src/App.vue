<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
    
    </v-app-bar>

    <v-main>
      <InputItem input-label="Countdown" input-value=""/>
      <br>
      <InputItem input-label="Countdown" input-value="2"/>
    </v-main>
  </v-app>
</template>

<script>
import InputItem from './components/InputItem';

export default {
  name: 'App',

  components: {
    InputItem,
  },

  data: () => ({
    //
  }),
};
</script>
