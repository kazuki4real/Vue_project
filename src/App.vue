<template>
    <Clock class="clock" />
</template>

<script>
  import Clock from './components/Clock.vue';

  export default {
    components: {
      Clock,
    }
  }
</script>

<style>
  .clock {
  width: 80%;
  max-width: 500px;
  margin: 30px auto;
}
</style>
