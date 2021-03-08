<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
    
    </v-app-bar>

    <v-main>
       <v-container>
    <v-row>
      <v-col>
        jeff
        </v-col>
        <v-col>
          <InputItem input-label="Countdown" input-value=""/>
        </v-col>
        <v-col>
          holst
        </v-col>
      </v-row>
      
       </v-container>

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
