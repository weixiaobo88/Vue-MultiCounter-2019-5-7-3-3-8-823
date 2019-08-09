<template>
  <div id="app">
    <counter-group :counter-num="counterNum" @show-current="updateSum" />
    <counter-sum :sum="sum"  />
  </div>
</template>

<script>
import CounterGroup from './components/CounterGroup.vue'
import CounterSum from './components/CounterSum.vue'

export default {
  name: 'app',
  data() {
    return {
      counterNum: 3,
      sum: 0
    }
  },
  components: {
    CounterGroup,
    CounterSum
  },
  methods: {
    updateSum(current) {
        this.sum += current;
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
