<template>
  <div :class="['dialog']">
    <h2>Dialog</h2>
    <p>Test {{ test2 }}</p>
    <div>
      <slot name="default" />
    </div>
  </div>
</template>

<script setup>
const test2 = "hi";
</script>



<style scoped>
.dialog {
  width: 40%;
  background: yellow;
  padding: 10px;
}

.dialog div {
  display: flex;
  justify-content: space-between;
}

.dialog div a {
  background: white;
  padding: 4px;
}
</style>
