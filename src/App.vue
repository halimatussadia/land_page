<template>
<!--  <Sadia></Sadia>-->
  <Navbar></Navbar>
  <MainNavbar></MainNavbar>


</template>

<script>
  import Navbar from './components/Navbar.vue'
  import MainNavbar from './components/MainNavbar.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    MainNavbar,
  }
}
</script>

