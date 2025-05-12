<!-- Message.vue
Este componente:
    Recibe una prop message
    Muestra el mensaje dentro de un <p> con clase "message" 
-->
    
<script setup>
const props = defineProps({
  message: String
});
</script>

<template>
    <p class="message">{{ message }}</p>
  </template>
  

  