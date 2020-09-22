<template>
  <a-layout id="components-layout-demo-custom-trigger">
    <a-layout-sider v-model="collapsed" :trigger="null" collapsible>
      <a-menu theme="dark" mode="inline" :default-selected-keys="['1']">
        <a-menu-item key="1">
          <nuxt-link to='/'>
            <a-icon type="border-outer" />
            <span>Game of Life</span>
          </nuxt-link>
        </a-menu-item>
        <a-menu-item key="2">
          <a-icon type="setting" />
          <span>Settings</span>
        </a-menu-item>
        <a-menu-item key="3">
          <nuxt-link to='/rules'>
            <a-icon type="profile" />
            <span>Rules</span>
          </nuxt-link>
        </a-menu-item>
        <a-menu-item key="4" href='/about'>
          <nuxt-link to='/about'>
            <a-icon type="user" />
            <span> About </span>
          </nuxt-link>
        </a-menu-item>
      </a-menu>
    </a-layout-sider>
    <a-layout>
      <a-layout-content
        :style="{ margin: '24px', padding: '24px', background: '#fff', minHeight: '280px' }"
      >
        <Nuxt />
      </a-layout-content>
    </a-layout>
  </a-layout>
</template>
<script>
export default {
  data() {
    return {
      collapsed: false,
    };
  },
};
</script>