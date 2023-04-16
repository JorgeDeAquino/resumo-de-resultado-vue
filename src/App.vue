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
#app {
  max-height: 100vh;
  display: flex;
  flex-direction: column;
  margin: 0;
  padding: 0;
  width: 375px;
  box-sizing: border-box;
}

</style>

