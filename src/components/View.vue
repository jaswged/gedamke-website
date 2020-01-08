<template>
  <div>
    <welcome />
    <resume/>
    <recent-projects />
    <about-me />
  </div>
</template>

<script>
export default {
  components: {
    AboutMe: () => import('@/components/AboutMe'),
    Resume: () => import('@/components/Resume'),
    RecentProjects: () => import('@/components/RecentProjects'),
    Welcome: () => import('@/components/Welcome')
  }
}
</script>
