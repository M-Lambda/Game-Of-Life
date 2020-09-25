<template>
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
      <nuxt-link to='/info'>Conway's Game of Life</nuxt-link>
    </div>
  </a-layout-footer>
</template>

<script>
export default {}
</script>

<style scoped>
.ant-layout-footer{
  text-align: center;
  background:#001529;
  color: hsl(209, 63%, 19%);
  padding: 10px;
}
a{
  color: hsl(209, 63%, 19%);
}
</style>