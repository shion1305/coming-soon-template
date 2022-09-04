<script setup>

import TextBouncing from "@/components/TextBouncing";
</script>
<template>
  <div class="home">
    <TextBouncing text="Coming Soon..." color="#ffffff" class="text-bouncing"/>
    <div class="title-below">タイトルタイトル</div>
  </div>
</template>
<style>
body {
  margin: 0;
}
</style>
<style scoped>
.title-below {
  background: linear-gradient(-90deg, #3DC2F5, #6E9AFF, #422EE6, #B65EFF, #F757FA);
  -webkit-background-clip: text;
  font-size: 0.6em;
  color: transparent;
}

.home {
  animation: gradient 15s ease infinite;
  height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-size: 12vw;
}

@media screen and (min-width: 480px) {
  .home {
    font-size: 10vw;
  }
}

@media screen and (min-width: 1024px) {
  .home {
    font-size: 8vw;
  }
}
</style>
