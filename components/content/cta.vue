<template>
  <div>
    <button @click="test" style="background-color: red">
      <slot />
    </button>
  </div>
</template>
<script setup>
const test = () => {
  console.log("here");
};
</script>
