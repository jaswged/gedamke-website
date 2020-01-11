<template>
  <div>
    <v-btn v-for="(item, i) in items.slice(0, large ? items.length : 3)" 
            :key="i" fab class="ma-2" :large="large" color="info" :href='item.link'>
      <v-icon dark v-text="item.icon"/>
    </v-btn>
  </div>
</template>

<script>
export default {
  props: {
    large: {
      type: Boolean,
      default: false
    }
  },
  data: () => ({
    items: [
      {
        name: 'LinkedIn',
        icon: 'mdi-linkedin',
        link: 'https://linkedin.com/in/jasonwgedamke'
      },
      {
        name: 'GitHub',
        icon: 'mdi-github-circle',
        link: 'https://github.com/jaswged'
      },
      {
        name: 'Email',
        icon: 'mdi-gmail',
        link: 'mailto:jaswged@gmail.com'
      },
      {
        name: 'GitHub',
        icon: 'mdi-github-box',
        link: 'https://github.com/jaswged'
      }
    ]
  })
}
</script>
