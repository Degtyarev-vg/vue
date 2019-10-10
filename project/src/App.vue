<template>
  <div>
    <button class="btn btn-primary" @click="selectedComponent = 'appQuote'">appQuote</button>
    <button class="btn btn-primary" @click="selectedComponent = 'appAdd'">appAdd</button>
    <button class="btn btn-primary" @click="selectedComponent = 'appEdie'">appEdie</button>

    <!-- В компоненте Add у нас есть кнопка, которая увеличивает счетчик
    Если переключиться на другой компонент, то счетчик сбрасывается, а это
    значит, что компонент полностью удаляется. Также это можно проверить при
    помощи метода destroyed
    Но иногда, при переключении между компонентами, вы хотите сохранить их
    состояния или избежать повторной отрисовки по соображениям производительности,
    для этого есть <keep-alive> -->
    <!-- Неактивные компоненты будут закэшированы! -->
    <keep-alive>
      <component :is="selectedComponent"></component>
    </keep-alive>
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
