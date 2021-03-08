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
        <InputItem input-label="Timer" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Rounds" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Work" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Rest" input-value=""/>
        </v-col>
      </v-row>
      <v-row>
      <v-col>
        <InputItem input-label="Timer" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Rounds" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Work" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Rest" input-value=""/>
        </v-col>
      </v-row>
      <v-row>
      <v-col>
        <InputItem input-label="Timer" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Rounds" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Work" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Rest" input-value=""/>
        </v-col>
      </v-row>
      <v-row>
      <v-col>
        <InputItem input-label="Timer" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Rounds" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Work" input-value=""/>
        </v-col>
        <v-col>
          <InputItem input-label="Rest" input-value=""/>
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
