<template>
  <Result />
  <Summary />
</template>

<script>
import Result from './components/Result/Result.vue'
import Summary from './components/Summary/Summary.vue'

export default {
  name: 'App',
  components: {
    Result,
    Summary
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}

#app {
  max-height: 100vh;
  display: flex;
  flex-direction: column;
  margin: 0;
  padding: 0;
  width: 375px;
  box-sizing: border-box;

  @media (min-width: 1341px) {
    // for devices with width larger than 1440px
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
}
</style>