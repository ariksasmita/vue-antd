<template>
  <a-layout-sider
    v-model:collapsed="collapsed"
    collapsible>
    <a-menu
      v-model:selectedKeys="selectedKeys"
      theme="dark">
      <a-menu-item key="1">
        <pie-chart-outlined></pie-chart-outlined>
        <router-link class="menu-label" to="/">Home</router-link>
      </a-menu-item>
      <a-menu-item key="2">
        <desktop-outlined></desktop-outlined>
        <router-link class="menu-label" to="/about">About</router-link>
      </a-menu-item>
      <a-menu-item key="3">
        <desktop-outlined></desktop-outlined>
        <router-link class="menu-label" to="/trade">Trade</router-link>
      </a-menu-item>
    </a-menu>
  </a-layout-sider>
</template>

<script>
import { PieChartOutlined, DesktopOutlined /* , UserOutlined */ } from '@ant-design/icons-vue';
import { LayoutSider, Menu, MenuItem } from 'ant-design-vue';
export default {
  name: 'SideBar',
  components: {
    ALayoutSider: LayoutSider,
    AMenuItem: MenuItem,
    AMenu: Menu,
    DesktopOutlined,
    PieChartOutlined,
  },
  data () {
    return {
      collapsed: false,
      selectedKeys: ['1']
    }
  },
  mounted () {
  }
}
</script>

<style scoped>
  .menu-label {
    margin-left: 2rem;
  }
</style>