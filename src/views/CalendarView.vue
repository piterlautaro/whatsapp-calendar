<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <CalendaryComponent msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import CalendaryComponent from '@/components/Calendary.vue'

export default {
  name: 'CalendarView',
  components: {
    CalendaryComponent
  }
}
</script>
