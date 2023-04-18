<script setup>
import { Menu, MenuButton, MenuItems, MenuItem } from '@headlessui/vue'
</script>
<template>
  <div class="">
    <Menu as="div" class="relative inline-block text-right">
      <div>
        <MenuButton class="py-4 p-x3" >
          <img src="/nav-hamburger.png" alt="navigation dropdown symbol" width="auto" height="auto" class="navHamburger">
        </MenuButton>
      </div>

      <transition
        enter-active-class="transition duration-100 ease-out"
        enter-from-class="transform scale-95 opacity-0"
        enter-to-class="transform scale-100 opacity-100"
        leave-active-class="transition duration-75 ease-in"
        leave-from-class="transform scale-100 opacity-100"
        leave-to-class="transform scale-95 opacity-0"
      >
        <MenuItems class="navdropdown">
          <div class="px-1 py-1 ">
            <MenuItem v-slot="{ active }">
              <a
                href="/"
                :class="[
                  active ? 'bg-violet-500 text-white' : 'text-gray-900',
                  'group flex w-full justify-end rounded-md px-2 py-2 text-sm text-right ',
                ]"
              >
               Home 
            </a>
            </MenuItem>
          </div>
          <div class="px-1 py-1">
            <MenuItem v-slot="{ active }">
              <a
                href="/about"
                :class="[
                  active ? 'bg-violet-500 text-white' : 'text-gray-900',
                  'group flex w-full justify-end items-center rounded-md px-2 py-2 text-sm',
                ]"
              >
                About Us
            </a>
            </MenuItem>
          </div>

          <div class="px-1 py-1">
            <MenuItem v-slot="{ active }">
              <button
                :class="[
                  active ? 'bg-violet-500 text-white' : 'text-gray-900',
                  'group flex w-full justify-end items-center rounded-md px-2 py-2 text-sm',
                ]"
              >
               Services 
            </button>
            </MenuItem>
          </div>
          <div class="px-1 py-1">
            <MenuItem v-slot="{ active }">
              <button
                :class="[
                  active ? 'bg-violet-500 text-white' : 'text-gray-900',
                  'group flex w-full justify-end items-center rounded-md px-2 py-2 text-sm',
                ]"
              >
                Delete
            </button>
            </MenuItem>
          </div>
        </MenuItems>
      </transition>
    </Menu>
  </div>
</template>

<style scoped>
.navHamburger{
  width: 75px;
  height: 85px;
}
.navdropdown{
  background-color: rgba(255, 255, 255, 0.866);
  position: absolute;
  width: 800px;
  right: 0;
}
</style>
