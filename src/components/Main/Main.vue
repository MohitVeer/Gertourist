<template>
  <div class="flex container mx-auto">
    <div class="h-14">
      <v-navigation-drawer app>
        <Sidebar />
      </v-navigation-drawer>
    </div>
    <div style="width: 62%; margin-left: 30px; margin-right: 30px" class="...">
      <!-- <Dashboard /> -->
    </div>
    <div class="flex-initial w-14 ...">
      <v-navigation-drawer app>
        <RightSidebar />
      </v-navigation-drawer>
    </div>
  </div>
</template>

<script>
// import Rightside from '../components/Rightside.vue'
// import Middle from '../components/Middle.vue'
import Sidebar from '../sidebar/Sidebar.vue'
// import Dashboard from '../../views/Dashboard.vue'
import RightSidebar from '../RightSidebar/RightSidebar.vue'
export default {
  name: 'Main',
  components: {
    // Rightside,
    // Middle,
    Sidebar,
    // Dashboard,
    RightSidebar
  }
}
</script>

<style scoped>
.container {
  width: 100%;
}

hr {
  border: 1px solid #f5f5f5;
  border-style: dashed;
}
</style>
