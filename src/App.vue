<template>
  <div id="app">
    <a-layout>
      <a-layout-sider>Sider</a-layout-sider>
      <a-layout>
        <a-layout-header>Header</a-layout-header>
          <a-layout-content>
            <a-button>
              <template #icon><SearchOutlined /></template>
            </a-button>
            <img alt="Vue logo" src="https://vuejs.org/images/logo.png" />
            <HelloWorld msg="Welcome to Your Vue.js App" />
          </a-layout-content>
        <a-layout-footer>Footer</a-layout-footer>
      </a-layout>
    </a-layout>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import { Button, Layout, LayoutContent, LayoutFooter, LayoutSider } from 'ant-design-vue';
import { SearchOutlined } from '@ant-design/icons-vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    AButton: Button,
    ALayout: Layout,
    ALayoutContent: LayoutContent,
    ALayoutFooter: LayoutFooter,
    ALayoutSider: LayoutSider,
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
}
</style>
