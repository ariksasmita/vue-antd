<template>
  <div id="app">
    <img alt="Vue logo" src="https://vuejs.org/images/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <a-button>
      <template #icon><SearchOutlined /></template>
    </a-button>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import { Button } from 'ant-design-vue';
import { SearchOutlined } from '@ant-design/icons-vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    AButton: Button,
    SearchOutlined,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
