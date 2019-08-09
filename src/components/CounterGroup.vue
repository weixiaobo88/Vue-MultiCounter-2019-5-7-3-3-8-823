<template>
  <div class="counter">
    <h1>Counter</h1>
    {{counterNum}} counters
    <counter
      v-for="index in counterNum"
      :key="index"
      @get-current="showCurrent"
    />
  </div>
</template>

<script>
import Counter from './Counter.vue'

export default {
  name: 'CounterGroup',
  props: {
    counterNum: Number
  },
  components: {
    Counter
  },
  methods: {
    showCurrent: function (current) {
      this.$emit('show-current',current);
  }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
button {
  margin: 0 20px;
}
</style>
