<template>
  <div style="width: 100px;">
    <v-text-field
            v-bind:value="value"
            v-bind:label="label"
            v-bind="attrs"
            v-on="on"
            readonly
          ></v-text-field>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    props: [
      'label', 'value', 'attrs', 'on'
    ],
    data: () => ({
    }),
  }
</script>
