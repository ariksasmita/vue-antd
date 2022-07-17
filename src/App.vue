<template>
  <div id="app">
    <a-layout style="min-height: 100vh">
      <sidebar></sidebar>
      <a-layout>
        <a-layout-content style="padding: 2rem">
          <router-view/>
          <a-button>
            <template #icon><SearchOutlined /></template>
          </a-button>
        </a-layout-content>
        <a-layout-footer>Footer</a-layout-footer>
      </a-layout>
    </a-layout>
  </div>
</template>

<script>
import { Button, Layout, LayoutContent, LayoutFooter /*, LayoutSider  */} from 'ant-design-vue';
import { SearchOutlined } from '@ant-design/icons-vue';
import Sidebar from '@/components/general/Sidebar.vue'

export default {
  name: 'App',
  components: {
    AButton: Button,
    ALayout: Layout,
    ALayoutContent: LayoutContent,
    ALayoutFooter: LayoutFooter,
    // ALayoutSider: LayoutSider,
    SearchOutlined,
    Sidebar,
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
