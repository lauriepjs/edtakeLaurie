<template>
  <div class="header">
    <nuxt-link to="/">Accueil</nuxt-link>
    <nuxt-link to="/gantttask">Gantt</nuxt-link>
  </div>
</template>


<script>

export default {
  name: 'Navbar'
}
</script>

<style scoped>

.header {
  display: flex;
  margin-bottom: 20px;
  justify-content: center;
  height: 30px;
}
a {
  margin-right: 20px;
  font-size: 23px;
  color: #00558A;
  text-decoration: none;
  text-transform: uppercase;
  padding-top: 2px;
  padding-bottom: 2px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  transition: color .25s;
  font-weight: 400;
  line-height: normal;
  cursor: pointer;
}
a:hover {
  color: #00558A;
}
a.nuxt-link-active {
  color: #00558A;
  border-top: 2px solid #00558A;
  border-bottom: 2px solid #00558A;
  font-weight: 600;
}
</style>