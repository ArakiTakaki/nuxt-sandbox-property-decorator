<template lang="pug">
.root
  input(type="text" :value="$props.value" @input="onInput")
</template>

<script>
import Vue from "vue";
import { Component, Prop, Model, Emit } from "vue-property-decorator";

@Component({
  props: {
    value: String
  },
  model: {
    prop: 'value',
    event: 'input'
  }
})
class Input extends Vue {
  @Emit('input')
  onInput(event) {
    return event.target.value;
  }
}

export default Input;
</script>

<style lang="scss" scoped>
//
</style>

