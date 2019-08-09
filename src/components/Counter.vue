<template>
  <div class="counter">
    <p>
      <button class="btn" @click="decrement">-</button>
      <span>{{count}}</span>
      <button class="btn" @click="increment">+</button>
    </p>
  </div>
</template>

<script>
export default {
  name: 'Counter',
  data() {
    return { count: 0 };
  },
  methods: {
    increment() {
      this.count += 1;  
      this.$emit('get-current', 1)
    },
    decrement() {
      this.count -= 1;
      this.$emit('get-current', -1)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.btn {
  margin: 0 20px;
}
</style>
