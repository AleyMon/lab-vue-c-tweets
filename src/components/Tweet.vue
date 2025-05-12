<script setup>
import ProfileImage from './ProfileImage.vue';
import User from './User.vue';
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';
import Actions from './Actions.vue';

// Recibe el objeto 'tweet' como prop
const props = defineProps({
  tweet: Object
});
</script>

<template>
  <div class="tweet">
    <ProfileImage :image="props.tweet.user.image" />

    <div class="body">
      <div class="top">
        <User :userData="props.tweet.user" />
        <Timestamp :time="props.tweet.timestamp" />
      </div>

      <Message :message="props.tweet.message" />
      <Actions />

      <!-- Este ícono forma parte de las acciones del tweet? -->
      <i class="fas fa-ellipsis-h"></i>
    </div> 
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>

<!-- Estructura final de archivos:
 
App.vue:
Aquí es donde se manejan los datos de los tweets (array tweets) y se iteran para renderizar múltiples componentes Tweet.

Tweet.vue:
Componente principal donde se muestran los datos del tweet. Utiliza subcomponentes como ProfileImage, User, Timestamp, Message, y Actions para estructurar el contenido de cada tweet.

ProfileImage.vue:
Componente encargado de mostrar la imagen de perfil del usuario.

User.vue:
Componente encargado de mostrar el nombre de usuario y el handle de Twitter.

Timestamp.vue:
Componente encargado de mostrar la fecha y hora del tweet.

Message.vue:
Componente encargado de mostrar el mensaje del tweet.

Actions.vue:
Componente encargado de mostrar los iconos de acción (comentarios, retweets, likes, compartir).

Resultado final:
App.vue contiene el array tweets con múltiples objetos que representan tweets.

Se usa v-for en App.vue para iterar sobre los tweets y renderizar múltiples componentes Tweet.

Cada componente Tweet recibe un objeto tweet y muestra la información correspondiente (imagen, nombre de usuario, mensaje, etc.) utilizando componentes modulares.
-->
