<template>
  <div>
    <NuxtLayout name="admin">
      <p>This is an counter page {{ counterStore.counter }}</p>
      <v-btn @click="counterStore.increment">Increment</v-btn>
    </NuxtLayout>
  </div>
</template>

<script>
import { useCounterStore } from '../store/counter';

export default {
  setup() {
    const counterStore = useCounterStore();

    return { counterStore };
  },
};
</script>

<style scoped></style>
