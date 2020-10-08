<template>
  <div id="app">
    <Navigation :user="user"/>
    <router-view :user="user"/>
  </div>
</template>

<script>
import db from './db.js'
import Navigation from '@/components/Navigation'

export default {
  name:'App',
  data: function() {
    return {
      user: null
    }
  },
  mounted() {
    db.collection('users')
      .doc('PSNArFzFw7wuaMGOu6e3')
      .get()
      .then(snapshot => {
        this.user = snapshot.data().name
      })
  },
  components: {
    Navigation
  }
}
</script>

<style lang="scss">
// $primary: #dddd;
@import 'node_modules/bootstrap/scss/bootstrap';
</style>
