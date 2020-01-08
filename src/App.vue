<template>
  <v-app>
    <core-toolbar />

    <core-view />

    <Footer />
  </v-app>
</template>

<script>
export default {
  components: {
    Footer: () => import('@/components/Footer'),
    CoreToolbar: () => import('@/components/Toolbar'),
    CoreView: () => import('@/components/View')
  }
}
</script>
<style>
  .v-application .info{
    background-color: #424242 !important;
    border-color: #0064A2 !important;
  }
</style>