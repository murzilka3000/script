<script setup>
import chat from './components/chat/chat.vue';
import search from './components/search/Search.vue';
import profile from './components/profile/Profile.vue';
import message from './components/message/Message.vue';

</script>

<template>
  <div :class="$style.height">
      <div :class="$style.grid">
        <chat :class="$style.chat"/>
        <search/>
        <profile :class="$style.profile"/>
    </div>
    <message :class="$style.message"/>
  </div>
</template>


<style module scoped>

.message {
  z-index: 1212121;
  position: fixed;
  bottom: 24px;
  right: 24px;
  left: 0;
}


.grid {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  gap: 24px;
  padding: 24px;
  height: calc(100vh - 48px);
}


@media screen and (max-width: 1270px) {
   .profile {
    display: none;
  } 

  .grid {
  grid-template-columns: 1fr 2fr;
}
} 

@media screen and (max-width: 882px) {

    .chat {
      display: none;
    }

    .grid {
      grid-template-columns: 1fr;
      padding: 16px;
    }

    .grid {
      display: grid;
      gap: 24px;
      padding:  0 24px;
      height: 100vh;
    }

    .message {
      bottom: 124px;
    }
}
</style>
