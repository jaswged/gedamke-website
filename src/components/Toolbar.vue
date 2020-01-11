<template>
  <v-app-bar app v-scroll="onScroll" :color="isTransparent ? 'transparent' : '#e8e8e8'" flat >
    <v-toolbar-title v-if="!isTransparent"
    class="display-1 ml-3 text-uppercase hidden-sm-and-down" @click="$vuetify.goTo('#home', options)">
      Jason Gedamke
    </v-toolbar-title>
    <v-spacer />
    <SocialMedia />
  </v-app-bar>
</template>

<script>
export default {
  components: {
    SocialMedia: () => import('@/components/SocialMedia')
  },
  data: () => ({
    isTransparent: true
  }),
  methods: {
    onScroll () {
      this.isTransparent = window.pageYOffset < 200
    }
  }
}
</script>
<style>
  .v-application .info{
    background-color: #424242 !important;
    border-color: #0064A2 !important;
  }
</style>