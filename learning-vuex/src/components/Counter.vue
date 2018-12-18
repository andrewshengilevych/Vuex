<template>
    <div>
        <h1>Counter</h1>
        <div> {{ count }} </div>
        <p>
            <button @click="increment">+</button>
            <button @click="decrement">-</button>
        </p>
    </div>
</template>

<script>
export default 
{
  name: 'Counter',
  computed: {
      count () {
          return this.$store.state.count
      }
  },
  methods: {
    increment () {
        this.$store.commit('increment')
    },
    decrement () {
        this.$store.commit('decrement')
    }
  }
}
</script>