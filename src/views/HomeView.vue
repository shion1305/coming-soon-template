<script setup>

import TextBouncing from "@/components/TextBouncing";
</script>
<template>
  <div class="home">
    <TextBouncing text="Coming Soon..." color="#ffffff" class="bouncing-text"/>
    <div class="title-below">令和5年<br><span>「がんの痛みは</span><span>正しい知識で取る」</span><br>市民向けシンポジウム</div>
  </div>
</template>
<style>
body {
  margin: 0;
}
</style>
<style scoped lang="scss">
.title-below {
  background: linear-gradient(-90deg, #59E4EB, #27F2A3, #2DDB4A);
  -webkit-background-clip: text;
  font-size: 0.6em;
  color: transparent;
  > span {
    display: inline-block;
  }
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
