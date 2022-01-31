<template>
  <div class="btn-group">
    <Button v-for="index in buttons" :key="index"/>
    <Button  @mousedown.native="increaseButtons()" :filled='false'/>
  </div>
</template>

<script>
import Button from './Button.vue'

// A group of buttons, aligned horizontally
// the last button is an add button that can add other buttons
export default {
  name: 'ButtonGroup',
  components: {
    Button
  },
  data: function () {
    return {
      buttons: 0
    }
  },
  methods: {
    increaseButtons() {
      this.buttons++;
    }
  }
}
</script>

<style scoped>
.btn-group {
  display: flex;
  flex-flow: row wrap;
  gap: 8px;
  width: 100%;
}
</style>