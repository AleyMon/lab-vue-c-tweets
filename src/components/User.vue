<!-- User.vue -->
<script setup>
const props = defineProps({
  userData: Object
});
</script>

<template>
    <span class="user">
      <span class="name">{{ userData.name }}</span>
      <span class="handle">@{{ userData.handle }}</span>
    </span>
  </template>
  

  