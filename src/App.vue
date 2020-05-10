<template>
  <div id="app">
  <h1> {{ listName }} </h1>
    <add-item-component/>
    <items-component/>
    <change-title-component/>
  </div>
</template>

<script>
import AddItemComponent from './components/AddItemComponent'
import ItemsComponent from './components/ItemsComponent'
import ChangeTitleComponent from './components/ChangeTitleComponent'
export default {
  name: 'App',
  data () {
    return {
      listName: 'standalone'
    }
  },
  components: { AddItemComponent, ItemsComponent, ChangeTitleComponent }
}
</script>

<style>
 #app {
     font-family: 'Avenir', Helvetica, Arial, sans-serif;
     -webkit-font-smoothing: antialiased;
     -moz-osx-font-smoothing: grayscale;
     text-align: center;
     color: #2c3e50;
     margin-top: 60px;
}
</style>
