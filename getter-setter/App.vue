<template>
  <button @click="add">ADD</button>
  <h1>{{ reversedMessage }}</h1>
  <h1>{{ reversedMessage }}</h1>
  <h1>{{ reversedMessage }}</h1>
  <h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello Computed!'
    }
  },
  computed: {
    //Getter -> 별도로 내용 추가 불가(캐싱)
    //   reversedMessage() {
    //     return this.msg.split('').reverse().join('')
    //   }

    //Getter,Setter
    reversedMessage: {
      get() {
        return this.msg.split('').reverse().join('')
      },
      set(value) {
        this.msg = value
      }
    }
  },
  methods: {
    add() {
      // this.reversedMessage+='!?'
      this.reversedMessage += '!?'
    }
  }
}
</script>

<style scoped>
.aa {
  font-size: 100px;
}

</style>