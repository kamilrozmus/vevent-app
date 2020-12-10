<template>
  <div class="content">
    <Nuxt />
  </div>
</template>
<script>

export default {
  name: 'DefaultLayout',
}
</script>

<style lang="scss" scoped>
html {
  font-family: 'Montserrat', sans-serif;
  font-size: 1em;
  word-spacing: .1em;
  line-height: 1.4;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}

*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  max-width: 60em;
  margin: 1em auto;
}
</style>
