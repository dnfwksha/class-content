<template>
  <h1>{{ reverseMessage()}}</h1>
  <h1>{{ reverseMessage()}}</h1>
  <h1>{{ reverseMessage()}}</h1>
  <h1>{{ reverseMessage()}}</h1>
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello Computed!'
    }
  },
  computed: {
    reversedMessage() {
      return this.msg.split('').reverse().join('')
    }
  },
  methods: {
    reverseMessage() {
      return this.msg.split('').reverse().join('')
    }
  }
}
</script>

<style scoped>
.aa {
  font-size: 100px;
}

</style>