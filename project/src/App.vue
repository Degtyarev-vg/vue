<template>
  <div class="container">
    <appSwitch v-model="dataSwitch"></appSwitch>
    <p>Switched: {{ dataSwitch }}</p>
  </div>
</template>

<script>
  import Switch from './components/Switch'

  export default {
  	data() {
  		return {
        dataSwitch: true
      }
    },
  	components: {
      appSwitch: Switch
    }
  }
</script>

<style lang="scss">

</style>
