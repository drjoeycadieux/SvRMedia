<script>
export default {
  data() {
    return {
      c: 0,
      f: 32
    }
  },
  methods: {
    setC(e, c = +e.target.value) {
      this.c = c
      this.f = c * (9 / 5) + 32
    },
    setF(e, f = +e.target.value) {
      this.f = f
      this.c = (f - 32) * (5 / 9)
    }
  }
}
</script>


<template>
  <div class="header-top-menu">
    <h1 class="header-text">
      Weather | Temperature Converter
    </h1>
  </div>
  <br>
  <br>
  <div class="wx-converter-container">
    <h1 class="title">
      Converter
    </h1>
    <br>
    <input type="number" :value="c" @change="setC"> Celsius =
    <input type="number" :value="f" @change="setF"> Fahrenheit
  </div>
</template>


<style scoped>
.header-top-menu {
  padding: 25px;
  background-color: rgb(46, 100, 174);
}

.title {
  font-family: sans-serif;
  color: white;
}

.header-top-menu .header-text {
  text-align: center;
  font-family: sans-serif;
  font-weight: bold;
  font-size: 40px;
  color: white
}

.wx-converter-container {
  padding: 25px;
  padding-top: 100px;
  text-align: center;
  background-color: rgb(46, 100, 174);
  width: 900px;
  margin: auto;
  border-radius: 15px;
}

input[type=number] {
  padding: 10px;
  outline: none;
  color: black;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
</style>