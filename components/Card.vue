<script setup lang="ts">
interface CardProps {
  card: {
    img: string;
    title: string;
    author: string;
  };
}
const { isDarkMode } = useDarkMode();
const props = defineProps<CardProps>();
</script>

<template lang="pug">
.card(:style="isDarkMode ? { backgroundColor: 'black', color: 'white' } : null")
  img(:src="card.img")
  .content
    h3 {{ card.title }}
    p {{ card.author }}

</template>

<style scoped>
.card {
  box-shadow: 1px 1px 5px black;
  background: white;
  width: 30%;
  margin-bottom: 30px;
  border-radius: 5px;
  overflow: hidden;
}
img {
  width: 100%;
  height: 200px;
}
.content {
  padding: 10px;
}
p {
  margin-top: 10px;
}
</style>
