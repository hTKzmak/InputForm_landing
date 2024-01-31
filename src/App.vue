<template>
  <Main :data="data"/>
</template>

<script>
import Main from './components/Main.vue'

export default {
  components: { Main },
  data() {
    return {
      data: [
        { title: 'Name', type: 'text', placeholder: 'Your Name' },
        { title: 'Phone Number', type: 'tel', placeholder: '(123) 456 - 7890' },
        { title: 'Email', type: 'email', placeholder: 'Your Mail ID' },
        { title: 'Date', type: 'text', placeholder: 'dd - mm - yyyy' },
      ]
    }
  }
}
</script>

<style>
</style>
