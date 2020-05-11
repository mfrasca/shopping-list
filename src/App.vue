<template>
<div id="app" class="container">
  <h2> {{ title[0] }} </h2>
  <add-item-component :items="items" @add="addItem" />
  <items-component :items="items" />
  <div class="footer">
    <hr/>
    <change-title-component :value="title" />
  </div>
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
      items: [],
      title: ['standalone']
    }
  },
  methods: {
    addItem: function (text) {
      this.items.push({
        text: text,
        checked: false
      })
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
