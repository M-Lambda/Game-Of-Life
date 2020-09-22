<template>
  <a-layout id="gol" style="min-height: 100vh">
    <a-layout-sider v-model="collapsed" collapsible>
      <a-menu theme="dark" :default-selected-keys="['1']" mode="inline">
        <a-menu-item class="logo" key='0'>
          <nuxt-link to='/'>
            <a-icon type="border-outer" />
            <span>Game of Life</span>
          </nuxt-link>
        </a-menu-item>
        <a-menu-item key="1">
          <nuxt-link to='/info'>
            <a-icon type="info-circle" />
            <span>Info</span>
          </nuxt-link>
        </a-menu-item>
        <a-menu-item key="2">
          <a-icon type="desktop" />
          <span>Option 2</span>
        </a-menu-item>
        <a-sub-menu key="sub1">
          <span slot="title"><a-icon type="user" /><span>User</span></span>
          <a-menu-item key="3">
            Tom
          </a-menu-item>
          <a-menu-item key="4">
            Bill
          </a-menu-item>
          <a-menu-item key="5">
            Alex
          </a-menu-item>
        </a-sub-menu>
        <a-sub-menu key="sub2">
          <span slot="title"><a-icon type="team" /><span>Team</span></span>
          <a-menu-item key="6">
            Team 1
          </a-menu-item>
          <a-menu-item key="8">
            Team 2
          </a-menu-item>
        </a-sub-menu>
        <a-menu-item key="9">
          <a-icon type="file" />
          <span>File</span>
        </a-menu-item>
      </a-menu>
    </a-layout-sider>
    <a-layout>
      <a-layout-content :style="{ margin: '24px', padding: '24px', background: '#fff'}">
        <Nuxt/>
      </a-layout-content>
      <a-layout-footer :style="{textAlign: 'center'}">
        <div :style="{ fontSize: '18px' }">
          <a href='https://github.com/MaryamMosstoufi' target="blank">
            <a-icon type="github"/>
          </a>  
          <a href='https://www.linkedin.com/in/maryammosstoufi/' target="blank">
            <a-icon type="linkedin" theme="filled" />
          </a>  
        </div> 
        <div>
        Game of Life ©2020 Created by Maryam Mosstoufi 
        </div>
      </a-layout-footer>
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

<style>
#gol .logo {
  height: 32px;
  font-size: 18px;
  font-weight: 600;
  background: transparent !important;
}
#gol .logo a {
  color: white !important;
}

#gol .logo i {
  margin-right: 12px;
}
</style>