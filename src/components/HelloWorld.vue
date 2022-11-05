<script setup>
import TestComponentVue from "./TestComponent.vue";
const props = defineProps({
  modelValue: String,
});

const emit = defineEmits(["update:modelValue"]);

const updateValue = (event) => {
  emit("update:modelValue", event.target.value);
};
</script>

<template>
  <div class="main">
    <h2>入力欄</h2>
    <TestComponentVue />
    <input type="text" :value="modelValue" @input="updateValue" />
  </div>
</template>

<style scoped>
.main {
  background-color: gold;
  color: black;
}
</style>
