<template>
  <div id="app">
    <issue></issue>
  </div>
</template>

<script>
import issue from './components/issue'

export default {
  name: 'App',
  components: {
    issue
  }
}
</script>

<style>
  @import url("../src/assets/css/init.css");
  @import url("../src/assets/css/wx_ent.css");
</style>
