
<template>
  <nav class="navbar bg-body-tertiary">
    <div class="container-fluid">
      <router-link class="navbar-brand" :to="{name: 'main'}"
      >Portal</router-link>
    </div>
  </nav>
  <div class="container">
    
    <router-view />
  </div>
</template>


<script>
export default {

}
</script>

<style scoped></style>
