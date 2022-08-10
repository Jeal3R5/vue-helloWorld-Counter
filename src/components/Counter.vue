<!-- Composition API Method -->

<template>
  <div>
    <h1 @click="addOne">{{ counter }}</h1>
    <h2>{{ cheese }}</h2>
    <h3 v-for="num in arr" :key="num">{{ num }}</h3>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "Counter",
  props: ["cheese"],
  setup() {
    const counter = ref(0);

    const addOne = () => (counter.value += 1);

    return { counter, addOne };
  },
};
</script>
