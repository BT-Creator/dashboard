<template>
  <div class="loading">
      <span></span>
      <span></span>
      <span></span>
  </div>
</template>

<script>
export default {
    name: 'LoadingAnimation'
}
</script>

<style lang="scss" scoped>
.loading {
  span {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background-color: white;
    animation: flashing 1.4s infinite linear;
    margin: 0 4px;
    display: inline-block;

    &:nth-child(2) {
      animation-delay: 0.2s;
    }

    &:nth-child(3) {
      animation-delay: 0.4s;
    }
  }
}

@keyframes flashing {
    0% {
      opacity: 0.2;
    }
    20% {
      opacity: 1;
    }
    100% {
      opacity: 0.2;
    }
  }

</style>
