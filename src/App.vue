<template>
  <input id="input-number" v-model="inputNumber" type="number" />
  <h2>{{ result }}</h2>
</template>

<script>
import { computed, ref } from "vue";
export default {
  setup() {
    const inputNumber = ref();
    const result = computed(() => (inputNumber.value >= 50 ? "Pass" : "Fail"));

    return {
      inputNumber,
      result,
    };
  },
};
</script>
