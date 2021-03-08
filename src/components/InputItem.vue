<template>
  <div class="myContent">
    <v-menu
      offset-y
      :closeOnContentClick="false"
      v-model="menuOpen"
      class="myMenu"
    >
      <template v-slot:activator="{ attrs, on }">
        <div
          v-bind:class="!menuOpen && !myValue ? 'myLabelLarge' : 'myLabelSmall'"
        >
          {{ myLabel }}
        </div>
        <div class="mySpan" v-bind="attrs" @click="clicked" v-on="on">
          {{ myValue }}
        </div>
      </template>
      <v-card style="width:300px">
        <v-card-title>
          <div class="text-h2 blink-me">-</div>
          <div class="text-h2">-</div>
          <span class="text-h2">:</span>
          <div class="text-h2">-</div>
          <div class="text-h2">-</div>
          <span class="text-h2">:</span>
          <div class="text-h2">-</div>
          <div class="text-h2">-</div>
        </v-card-title>
        <v-card-text>
            <table>
                <tr>
                    <td><v-btn @click="add(0)" depressed>
                0
              </v-btn></td>
              <td> <v-btn @click="add(1)" depressed>
                1
              </v-btn></td>
              <td> <v-btn @click="add(2)" depressed>
                2
              </v-btn></td>
              <td> <v-btn @click="add(3)" depressed>
                3
              </v-btn></td>
                </tr>
            </table>
          

          <v-btn @click="clear" depressed>
            clear
          </v-btn>
        </v-card-text>
      </v-card>
    </v-menu>
  </div>
</template>

<script>
export default {
  name: "InputItem",
  props: ["inputLabel", "inputValue"],
  data: function() {
    return {
      myLabel: this.inputLabel,
      myValue: this.inputValue,
      isLarge: true,
      menuOpen: false,
    };
  },
  methods: {
    add: function(input) {
      this.myValue += input;
    },
    clear: function() {
      this.myValue = "";
    },
    clicked: function() {
      this.menuOpen = true;
      this.isLarge = false;
    },
  },
};
</script>

<style scoped>
.myContent {
  position: relative;
  height: 50px;
  width: 65px;
}

.mySpan {
  position: absolute;
  top: 20px;
  left: 0;
  width: 65px;
  height: 20px;
  z-index: 10;
  background: transparent;
  border-bottom: solid;
  border-width: 1px;
}

.myLabelSmall {
  top: 5px;
  position: absolute;
  font-size: x-small;
  transition: all 0.5s ease-in-out;
  z-index: 1;
}

.myLabelLarge {
  position: absolute;
  font-size: inherit;
  top: 19px;
  transition: all 0.5s ease-in-out;
  z-index: 1;
}

.myMenu {
  z-index: 20;
}

.blink-me {
  animation: blinker 1s linear infinite;
}

@keyframes blinker {
  50% {
    opacity: 0;
  }
}
</style>
