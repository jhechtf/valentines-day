<template>
  <div id="app">
    <Card/>
  </div>
</template>

<script>
import Card from './components/Card';

export default {
  name: 'App',
  components: {
    Card
  }
}
</script>

<style>
@import url("https://unpkg.com/font-awesome@4.7.0/css/font-awesome.css");
@tailwind preflight;
@tailwind utilities;
</style>
