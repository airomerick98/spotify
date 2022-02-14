<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-size: $medium16;
}

p {
  margin: 0;
}

.bold {
  font-weight: bold;
}

body {
  margin: 0;
}

button, input {
  border: none;
}
</style>
