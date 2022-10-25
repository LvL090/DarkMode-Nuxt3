<script setup lang="ts">
const { isDarkMode } = useDarkMode();
</script>

<template lang="pug">
div(:style="isDarkMode ? { backgroundColor: 'black' } : null")
  Nav
  Heading
  Cards
</template>

<style>
* {
  margin: 0;
  padding: 0;
  font-family: Georgia;
}
</style>
