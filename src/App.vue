<template>
  <v-app>
    <v-main>
      <v-toolbar>
        <p>v-breadcrumbs:</p>
        <v-breadcrumbs :items="crumbs"></v-breadcrumbs>

        <p class="ml-10">Working links:</p>
        <div class="d-flex ml-4" style="gap: 16px">
          <router-link v-for="crumb in crumbs" :key="crumb.to" :to="crumb.to">{{ crumb.text }}</router-link>
        </div>
        <router-view></router-view>
      </v-toolbar>
    </v-main>
  </v-app>
</template>

<script setup>

const crumbs = [
  {
    text: 'Home',
    to: '/',

  },
  {
    text: '1st',
    to: '/first',
    link: true,
  },
  {
    text: '2st',
    to: '/second'
  }
]
</script>
