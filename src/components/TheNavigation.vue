<template>
  <nav class="sticky top-0 w-full bg-white px-6 shadow-lg">
    <div class="flex items-center justify-between">
      <div class="flex h-16 space-x-6">
        <div class="flex items-center space-x-4">
          <TerminalIcon class="h-12 w-12 text-teal-500" />
          <div class="font-semibold">&lt;CodeFlow /&gt;</div>
        </div>
        <router-link
          v-for="item in navigation"
          :key="item.name"
          v-slot="{ href, navigate, isActive }"
          :to="item.to"
          custom
        >
          <a
            :href="href"
            class="group relative flex w-16 items-center justify-center"
            @click="navigate"
          >
            <div
              class="font-semibold group-hover:text-gray-800"
              :class="[!isActive && 'font-semibold text-gray-400']"
            >
              {{ item.name }}
            </div>
            <div
              class="absolute h-full w-full border-b-2"
              :class="[
                isActive
                  ? 'block border-teal-500'
                  : 'hidden border-transparent text-gray-400',
              ]"
            ></div>
          </a>
        </router-link>
      </div>
      <div>
        <a href="">
          <img
            class="h-10 w-10 rounded-full border-2 ring-teal-500 hover:ring-2"
            src="https://images.unsplash.com/photo-1532073150508-0c1df022bdd1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
            alt=""
          />
        </a>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { TerminalIcon } from '@heroicons/vue/outline';
const navigation = [
  {
    name: 'Home',
    to: '/',
    current: true,
  },
  {
    name: 'About',
    to: '/about',
    current: false,
  },
];
</script>
