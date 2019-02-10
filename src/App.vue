<template>
  <div id="app">
    <p>
      <MyInput v-model="message" label="Your tweet:" :max="20"/>
    </p>
    <div class="box">
      <p>Preview:</p>
      <p>{{ message }}</p>
    </div>
  </div>
</template>

<script>
import MyInput from './components/MyInput.vue'

export default {
  name: 'app',
  data: () => ({
    message: 'Hello world'
  }),
  components: {
    MyInput
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

.box {
  border: solid 1px #333;
}
</style>
