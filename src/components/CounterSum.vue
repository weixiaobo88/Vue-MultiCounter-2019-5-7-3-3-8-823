<template>
  <div>
    <h2>sum: {{sum}} </h2>
  </div>
</template>

<script>
export default {
  name: 'CounterSum',
  props: {
    sum: Number
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
