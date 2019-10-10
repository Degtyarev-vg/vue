<template>
  <div>
    <button @click="selectedComponent = 'appQuote'">appQuote</button>
    <button @click="selectedComponent = 'appAdd'">appAdd</button>
    <button @click="selectedComponent = 'appEdie'">appEdie</button>

    <component :is="selectedComponent"></component>
  </div>
</template>

<script>
  import Quote from './components/Quote'
  import Add from './components/Add'
  import Edit from './components/Edit'

  export default {
  	data() {
  		return {
				selectedComponent: 'appQuote'
      }
    },
  	components: {
  		appQuote: Quote,
      appAdd: Add,
      appEdie: Edit
    }
  }
</script>

<style lang="scss">

</style>
