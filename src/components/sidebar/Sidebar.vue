<script>
import SidebarLink from './SidebarLink'
import { collapsed, toggleSidebar, sidebarWidth } from './state'

export default {
  props: {},
  components: { SidebarLink },
  setup() {
    return { collapsed, toggleSidebar, sidebarWidth }
  }
}
</script>

<template>
  <div class="sidebar">
    <!-- <h1>
      <span v-if="collapsed">
        <div>G</div>
        <div>T</div>
      </span>
      <span v-else>Geotourist</span>
    </h1> -->
    <div class="overflow-y-auto py-4 px-3 bg-gray-50 rounded dark:bg-gray-800">
      <ul class="space-y-2 text-left">
        <li>
          <a
            href="#"
            class="
              flex
              items-center
              p-2
              text-base
              font-normal
              text-gray-900
              rounded-lg
              dark:text-white
              hover:bg-gray-100
              dark:hover:bg-gray-700
            "
          >
            <span class="ml-3" style="border-bottom: 1px solid blue">
              <SidebarLink to="/">Description</SidebarLink>
            </span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="
              flex
              items-left
              p-2
              text-base
              font-normal
              text-gray-900
              rounded-lg
              dark:text-white
              hover:bg-gray-100
              dark:hover:bg-gray-700
            "
          >
            <span class="flex-1 ml-3 whitespace-nowrap">
              <SidebarLink to="">Points</SidebarLink>
            </span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="
              flex
              items-center
              p-2
              text-base
              font-normal
              text-gray-900
              rounded-lg
              dark:text-white
              hover:bg-gray-100
              dark:hover:bg-gray-700
            "
          >
            <span
              class="
                inline-flex
                justify-center
                items-center
                p-3
                ml-3
                w-3
                h-3
                text-sm
                font-medium
                text-blue-600
                bg-blue-200
                rounded-full
                dark:bg-blue-900
                dark:text-blue-200
              "
            >
              1
            </span>
            <span class="flex-1 ml-3 whitespace-nowrap">
              <SidebarLink to="/dashboard">Abbesses Metro Station</SidebarLink>
            </span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="
              flex
              items-center
              p-2
              text-base
              font-normal
              text-gray-900
              rounded-lg
              dark:text-white
              hover:bg-gray-100
              dark:hover:bg-gray-700
            "
          >
            <span
              class="
                inline-flex
                justify-center
                items-center
                p-3
                ml-3
                w-3
                h-3
                text-sm
                font-medium
                text-blue-600
                bg-blue-200
                rounded-full
                dark:bg-blue-900
                dark:text-blue-200
              "
            >
              2
            </span>
            <span class="flex-1 ml-3 whitespace-nowrap">
              <SidebarLink to="/friends">
                Pigalle and the Moulin R...
              </SidebarLink>
            </span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="
              flex
              items-center
              p-2
              text-base
              font-normal
              text-gray-900
              rounded-lg
              dark:text-white
              hover:bg-gray-100
              dark:hover:bg-gray-700
            "
          >
            <span
              class="
                inline-flex
                justify-center
                items-center
                p-3
                ml-3
                w-3
                h-3
                text-sm
                font-medium
                text-blue-600
                bg-blue-200
                rounded-full
                dark:bg-blue-900
                dark:text-blue-200
              "
            >
              +
            </span>
            <span class="flex-1 ml-3 whitespace-nowrap">
              <SidebarLink to="/image">Create New Point</SidebarLink>
            </span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="
              flex
              items-center
              p-2
              text-base
              font-normal
              text-gray-900
              rounded-lg
              dark:text-white
              hover:bg-gray-100
              dark:hover:bg-gray-700
            "
          >
            <span class="flex-1 ml-3 whitespace-nowrap">Media</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="
              flex
              items-center
              p-2
              text-base
              font-normal
              text-gray-900
              rounded-lg
              dark:text-white
              hover:bg-gray-100
              dark:hover:bg-gray-700
            "
          >
            <span class="flex-1 ml-3 whitespace-nowrap">Settings</span>
          </a>
        </li>
      </ul>
    </div>

  </div>
</template>

<style>
:root {
  --sidebar-item-hover: #d3dce0;
  --sidebar-item-active: #0091de;
}
</style>

<style scoped>
.sidebar h1 {
  height: 3em;
}

.collapse-icon {
  position: absolute;
  bottom: 0;
  padding: 0.75em;

  color: black;

  transition: 0.2s linear;
}

.rotate-180 {
  transform: rotate(180deg);
  transition: 0.2s linear;
}
</style>
