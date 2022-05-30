<script>
import { sidebarWidth } from '@/components/sidebar/state'
import Header from './components/Header/Header.vue'
import Main from './components/Main/Main.vue'
export default {
  components: { Header, Main },
  setup() {
    return { sidebarWidth }
  }
}
</script>
<template>
  <Header />
  <Main />
  <!-- <Sidebar /> -->
  <div :style="{ 'margin-left': sidebarWidth }">
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
