<script setup>
import Default from './components/Default.vue'
import Thanks from './components/Thanks.vue';

const transition = () => {
  const main = document.getElementById('main-container')
  main.classList.toggle('hidden')
}
</script>


<template>
  <Default />
  <Thanks />
</template>
