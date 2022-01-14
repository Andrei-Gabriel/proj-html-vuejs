<template>
  <main>
    <Award/>
    <MensGrooming/>
  </main>
</template>

<script>
  import Award from './main_sections/Award.vue'
  import MensGrooming from './main_sections/MensGrooming.vue'

  export default {
      name: 'Main',
      components: {
        Award,
        MensGrooming,
      }
  }
</script>

<style scoped lang="scss">
  
</style>