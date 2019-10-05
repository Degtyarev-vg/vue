<template>
  <div class="container">
    <div class="row">
      <div class="col-xl-12">
        <app-quote>
          <h1 slot="title">{{ quoteTitle }}</h1>
          <p>A wonderful Quote</p>
        </app-quote>
      </div>
    </div>
  </div>
</template>

<script>
  import Quote from './components/Quote.vue';

  export default {
    data: function() {
      return {
        quoteTitle: 'The Quote Title'
      }
    },
    components: {
      appQuote: Quote
    }
  }
</script>

<style scoped>
  /*Этот цвет не применится к заголовку, т.к. h1 используется в компоненте*/
  h1 {
    color: red;
  }
</style>
