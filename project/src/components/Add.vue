<template>
  <div>
    <h1>Add</h1>
    <button class="btn btn-primary" @click="counter++">Increase</button>
    <p>{{ counter }}</p>
  </div>
</template>

<script>
  export default {
  	data() {
  		return {
  			counter: 0
      }
    },
    destroyed() {
  		console.log('Component Destroyed');
		}
	}
</script>
