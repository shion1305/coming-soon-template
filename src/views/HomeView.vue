<script setup>

// import TextBouncing from "@/components/TextBouncing";
</script>
<template>
  <div class="home">
<!--    <TextBouncing text="Coming Soon..." color="#ffffff" class="text-bouncing"/>-->
    <div>令和4</div>
  </div>
</template>
<style>
body{
  margin: 0;
}
</style>
<style scoped>
.home {
  animation: gradient 15s ease infinite;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.text-bouncing {
  margin: auto;
  vertical-align: middle;
}

</style>
