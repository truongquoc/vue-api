<template>
  <div>
    <input type="text" v-model="message">
    <div>{{ message }}</div>
    <div>{{ reverseMessage }}</div>
    <div @click="increase">{{ counter }}</div>
  </div>
</template>

<script>
import {
  createComponent,
  setup,
  reactive,
  computed,
  ref
} from "@vue/composition-api";

export default {
  setup() {
    // Message
    const message = ref("hello world");

    const reverseMessage = computed(() => {
      return message.value
        .split("")
        .reverse()
        .join("");
    });

    // Misc
    const counter = ref(0);

    function increase() {
      counter.value++;
    }

    return {
      message,
      counter,
      reverseMessage,
      increase
    };
  }
};
</script>

<style>
</style>
