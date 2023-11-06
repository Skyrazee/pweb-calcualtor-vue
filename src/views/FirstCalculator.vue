<template>
  <main>
    <h1>Calculator Web </h1>
    <h3>Nama : Muhammad Arsy Athallah</h3>
    <h3>NRP : 5027221048</h3>

    <input type="number" v-model.number="first" placeholder="Input here" />
    <input type="number" v-model.number="second" placeholder="Input here" />

    <br />
    <br />

    <input type="button" value="+" @click="addCalc" />
    <input type="button" value="-" @click="subCalc" />
    <input type="button" value="*" @click="multiCalc" />
    <input type="button" value="/" @click="divCalc" />

    <br />
    <br />

    <input v-model="result" readonly />
  </main>
</template>

<script>
export default {
  data() {
    return {
      first: '',
      second: '',
      result: ''
    }
  },
  methods: {
    addCalc() {
      this.result = this.first + this.second
    },
    subCalc() {
      this.result = this.first - this.second
    },
    multiCalc() {
      this.result = this.first * this.second
    },
    divCalc() {
      this.result = this.first / this.second
    }
  }
}
</script>
