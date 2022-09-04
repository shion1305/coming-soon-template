<script setup>

const props = defineProps({
  text: {
    type: String
  },
  color: {
    type: String,
    required: false,
    default: "#2c3e50"
  }
})
</script>
<template>
  <div class="parent">
    <span v-for="t in props.text" :key="t.index" class="bouncing-text">
      {{ t }}
    </span>
  </div>
</template>

<style scoped lang="scss">

.bouncing-text {
  display: flex;
  line-height: 2;
  animation: bounce 4s ease infinite,
  gradient 20s ease alternate infinite;
  background: linear-gradient(-45deg, #3DC2F5, #6E9AFF, #422EE6, #B65EFF, #F757FA);
  -webkit-background-clip: text;
  color: transparent;
  background-size: 400% 400%;
}

.parent {
  display: flex;
}

@for $i from 1 through 15 {
  .bouncing-text:nth-child(#{$i}) {
    animation-delay: $i * 0.02s;
  }
}


@keyframes bounce {
  0% {
    transform: scale(1, 1) translateY(0);
  }
  2% {
    transform: scale(1.1, .85) translateY(0);
  }
  7% {
    transform: scale(.85, 1.2) translateY(-0.5em);
  }
  13% {
    transform: scale(1.05, .95) translateY(0);
  }
  18% {
    transform: scale(1, 1) translateY(-0.25em);
  }
  22% {
    transform: scale(1, 1) translateY(0);
  }
  25% {
    transform: scale(1, 1) translateY(0);

    100% {
      transform: scale(1, 1) translateY(0);
    }
  }
}

@keyframes gradient {
  0% {
    background-position: 0 0;
  }
  25% {
    background-position: 0 100%;
  }

  50% {
    background-position: 100% 100%;
  }

  100% {
    background-position: 100% 0%;
  }
}
</style>