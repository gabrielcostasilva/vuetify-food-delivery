<template>
  <v-chip class="ml-n5" color="green" outlined text-color="black" small>
    <v-icon left x-small @click="increaseValue"> fas fa-plus </v-icon>
    <v-divider vertical inset class="mr-1"></v-divider>
    {{ currentValue }}
    <v-divider vertical inset class="ml-1"></v-divider>
    <v-icon right x-small @click="decreaseValue"> fas fa-minus </v-icon>
  </v-chip>
</template>

<script>
export default {
  props: {
      initValue: {
          default: 0
      },
      maxValue: {
          default: 3
      },
      minValue: {
          default: 0
      }
  },
  beforeMount() {
      this.currentValue = this.initValue
  },
  data() {
    return {
      currentValue: 0
    }
  },
  methods: {
    increaseValue() {
      if (this.currentValue < this.maxValue) {
        this.currentValue++
        this.$emit('currentValue', this.currentValue)
      }
    },
    decreaseValue() {
      if (this.currentValue > this.minValue) {
        this.currentValue--
        this.$emit('currentValue', this.currentValue)
      }
    },
  },
}
</script>

<style></style>
