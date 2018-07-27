<template>
  <div id="app">
    <div id="hover"></div>
    <keep-alive>
      <router-view v-if="$route.meta.keepAlive"></router-view>
    </keep-alive>
    <router-view v-if="!$route.meta.keepAlive"></router-view>
  </div>
</template>

<script>
export default {
  beforeCreate() {
    
  }
};
</script>
<style>
html,
body {
  height: 100%;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#app {
  /*height:100%;爱车频道无法下拉*/
  height: 100%;
  box-sizing: border-box;
}
#hover {
  display: none;
  position: fixed;
  transform: translateZ(0);
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: #000;
  z-index: 1000;
  justify-content: center;
  align-items: center;
}
</style>
