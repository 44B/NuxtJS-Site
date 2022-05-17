<template>
  <div>  
    <div>
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/fun">Fun</NuxtLink>
    </div>

    <Tutorial />
  </div>

</template>

<script>
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})
</script>
