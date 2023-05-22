<template>
  <a @click="handleClick">
    <slot name="default" />
  </a>
</template>

<script setup>
import { defineEmits, defineProps } from "vue";

const props = defineProps(["returnValue"]);
const emit = defineEmits(["buttonClick"]);

function handleClick() {
  console.log(props.returnValue);
  emit("buttonClick", props.returnValue);
}
</script>
